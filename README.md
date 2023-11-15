# NetEquipConfigurator

## 소개
`NetEquipConfigurator`는 네트워크 및 서버 장비를 초기 설정하는 데 도움을 주는 파이썬 기반의 스크립트입니다. 이 프로그램은 시리얼, SSH, 텔넷 연결을 통해 다양한 장비에 접속하고, 엑셀 파일에 정의된 설정 명령을 자동으로 적용합니다.

## 기능
- **다양한 연결 지원**: 시리얼, SSH, 텔넷 연결을 통한 장비 접속 지원
- **자동 설정 적용**: 엑셀 파일에 정의된 설정을 장비에 자동 적용
- **사용자 친화적 인터페이스**: 사용 가능한 시리얼 포트 선택, 오류 메시지 출력 등

## 시작하기
이 프로그램을 사용하기 위해서는 Python이 설치되어 있어야 하며, 필요한 라이브러리를 설치해야 합니다.

### 필요 조건
- Python 3.x
- 필요한 Python 라이브러리: `pandas`, `paramiko`, `pyserial`, `telnetlib`

### 설치
필요한 라이브러리를 설치하려면 다음 명령을 실행하세요:
```bash
pip install pandas paramiko pyserial
```

## 사용 방법
이 프로그램을 사용하는 과정은 다음과 같습니다:

1. **엑셀 파일 준비**
   - `device_configs.xlsx` 파일에 각 장비의 설정 정보를 입력합니다. 이 파일에는 장비의 연결 유형(시리얼, SSH, 텔넷), IP 주소, 포트 번호, 사용자 이름, 비밀번호 등의 정보가 순차적으로 포함되어야 합니다.

2. **프로그램 실행**
   - 스크립트를 실행하면, 엑셀 파일에서 장비 설정 데이터를 읽어옵니다.

3. **장비 설정**
   - 프로그램은 엑셀 파일의 맨 위에 있는 장비부터 시작하여 순차적으로 각 장비에 접속합니다.
   - 장비에 성공적으로 접속하면, 엑셀 파일에 정의된 설정 명령어가 자동으로 입력됩니다.
     - **시리얼 연결**: 사용 가능한 시리얼 포트를 나열하고, 사용자가 선택한 포트를 통해 장비에 연결합니다.
     - **SSH 연결**: SSH를 통해 장비에 접속합니다. IP 주소, 포트 번호, 사용자 이름, 비밀번호를 사용하여 연결을 시도합니다.
     - **텔넷 연결**: 텔넷을 통해 장비에 접속합니다. IP 주소와 포트 번호를 사용하여 연결을 시도합니다.

4. **다음 장비로 이동**
   - 첫 번째 장비의 설정이 완료되면, 사용자는 다음 장비에 연결 후 엔터키를 누릅니다. 그러면 두 번째 장비에 접속하여 설정 명령어가 입력됩니다. 이 과정을 모든 장비에 반복합니다.

5. **프로그램 종료**
   - 모든 장비의 설정이 완료되면 프로그램이 종료됩니다.

이 스크립트는 네트워크 또는 서버 장비를 대량으로 초기 설정해야 할 때 시간과 노력을 절약해 줍니다. 사용자는 각 장비의 설정을 수동으로 입력할 필요 없이, 엑셀 파일에 미리 정의된 설정을 자동으로 적용할 수 있습니다.


