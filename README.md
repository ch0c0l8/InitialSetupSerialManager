# InitialSetupSerialManager

## 소개
`InitialSetupSerialManager`는 네트워크 엔지니어와 시스템 엔지니어를 위해 다수의 장비를 신속하고 효율적으로 초기 설정할 수 있도록 돕는 파이썬 스크립트입니다. 이 스크립트는 사용 가능한 시리얼 포트를 자동으로 감지하고, 엑셀 파일에 정의된 구성을 각 장비에 적용하여 일괄 설정을 간소화합니다.

## 주요 기능
- 사용 가능한 시리얼 포트 자동 감지
- 엑셀 파일을 통한 장비 구성 정보 입력
- 선택된 시리얼 포트를 통한 장비 설정 자동 적용
- 다수의 장비에 대한 일괄 설정 지원

## 시작하기
이 섹션에서는 스크립트를 사용하기 위한 기본적인 설치 방법과 실행 절차를 설명합니다.

### 필요 조건
- Python 3.x
- pandas 라이브러리
- pySerial 라이브러리

### 설치
1. Python 3.x를 설치합니다.
2. 필요한 라이브러리를 설치합니다: `pip install pandas pyserial`

### 사용 방법
1. `device_configs.xlsx` 파일에 장비 구성 정보를 입력합니다.
2. 스크립트를 실행합니다: `python InitialSetupSerialManager.py`
3. 화면의 지시에 따라 사용 가능한 시리얼 포트를 선택하고, 장비를 연결합니다.
