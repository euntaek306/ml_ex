# ml_ex
머신러닝 scikit-learn 실습 - 지도학습 비지도학습

# streamlit 배포시 필수사항
- os는 linux임, 인식하는 path로 변경해야 함.
## 1. 파일 path
- 예시)모델 로딩 방법
```
#./ : 현재 디렉토리
base_path = os.path.dirname(__file__)

#모델 로드 함수
def load_model():
    model_path = os.path.join(base_path, "models", "iris_model_rfc.pkl")
    # with open('models/iris_model_lr.pkl', 'rb') as f:
    with open(model_path, 'rb') as f:
        model = pickle.load(f)
    return model
```

# requirements.txt. 파일 생성
```
pip freeze -> requirements.txt
# 예시 requrements
numpy==2.2.6
streamlit==1.51.0
joblib == 1.5.2
scikit-learn==1.7.20
```