# NovelAI V5 Usage Monitor — 파일

## 1. Python 설치

Windows에 Python이 없다면 Python 3.10 이상을 설치하세요.

설치할 때 가능하면 다음 옵션을 체크하세요.

- `Add Python to PATH`
- `pip`

---

## 2. 필요한 패키지 한 번에 설치

`install_dependencies.bat`을 더블클릭하세요.

자동으로 아래 패키지가 설치됩니다.

- customtkinter
- requests
- pystray
- pillow
- plyer
- keyring

설치할 때는 설치 진행 상황을 보여주기 위해 터미널 창이 열립니다.

---

## 3. CMD 창 없이 실행

### 가장 쉬운 방법

`RUN_NO_CONSOLE.vbs`를 더블클릭하세요.

그러면 `pythonw.exe`를 통해 `novelai_monitor.py`가 실행되므로 **검은 CMD 창이 뜨지 않습니다.**

프로그램을 시스템 트레이로 보낸 뒤에도 콘솔 창 없이 계속 실행됩니다.

### VBS 없이 실행하고 싶다면

Python 파일 확장자를 다음처럼 바꿀 수도 있습니다.

```text
novelai_monitor.py
        ↓
novelai_monitor.pyw
```

`.pyw` 파일은 Windows에서 일반적으로 콘솔 창 없이 실행됩니다.

단, 파일명을 `.pyw`로 바꾸면 `RUN_NO_CONSOLE.vbs`의 기본 대상 파일명과 달라지므로 VBS를 쓰지 않고 `.pyw`를 직접 실행하는 편이 편합니다.

---

## 4. 바로가기 만들기

매번 폴더를 열기 싫다면:

1. `RUN_NO_CONSOLE.vbs`를 우클릭
2. `바로 가기 만들기`
3. 생성된 바로가기를 바탕화면 등 원하는 곳으로 이동

이 바로가기를 실행하면 CMD 없이 프로그램이 열립니다.

---

## 5. 토큰 저장 위치

프로그램이 `keyring`을 사용함으로써 Persistent API Token은 Python 코드 파일에 저장되는 것이 아니라 **각 사용자의 운영체제 자격 증명 저장소**에 저장됩니다.

따라서 재배포할 때 재배포자의 NovelAI 토큰이 다른 사용자에게 같이 전달되는 구조가 아닙니다.

---

## 6. 연결 해제

프로그램 내부의 `연결 해제` 버튼을 사용하면 저장된 NovelAI API Token을 삭제하도록 구성할 수 있습니다.

---

## 문제 해결

### `python` 또는 `py`를 찾을 수 없다고 나오는 경우

Python을 다시 설치하고 `Add Python to PATH`를 체크하거나, 설치된 Python의 PATH 설정을 확인하세요.

### 실행해도 아무 반응이 없는 경우

CMD 없이 실행하면 오류 메시지가 콘솔에 표시되지 않습니다.

문제 확인이 필요할 때만 임시로 다음처럼 실행하세요.

```text
python novelai_monitor.py
```

오류를 수정한 뒤 다시 `RUN_NO_CONSOLE.vbs` 또는 `.pyw` 방식으로 실행하면 됩니다.

### 시스템 트레이에 아이콘이 안 보이는 경우

Windows 작업 표시줄 오른쪽의 `^` 숨겨진 아이콘 영역도 확인하세요.
