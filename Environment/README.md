# 개발 환경 구성
MacOSX 에서 ARM 기반 Embeded Firmware 개발을 위한 개발환경 구성

## 컴파일러 설치
gcc-arm-[Platform]-[ABI Type]

Platform: linux와 none 2가지 존재

linux는 ARM용으로 동작하는 리눅스의 실행 파일을 만드는 것이 목적, none은 플랫폼이 없다는 의미로 날것 그대로의 ARM 바이너리를 생성해 준다는 의미

ABI(Application Binary Interface)는 C언어에서 함수 호출을 어떻게 하느냐를 정해놓은 규약, 어떤 레지스터를 몇 번째 파라미터에 배정하고 스택과 힙은 어떻게 쓰고 하는 것 등을 정해놓은 규약

-  gcc-arm-none-eabi 설치
```
$ brew tap PX4/homebrew-px4
$ brew update
$ brew install gcc-arm-none-eabi
```

## QEMU 설치
QEMU는 x86, ARM등 여러 환경을 가상 머신으로 사용할 수 있는 에뮬레이터

Install the QEMU
```
$ brew install qemu
```

qemu-system-arm 버전 확인
```
$ qemu-system-arm --version
```

qemu-system-arm이 지원하는 머신 목록
```
$ qemu-system-arm -M ?
```

