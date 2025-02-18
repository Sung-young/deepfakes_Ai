# deepfakes
이 저장소는 CLIP, LLaMA, Grad-CAM 등 다양한 기법을 활용하여 이미지 데이터셋의 분석, 시각화, 탐지 및 레이블링을 수행하는 코드를 포함하고 있습니다. 각 파일은 특정 작업을 처리하기 위해 설계되었으며, 이를 통해 모델의 성능을 평가하거나 특정 사용 사례에 적합하도록 최적화할 수 있습니다.

## 디렉터리 구조 및 파일 설명
### 1. visualization
이미지 입력에 대한 주의 영역(Attention) 및 가중치 시각화를 수행합니다.

* **[attention_rollout_final.ipynb](https://github.com/KimEunOh/deepfakes/blob/main/visualization/attention_rollout_final.ipynb)**: Attention Rollout 기법을 활용하여 CLIP 모델의 텍스트 입력과 관련된 탐지 Heatmap 생성.
* **[Grad_CAM.ipynb](https://github.com/KimEunOh/deepfakes/blob/main/visualization/Grad_CAM.ipynb)**: Grad-CAM을 적용하여 CLIP 모델에서 텍스트 입력값에 대한 가중치를 시각화.
### 2. data
데이터셋의 임베딩, 레이블링, 형식 변환 등을 처리합니다.

* **[CLIP_RAG.ipynb](https://github.com/KimEunOh/deepfakes/blob/main/data/CLIP_RAG.ipynb)**: 데이터를 키워드 형식으로 변환 후, CLIP를 사용한 임베딩 및 유사도 계산 수행.
* **[GPT_label.ipynb](https://github.com/KimEunOh/deepfakes/blob/main/data/GPT_label.ipynb)**: GPT 모델을 활용하여 이미지 데이터셋에 대해 자동으로 레이블링.
* **[label_LLaMA.ipynb](https://github.com/KimEunOh/deepfakes/blob/main/data/label_LLaMA.ipynb)**: TogetherAI 엔드포인트를 활용하여 LLaMA 모델로 이미지 데이터셋 레이블링.
* **[llava_convert.py](https://github.com/KimEunOh/deepfakes/blob/main/data/llava_convert.py)**: 데이터를 llava에서 요구하는 형식으로 변환.
### 3. fine_tuning
LMM 모델을 파인튜닝하여 딥페이크 탐지에 최적화하는 작업을 수행합니다.

* **[tuning_Gemini_Flash.ipynb](https://github.com/KimEunOh/deepfakes/blob/main/fine_tuning/tuning_Gemini_Flash.ipynb)**: Gemini 모델의 하이퍼파라미터 튜닝 작업을 수행하여 딥페이크 탐지 성능을 최적화합니다.  
  <sub>Google Colab 환경에서 실행되었습니다.</sub>


### &nbsp;&nbsp; 3-1. LLaVA
&nbsp;&nbsp; LLaVA 모델의 WanDB 파일 및 튜닝 코드들을 포함합니다.

* **[https://huggingface.co/pou876/llava-deepfake-model](https://huggingface.co/pou876/llava-deepfake-model)**: huggingface에 업로드한 파인튜닝 모델

* **[LLaVA_tuning.ipynb](https://github.com/KimEunOh/deepfakes/blob/main/fine_tuning/LLaVA_tuning.ipynb)**: LLaVA 모델의 파인튜닝 코드

### 4. model_response
모델의 예측(Prediction) 및 점수화(Scoring) 작업을 포함합니다.

* **[Gemini_basemodel_Prediction.ipynb](https://github.com/KimEunOh/deepfakes/blob/main/response_model/Gemini_basemodel_Prediction.ipynb)**: Gemini-1.5-Flash-002 기본 모델을 사용하여 입력 데이터에 대한 예측을 수행합니다.  
  <sub>Google Colab 환경에서 실행되었습니다.</sub>
* **[Gemini_basemodel_Score.ipynb](https://github.com/KimEunOh/deepfakes/blob/main/response_model/Gemini_basemodel_Score.ipynb)**: Gemini-1.5-Flash-002 기본 모델의 점수화 작업을 통해 모델 성능을 평가합니다.  
  <sub>Google Colab 환경에서 실행되었습니다.</sub>
* **[tuned_Gemini_Prediction.ipynb](https://github.com/KimEunOh/deepfakes/blob/main/response_model/tuned_Gemini_Prediction.ipynb)**: 조정된 Gemini-1.5-Flash-002 모델을 사용하여 입력 데이터에 대한 예측을 수행합니다.  
  <sub>Google Colab 환경에서 실행되었습니다.</sub>
* **[tuned_Gemini_Score.ipynb](https://github.com/KimEunOh/deepfakes/blob/main/response_model/tuned_Gemini_Score.ipynb)**: 조정된 Gemini-1.5-Flash-002 모델의 점수화 작업을 수행하여 성능을 평가합니다.  
  <sub>Google Colab 환경에서 실행되었습니다.</sub>

* **[Llama_detection.ipynb](https://github.com/KimEunOh/deepfakes/blob/main/response_model/Llama_detection.ipynb)**: TogetherAI 엔드포인트를 사용하여 LLaMA 3.2 모델 기반으로 딥페이크 이미지 분류.

  
# 파일 추가 규칙
새로운 파일을 추가하거나 업데이트할 때는 다음 형식을 따르세요.
### 디렉터리 설명 템플릿
 ```
### **디렉터리명**
디렉터리가 포함하는 파일들의 공통적인 목적이나 기능을 설명하세요.

* **[파일명1](링크)**: 간략한 기능 설명.
* **[파일명2](링크)**: 간략한 기능 설명.
```

