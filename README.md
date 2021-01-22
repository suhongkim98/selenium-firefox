selenium-firefox
===========================================================================

## 우분투에 기본적으로 설치되어 있는 firefox를 사용한 파이썬 셀레니움 프로젝트 생성 방법입니다.
```
gecko driver: firefox를 제어하기 위한 웹 드라이버입니다.
virtualenv: 시스템에 설치된 python에 영향을 주지 않는, python 가상 환경을 프로젝트마다 만들어주는 도구입니다.
```

## 1. 프로젝트 세팅 과정

### 가. virtualenv를 설치합니다.
```
sudo pip3 install virtualenv
```

### 나. 프로젝트 폴더를 생성합니다.
```
mkdir -pv ~/selenium-firefox/drivers 
```

### 다. 해당 폴더로 이동한 후 파이썬 가상환경을 생성합니다.
```
cd ~/selenium-firefox/
virtualenv .venv
```

### 라. 가상환경을 활성화 합니다.
```
source .venv/bin/activate
```

### 마. 해당 가상환경에 pip를 이용하여 셀레니움을 설치합니다.
```
pip3 install selenium
```

### 바. gecko driver를 프로젝트의 drivers 경로에 설치합니다.

* 1) 운영체제에 맞는 gecko driver를 다운받는다. <br />
<https://github.com/mozilla/geckodriver/releases/latest/>

* 2) 명령어를 통해 프로젝트의 drivers폴더에 압축을 푼다.
```
tar -xzf ~/Downloads/geckodriver-v0.26.0-linux64.tar.gz -C ~/selenium-firefox/drivers/
```

### 사. 예제 파이썬 파일을 생성한 후 실행을 해봅니다.

## 2. PyCharm 가상환경 설정하기
```
프로젝트를 파이참에서 열어보면 가상환경이 적용되어있지 않습니다.
파이참에서 가상환경 경로를 잡아주어 프로젝트를 열 때마다 가상환경의 파이썬을 사용해봅니다.
```

### 가. File -> Settings -> project: selenium-firefox로 이동

### 나. Python Interceptor 우측 톱니바퀴 클릭 -> Show All 클릭

### 다. + 버튼을 클릭
```
New Environment혹은 Existing Environment에서 selenium-firefox 프로젝트 하위 venv폴더 내에 있는 python경로를 지정합니다.
```

### 라. Apply로 적용
