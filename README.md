# Notebooks As Sandbox

이 저장소는 노트북을 이용해 새로운 개념을 빠르게 실험하고, 아주 가벼운 PoC를 해보는 개인용 샌드박스입니다.

복잡한 구조나 배포를 목표로 하지 않으며, 아이디어 검증과 학습에 초점을 둡니다.

## Getting Started

### Prerequisites

- Python 3.12.x
- pyenv 설치 및 기본 사용법
- 선택 사항
    - JupyterLab 또는 Jupyter Notebook
    - ffmpeg(오디오/비디오 처리 실험 시)
    - Chrome/ChromeDriver(웹 자동화/스크래핑 실험 시)

### Installation

1) pyenv로 Python 3.12 설치 및 프로젝트에 지정

    ```bash
    pyenv install 3.12.11
    pyenv local 3.12.11
    python -V  # Python 3.12.11 확인
    ```

2) Poetry 설치

    - 공식 설치 스크립트(권장)

         ```bash
         curl -sSL https://install.python-poetry.org | python3 -
         # 설치 경로를 PATH에 추가 (쉘에 따라 한 줄 추가)
         # bash/zsh: echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc  # 또는 ~/.zshrc
         # fish: set -U fish_user_paths $HOME/.local/bin $fish_user_paths
         ```

    - 설치 확인

        ```bash
        poetry --version
        ```

3) Poetry를 pyenv Python으로 가상환경 생성하도록 설정

    ```bash
    # 프로젝트 루트에서 실행
    poetry env use 3.12.11   # 또는: poetry env use $(pyenv which python)
    poetry config virtualenvs.in-project true
    ```

4) 의존성 설치

    - 기본 의존성만

        ```bash
        poetry install
        ```

    - 노트북/개발 도구까지 함께

        ```bash
        poetry install --extras dev
        ```

5) 가상환경 활성화 및 확인

    ```bash
    poetry shell
    python -V
    ```

## Usage

- JupyterLab 실행
  ```bash
  jupyter lab
  ```
  또는
  ```bash
  jupyter notebook
  ```

## Code Style

- 간단한 샌드박스지만, 기본 코드 품질 유지를 위해 Ruff를 권장합니다.
    - 설치
      ```bash
      pip install ruff pre-commit
      ```
    - 린트
      ```bash
      ruff check .
      ```
    - 포맷팅
      ```bash
      ruff format .
      ```
    - 선택: 커밋 전 자동 체크
      ```bash
      pre-commit install
      ```
