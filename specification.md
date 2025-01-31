#DOFBOT_PROJECT_SPECIFICATION

### 1. 구성
1. 로봇 arm: 서보모터 + 알루미늄 프레임
2. 라즈베리파이 4B 보드
3. jetson_nano 확장 보드

### 2. About Jeston_Nano
* Nvidia의 임베디드 컴퓨팅 보드
* 라즈베리파이를 추가적으로 사용하는 이유
1. 라즈베리파이는 "서브 컴퓨터 역할/추가 기능 보완 "을 위해 부착
2. jetson nano의 단점: GPIO pin 부족, 고전력, OS가 무거움(ubuntu)
   + 같은 ubuntu지만 Jetson은 AI 연산을 위한 JetPack, 라즈베리파이는 경량화된 Debian기반 OS
3. Jetson은 AI를 위한 메인 연산 장치로, 라즈베리파이는 센서&제어와 같은 보조적인 가벼운 연산을 수행함

