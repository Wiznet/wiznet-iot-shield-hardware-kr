# WIZnet IoT Shield Hardware Materials

이 저장소에는 다음 자료들이 포함되어 있습니다.
* WIZnet IoT Shield 및 Cat.M1 인터페이스 보드의 하드웨어 개발 자료
  * `Schematic`, `Gerber`, `BOM` 
  * `Pinout`, `Layout` 
* WIZnet IoT Shield 하드웨어 설정 가이드


## WIZnet IoT Shield Hardware
WIZnet IoT Shield Hardware Materials 저장소에서는 WIZnet IoT Shield의 하드웨어 설정, 보드 개발 자료 및 각종 설계 가이드 문서를 저장하고 공개합니다. 이와 더불어, 제품 활용에 필요한 각종 자료와 프로그램 등도 함께 제공합니다.

**모든 개발 자료는 공개되어 있으며, 자유롭게 활용 하실 수 있습니다.**

## Folder Structure

### /docs
다양한 인터페이스 보드를 지원하는 WIZnet IoT Shield의 모듈 별 점퍼 설정 등 다양한 하드웨어 관련 문서가 위치합니다.
* imgs: 문서에서 활용된 이미지들이 저장된 폴더입니다.

### /hardware
WIZnet IoT Shield 및 인터페이스 보드의 `Schematic`, `Gerber`, `BOM`, `Layout`, `Pinout` 등의 하드웨어 개발 자료입니다. IoT Shield 및 각 Cat.M1 모듈 벤더 별 인터페이스 보드가 각각의 폴더로 나뉘어 있으며, 하드웨어 리비전 별로 관리됩니다.
* WIoT-Shield01_Vxxx: WIZnet IoT Shield 보드의 하드웨어 개발 자료
* WIoT-QC01_Vxxx: 앰투앰넷 BG96(Quectel) 모듈 인터페이스 보드의 하드웨어 개발 자료
* WIoT-WM01_Vxxx: 우리넷 WM-N400MSE 모듈 인터페이스 보드의 하드웨어 개발 자료
* WIoT-AM01_Vxxx: AM텔레콤 AMM5918K 모듈 인터페이스 보드의 하드웨어 개발 자료

### /resources
WIZnet IoT Shield의 활용에 필요한 각종 자료 및 프로그램, 드라이버 등이 위치합니다.

### /settings
Cat.M1 모듈 종류에 따른 WIZnet IoT Shield 하드웨어 설정 정보가 위치합니다.

## Examples of content

### WIZnet IoT Shield Hardware
#### Pinout
![][shield-pinout]

#### Layout
![][shield-layout]

## Other WIZnet IoT Shield Repository
**[wiznet-iot-shield][link-wiznet-iot-shield-kr]** 저장소를 방문하면 다른 플랫폼 보드를 기반으로 동작하는 다양한 예제에 대한 저장소 리스트를 확인 할 수 있습니다.


## Support

[![WIZnet Developer Forum][forum]](https://forum.wiznet.io/)

**[WIZnet Developer Forum][link-wiznet-forum]** 에서 전세계의 WIZnet 기술 전문가들에게 질문하고 의견을 전달할 수 있습니다.
지금 방문하세요.

## License
**WIZnet IoT Shield Hardware Materials** 저장소의 모든 문서와 예제는 [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)으로 배포됩니다.



[forum]: ./docs/imgs/forum.jpg
[link-wiznet-forum]: https://forum.wiznet.io/
[link-wiznet-iot-shield-kr]: https://github.com/Wiznet/wiznet-iot-shield-kr/

[shield-layout]: ./docs/imgs/WIoT-Shield_Allparts.png
[shield-pinout]: ./docs/imgs/WIoT-Shield_Pinout.png

