# WIZnet IoT Shield Hardware Guide
## 시작하기 전에
### 대상 장치
- WIoT-Shield01 (Base 보드)
- WIoT-QC01 (Socket 타입 모듈)
- WIoT-WM01 (Socket 타입 모듈)
- WIoT-AM01 (Socket 타입 모듈)


## 소개

본 문서에서는 WIoT 제품들의 하드웨어 구성 및 설정에 대한 가이드를 제공합니다.

WIoT 시리즈 보드들은 아두이노, ARM MBED 및 상용 보드 플랫폼을 기반으로 다양한 무선 모듈 응용 개발에 활용 할 수 있는 연결형 보드 및 인터페이스 보드입니다.

다양한 인터페이스 보드가 연결되는 WIoT-Shield Base보드는 두 개의 USB PORT와 CDS, TEMP 센서, VoLTE용 오디오를 지원합니다. Xbee type Socket으로 제작된 Cat.M1 모듈들을 Base보드에 결합하여 사용하도록 구성되어 있으며, 각 모듈의 종류 및 테스트 환경에 따라 WIoT-Shield의  하드웨어 설정이 변경되어야 합니다.

본 가이드는 아래와 같은 순서로 구성되어 있습니다.
 * WIoT 시리즈 하드웨어 Overview
 * WIoT 시리즈 하드웨어 Settings
   * Standard alone mode
   * Arduino/MBED mode (SerialD0,D1)
   * Arduino/MBED mode (SerialD2,D8)
       


## WIoT 시리즈 모듈

### 1. WIoT-Shield01
WIoT-Shield는 Base보드로서 아두이노, Arm MBED, USB를 통해 5V 전압을 인가받아 동작하며 내부에서 3.8V, 1.8V전압을 변환하여 구동됩니다.

WIoT-Shield는 WIoT 무선 모듈의 기능 동작을 위해 Power key 세팅(HIGH/LOW), UART의 전압 세팅(3.3V/1.8V)등을 제공합니다. 또한 무선 통신을 위한 U.FL, SMA 커넥터와 VoLTE 기능이 구현되어 있습니다. 프로토타입 구현에 활용 할 수 있는 CDS(조도센서), Temp.(온도센서)가 내장되어 있어 아두이노 및 Arm MBED 플랫폼 보드와 결합하여 사용 가능합니다.

#### Features
* Arduino compatible pinout
* 3종 LTE CAT.M1 모듈 사용(Quectel,AMTelecom,Woori-net)
* Power key 세팅(HIGH/LOW)
* UART 전압 세팅(3.3V/1.8V)
* VoLTE Audio JACK 구현
* U.FL / SMA 안테나 커넥터 내장
* CDS, TEMP 센서 내장
* 모듈의 부가 기능 사용을 위해 Jumper 기능 내장
* Standard alone 동작을 위한 USB 커넥터 내장
* RNDIS기능을 위한 USB 커넥터 내장


![][1]

![][2]

###2. WIoT-QC01
WIoT-QC01보드는 앰투앰넷 BG96(Quectel) 모듈로 개발된 LTE Cat.M1 무선 모듈입니다.
무선 통신 시스템과 VoLTE기능을 사용할 수 있으며 Micro-SIM과 e-SIM중 한 가지를 제공합니다.

![][9]
![][10]

###3. WIoT-WM01
WIoT-WM01보드는 우리넷의 WM-N400MSE을 사용하기 위한 인터페이스 보드로서 PCIe 인터페이스와 JTAG기능을 제공합니다.
Nano-SIM과 e-SIM중 한 가지를 사용할 수 있습니다.

![][15]
![][16]

###4. WIoT-AM01
WIoT-AM01보드는 AMTELCOM의 AMM592을 사용하기 위한 인터페이스 보드로서 PCIe 인터페이스와 JTAG기능을 제공합니다.
Micro-SIM과 e-SIM중 한 가지를 사용할 수 있습니다.

![][3]
![][4]

## 하드웨어 설정

### 1. WIoT 보드 기본 설정
WIoT-Shield의 기본적인 설정방법은 다음과 같습니다.

* WIoT-QC01 하드웨어 설정
  * Standard alone mode
  * Arduino / MBED mode (Serial D0,D1)
  * Arduino / MBED mode (Serial D2,D8)
* WIoT-WM01 하드웨어 설정
  * Standard alone mode
  * Arduino / MBED mode (Serial D0,D1)
  * Arduino / MBED mode (Serial D2,D8)
* WIoT-AM01 하드웨어 설정
  * Standard alone mode
  * Arduino / MBED mode (Serial D0,D1)
  * Arduino / MBED mode (Serial D2,D8)

### 2. WIoT-QC01 하드웨어 설정
* Standalone mode
  * 해당 모드는 아두이노 / MBED 등 다른 MCU기기를 결합하지 않고 WIoT-QC01를 테스트할 수 있습니다.

![][12]

* Arduino / MBED mode (Serial D0,D1)
  * 해당 모드는 아두이노 / MBED 등 MCU 보드의 `D0` `D1` 핀에 할당된 UART를 Cat.M1 모듈과 연결합니다.

> **Notice) 아두이노에서 코드 컴파일 및 업로드는 WIoT-Shield의 UART Jumper 제거 후 수행해야 합니다.**

![][13]

* Arduino / MBED mode (Serial D2,D8)
  * 해당 모드는 아두이노 / MBED 등 MCU 보드의 `D2` `D8` 핀에 할당된 UART를 Cat.M1 모듈과 연결합니다.

![][14]

### 3. WIoT-WM01 하드웨어 설정
* Standalone mode
  * 해당 모드는 아두이노 / MBED 등 다른 MCU기기를 결합하지 않고 WIoT-WM01를 테스트할 수 있습니다.

![][18]

* Arduino / MBED mode (Serial D0,D1)
  * 해당 모드는 아두이노 / MBED 등 MCU 보드의 `D0` `D1` 핀에 할당된 UART를 Cat.M1 모듈과 연결합니다.

> **Notice) 아두이노에서 코드 컴파일 및 업로드는 WIoT-Shield의 UART Jumper 제거 후 수행해야 합니다.**

![][19]

* Arduino / MBED mode (Serial D2,D8)
  * 해당 모드는 아두이노 / MBED 등 MCU 보드의 `D2` `D8` 핀에 할당된 UART를 Cat.M1 모듈과 연결합니다.

![][20]

### 4. WIoT-AM01 하드웨어 설정
* Standalone mode
  * 해당 모드는 아두이노/MBED 등 다른 MCU기기를 결합하지 않고 WIoT-AM01를 테스트할 수 있습니다.

![][6]

* Arduino / MBED mode (Serial D0,D1)
  * 해당 모드는 아두이노 / MBED 등 MCU 보드의 `D0` `D1` 핀에 할당된 UART를 Cat.M1 모듈과 연결합니다.

> **Notice) 아두이노에서 코드 컴파일 및 업로드는 WIoT-Shield의 UART Jumper 제거 후 수행해야 합니다.**

![][7]

* Arduino / MBED mode (Serial D2,D8)
  * 해당 모드는 아두이노 / MBED 등 MCU 보드의 `D2` `D8` 핀에 할당된 UART를 Cat.M1 모듈과 연결합니다.

![][8]



[1]: ./imgs/WIoT_allparts.png
[2]: ./imgs/WIoT_series_Pinout.png
[3]: ./imgs/WIoT-AM01_TOP.png
[4]: ./imgs/WIoT-AM01_BOTTOM.png
[5]: ./imgs/WIoT-AM01_Pinout.png
[6]: ./imgs/WIoT-AM01_JUMP_STalone_mode.png
[7]: ./imgs/WIoT-AM01_JUMP_Arduino_serialD0_D1.png
[8]: ./imgs/WIoT-AM01_JUMP_Arduino_serialD2_D8.png
[9]: ./imgs/WIoT-QC01_TOP.png
[10]: ./imgs/WIoT-QC01_BOTTOM.png
[11]: ./imgs/WIoT-QC01_Pinout.png
[12]: ./imgs/WIoT-QC01_JUMP_STalone_mode.png
[13]: ./imgs/WIoT-QC01_JUMP_Arduino_serialD0_D1.png
[14]: ./imgs/WIoT-QC01_JUMP_Arduino_serialD2_D8.png
[15]: ./imgs/WIoT-WM01_TOP.png
[16]: ./imgs/WIoT-WM01_BOTTOM.png
[17]: ./imgs/WIoT-WM01_Pinout.png
[18]: ./imgs/WIoT-WM01_JUMP_STalone_mode.png
[19]: ./imgs/WIoT-WM01_JUMP_Arduino_serialD0_D1.png
[20]: ./imgs/WIoT-WM01_JUMP_Arduino_serialD2_D8.png





