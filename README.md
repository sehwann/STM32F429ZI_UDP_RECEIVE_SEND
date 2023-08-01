# STM32F429ZI_UDP_RECEIVE_SEND
Nucleo-F429ZI LwIP 스택(RAW API)을 사용하는 UDP 송수신 구현입니다.<br>

## 개발환경

프로젝트에 사용된 환경입니다.<br>
- 디바이스 : Nucleo-F429ZI (STM32F429ZI)<br>
- 개발환경 : CUBEIDE<br>
- 사용언어 : C<br>
- 사용기능 : UART, LwIP, UDP<br>
- 통신프로그램 : Hercules, SerialPortMon<br>

## 사용 및 변경법

LAN선은 MCU-PC 직접연결하였습니다.<br>
프로젝트에 사용된 IP는 CMD의 ipconfig로 확인하여 수정하여 사용가능합니다.<br>
<br>
SEND : MCU에서 USER_BUTTON을 누르면 데이터를 전송합니다.<br>
RECEIVE : PC에서 데이터를 보낼 시, MCU에서 데이터를 수신합니다.<br>


## ipconfig설정

<img src="capture/1_ipconfig.png" width="400"><br>


## 송신모드 시 main.h 변경

<img src="capture/2_SEND_main_h.png"> <br>


## 송신 결과

<img src="capture/7_UDP_SEND.png"> <br>

## 수신모드 시 변경

<img src="capture/5_Receive_config.png"> <br>


## 수신 시, UART로 전송되는 코드

<img src="capture/6_udp_echoserver_receive_callback.png"> <br>

## 수신 결과

<img src="capture/3_PCSendMCU.png"> <br>

<img src="capture/4_PCSendMCU2.png"> <br>



<br/>

## License
(C) 2023 PETABREW. Author : sehwan.park. Version : Ver 0.1
