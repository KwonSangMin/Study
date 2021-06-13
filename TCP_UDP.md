1. UDP :  비연결형 프로토콜 -> 재전송, 순서 정립 X
          IP 프로토콜을 통해서 들어온 패킷에게 Port 번호를 통해 Process를 특정한다.
          비연결형이라 데이터를 보냇을 때 손실될 수도 있지만, TCP처럼 연결 성립과정이 없으므로 Overhead가 적다. 따라서, 비디오 스트리밍이나 DNS에서 사용된다.
          
2. TCP :  연결형 프로토콜 -> 패킷이 수신지에 도착하지 않거나 오류가 날 경우 재전송, 혼잡제어, 흐름제어 기능을 제공한다
          -흐름제어 : 송신측과 수신측의 데이터 처리 속도 차이를 해결하기 위한 기법
                    * Stop and Wait : 전송 패킷에 대한 ACK 신호를 받아야 다음 패킷을 전송. 데이터 전송 속도면에서 비효율적
                    * Sliding Window : 3-way hand shaking 과정을 통해서 Send window size와 Recive window size를 교환하여 정하고 해당 size만큼의 패킷을 한 번에 보낸 뒤 ACK를 관리
          -혼잡제어 : 특정 네트워크에 패킷이 과부하된 경우 송신측의 패킷 전송 속도를 조절하는 방법
                    * AIMD : 네트워크에 문제가 없을 시 전송량 1씩 증가, 문제 발생시 절반으로 감소
                    * Slow Start : 전송량 2배씩 증가, 임계점(Threshold) 이후에는 1씩 증가, 문제 발생 시 1부터 다시 시작