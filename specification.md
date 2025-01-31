# DOFBOT_PROJECT_SPECIFICATION

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
4. cpu는 ARM Cortex

### 3. Nvidia Jetpack
1. Nvidia가 개발한 소프트웨어 개발 키트로 GPU와 여러 라이브러리를 제공
2. GPU 드라이버, CUDA, Tensor, cuDNN을 제공

### 4. ROS(멜로딕)
1. dofbot의 OS는 Ubuntu+ROS; 로봇 개발 환경에서는 이러한 운영체제 조합이 흔히 사용된다고 함
2. ROS는 완전한 운영체제는 아니고 로봇 소프트웨어 프레임워크(플랫폼)
3. 즉 로봇 미들웨어(제어코드-미들웨어-OS, 즉 프로그램 간의 연결을 가능하게 함)
   하드웨어 (센서, 모터, 카메라)
   펌웨어 (모터 컨트롤러, 센서 드라이버)
   운영체제 (Linux, Ubuntu)
   ROS (로봇 미들웨어)
   로봇 제어 코드 (Python, C++ 프로그램)
5. ROS 역할: 하드웨어 추상화, 메시지 통신, 로봇 알고리즘 지원(SLAM 등)
6. ROS에 대해서 좀 더 알아보자..
