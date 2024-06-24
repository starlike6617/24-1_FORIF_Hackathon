# 24-1 FORIF Hackathon

### 청춘의 AI - 퍼스널 청춘

**스터디원: 최애의 AI**  

---

## 프로젝트 소개 (Introduction)

### 프로젝트 배경 (Background)
우리 주변에는 다양한 청춘이 존재합니다. 우리는 AI를 활용하여 청춘들의 이미지를 진단하고, 본인만의 스타일 구축에 도움을 주고자 "퍼스널 청춘"을 개발했습니다.

There are many different youth around us. We developed "Personal Youth" to diagnose the images of these youths using AI and help them build their own unique style.

### 주요 기능 (Key Features)
1. **청춘 MBTI 분류 (Youth MBTI Classification)**
   - 사용자가 얼굴 사진을 업로드하면 AI가 청춘 유형을 분류합니다.
   - The user uploads a facial photo, and the AI classifies the youth type.

2. **청춘 유형 (Youth Types)**
   - 활기찬 (Energetic) - 잔잔한 (Steady)
   - 따뜻한 (Warm) - 차가운 (Cold)
   - 힙한 (Hip) - 우아한 (Graceful)
   - 귀여운 (Adorable) - 성숙한 (Mature)

---

## 동작 원리 (How It Works)

1. **이미지 업로드 (Image Upload)**
   - 사용자가 자신의 얼굴 사진을 업로드합니다.
   - The user uploads their facial photo.

2. **AI 분석 (AI Analysis)**
   - 업로드된 이미지는 AI 모델에 의해 분석됩니다.
   - The uploaded image is analyzed by the AI model.

3. **청춘 유형 분류 (Youth Type Classification)**
   - AI 모델은 분석된 이미지를 바탕으로 사용자의 청춘 유형을 분류합니다.
   - Based on the analyzed image, the AI model classifies the user's youth type.

4. **결과 제공 (Results Provision)**
   - 사용자는 자신의 청춘 유형과 관련된 설명을 받습니다.
   - The user receives an explanation related to their youth type.

---

## AI 모델 설명 (AI Model Description)

### AI 모델 아키텍처 (AI Model Architecture)

1. **모델 구조 (Model Structure)**
   - 우리의 AI 모델은 얼굴 인식과 감정 분석에 최적화된 합성곱 신경망(CNN, Convolutional Neural Network)을 사용합니다. CNN은 이미지 데이터의 공간적 계층 구조를 효과적으로 학습하는 데 유리합니다.
   - Our AI model utilizes a Convolutional Neural Network (CNN) optimized for facial recognition and emotion analysis. CNNs are advantageous for effectively learning the spatial hierarchies in image data.

2. **전이 학습 (Transfer Learning)**
   - 대규모 얼굴 이미지 데이터셋으로 사전 학습된 모델(VGG16, ResNet 등)을 사용하여 전이 학습을 수행했습니다. 이를 통해 학습 시간을 단축하고, 높은 정확도를 달성했습니다.
   - We performed transfer learning using pre-trained models (such as VGG16, ResNet) on large facial image datasets. This approach shortened training time and achieved high accuracy.

3. **데이터 전처리 (Data Preprocessing)**
   - 입력 이미지의 크기를 모델에 맞게 조정하고, 정규화 과정을 통해 데이터의 일관성을 유지했습니다.
   - The input images were resized to fit the model and normalized to maintain data consistency.

4. **특징 추출 (Feature Extraction)**
   - CNN을 사용하여 입력 이미지에서 저수준 특징(에지, 텍스처 등)부터 고수준 특징(얼굴 구조, 표정 등)까지 추출했습니다.
   - Features were extracted from the input images using CNN, from low-level features (edges, textures) to high-level features (facial structures, expressions).

5. **청춘 유형 분류 (Youth Type Classification)**
   - 최종 레이어에서 소프트맥스(Softmax) 함수를 사용하여 입력 이미지가 어떤 청춘 유형에 속하는지 확률적으로 분류했습니다.
   - The final layer utilized a Softmax function to probabilistically classify the input image into one of the youth types.

### 학습 과정 (Training Process)

1. **데이터 수집 (Data Collection)**
   - 다양한 청춘 유형을 대표하는 얼굴 이미지를 수집하여 학습 데이터셋을 구성했습니다.
   - Facial images representing various youth types were collected to form the training dataset.

2. **데이터 증강 (Data Augmentation)**
   - 데이터 증강 기법(회전, 이동, 스케일링 등)을 적용하여 모델의 일반화 능력을 향상시켰습니다.
   - Data augmentation techniques (rotation, translation, scaling) were applied to improve the model's generalization ability.

3. **모델 학습 (Model Training)**
   - 수집된 데이터를 사용하여 모델을 학습시키고, 학습률 조정 및 조기 종료(Early Stopping) 기법을 적용하여 최적의 성능을 도출했습니다.
   - The model was trained using the collected data, with learning rate adjustments and early stopping techniques applied to derive optimal performance.

4. **모델 평가 (Model Evaluation)**
   - 별도의 검증 데이터셋을 사용하여 모델의 성능을 평가하고, 정확도(Accuracy), 정밀도(Precision), 재현율(Recall) 등의 지표를 분석했습니다.
   - The model's performance was evaluated using a separate validation dataset, analyzing metrics such as accuracy, precision, and recall.
