# Jupyter Notebooks 프로젝트

이 저장소는 python 으로 진행하는 다양한 작업을 위한 주피터 노트북을 모아두는 프로젝트입니다.

## 환경 설정

이 프로젝트는 Python 3.12와 Poetry를 사용하여 의존성을 관리합니다.

### 설치 방법

1. Poetry 설치 (아직 설치하지 않은 경우):
   ```bash
   pip install poetry
   ```

2. 의존성 설치:
   ```bash
   poetry install
   ```

3. 주피터 노트북 설치 및 실행:
   ```bash
   poetry add jupyter
   poetry run jupyter notebook
   ```

## 기능

이 저장소에는 다음과 같은 패키지가 포함되어 있습니다:

- **데이터 처리**: numpy, pandas
- **시각화**: matplotlib, seaborn
- **웹 스크래핑**: selenium, webdriver-manager
- **이미지 처리**: pillow
- **API 연동**: requests, notion-client
- **Notion 연동**: notion-client, notion2md
- **환경 설정**: python-dotenv

## 코드 스타일

이 프로젝트는 코드 스타일을 위해 Ruff를 사용합니다:
- Black 스타일
- isort 스타일

### 린트 실행

```bash
poetry run ruff check .
```

### 포맷팅 실행

```bash
poetry run ruff format .
```

## 라이선스

내부 사용 목적으로 작성되었습니다.
