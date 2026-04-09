# 🛰️  Satellite Image Building Segmentation                                                                                    
                                                                                                                        
  이 프로젝트는 위성 이미지를 분석하여 건물(Building) 영역을 세그멘테이션하는 딥러닝 모델 프로젝트입니다.                       
  **Google Colab** 환경에 최적화되어 있어, 데이터셋을 구글 드라이브에 업로드하기만 하면 클릭 한 번으로 즉시 학습 및 추론이      
  가능합니다.                                                                                                                   
                  
  ## 🚀 Quick Start (One-Click Run)                                                                                             
                  
  사용자는 별도의 로컬 환경 구축 없이 아래 버튼을 통해 바로 실행할 수 있습니다.                                                 
                  
  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)              
                  
  ### 🛠️  실행 방법 (Instructions)                                                                                               
                  
  1. **데이터 준비**:                                                                                                           
     - 학습에 사용할 데이터셋(`open.zip`)을 준비합니다.
     - 본인의 **Google Drive** 최상단 경로(My Drive)에 `open.zip` 파일을 업로드합니다.                                          
  2. **Colab 실행**:                                                                                                            
     - 상단의 **"Open in Colab"** 버튼을 클릭합니다.                                                                            
  3. **드라이브 마운트 및 실행**:                                                                                               
     - 실행 시 나타나는 팝업에서 구글 드라이브 접근 권한을 승인합니다.                                                          
     - 코드가 자동으로 `open.zip`의 압축을 풀고, 모든 경로를 설정하며 학습을 시작합니다.                                        
                                                                                                                                
  ---                                                                                                                           
                                                                                                                                
  ## 🔍 Project Details                                                                                                         
                  
  ### 🤖 Model Architecture                                                                                                     
  - **Base Model**: EfficientNet-B0
  - **Task**: Semantic Segmentation (Single-channel mask prediction)                                                            
  - **Optimization**: Mixed Precision Training (FP16)을 사용하여 학습 속도를 극대화했습니다.                                    
                                                                                                                                
  ### 🧪 Data Pipeline                                                                                                          
  - **Augmentation**: Albumentations를 활용한 고성능 데이터 증강 (Crop, Brightness, Color Jitter, Coarse Dropout 등)            
  - **Preprocessing**: EfficientNet에 최적화된 Normalize 및 Resize 적용                                                         
                                                                                                                                
  ### 📊 Dataset Structure                                                                                                      
  본 코드는 `open.zip` 내에 다음과 같은 구조가 있다고 가정합니다:                                                               
  - `train.csv`, `test.csv`: 이미지 경로 및 RLE 마스크 정보 포함                                                                
  - `train_img_XXXX.png`: 학습용 이미지 파일                                                                                    
                                                              
