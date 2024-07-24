# -
## OSI 7계층
![image](https://github.com/user-attachments/assets/d7a6e39c-8eeb-495c-b92f-2df4f7cbcc78)
네트워크에서 통신이 일어나는 과정을 7단계로 나눈 것을 말한다. 계층을 나눈 이유는 통신이 일어나는 과정을 단계별로 파악할 수 있기 때문이다. 7단계 중 특정한 곳에 이상이 생기면 다른 단계의 장비 및 소프트웨어를 건들이지 않고도 이상이 생긴 단계만 고칠 수 있기 때문이다.

### 1계층 - 물리 계층(Physical Layer)
### 2계층 - 데이터링크 계층(DataLink Layer)
### 3계층 - 네트워크 계층(Network Layer)
### 4계층 - 전송 계층(Transport Layer)
### 5계층 - 세션 계층(Session Layer)
### 6계층 - 표현 계층(Presentation Layer)
### 7계층 - 응용 계층(Transmission Control Protocol)


## TCP와 UDP의 비교
### UDP
UDP(User Datagram Protocol, 사용자 데이터그램 프로토콜)은 비연결형 프로토콜이다.

IP 데이터그램을 캡슐화하여 보내는 방법과 연결 설정을 하지 않고 보내는 방법을 제공한다. UDP는 흐름제어, 오류제어 또는 손상된 세그먼트의 수신에 대한 재전송을 하지 않는다. 이모두가 사용자 프로세스의 몫이다. UDP가 행하는 것은 포트들을 사용하여 IP 프로토콜에 인터페이스를 제공하는 것이다.

종종 클라이언트는 서버로 짧은 요청을 보내고, 짧은 응답을 기대한다. 만약 요청 또는 응답이 손실된다면, 클라이언트는 time out 되고 다시 시도할 수 있으면 된다. 코드가 간단할 뿐만 아니라 TCP 처럼 초기설정에서 요구되는 프로토콜보다 적은 메시지가 요구된다.

UDP를 사용하는 것들에는 DNS가 있다. 어떤 호스트 네임의 IP 주소를 찾을 필요가 있는 프로그램은, DNS 서버로 호스트 네임을 포함한 UDP 패킷을 보낸다. 이 서버는 호스트의 IP주소를 포함한 UDP 패킷으로 응답한다. 사전에 설정이 필요하지 않으며 그 후에 해제가 필요하지 않다.

### TCP
대부분의 인터넷 응용 분야들은 신뢰성과 순차적인 전달을 필요로 한다. UDP로는 이를 만족시킬 수 없으므로 다른 프로토콜이 필요하여 탄색한 것이 TCP이다.
TCP(전송 제어 프로토콜)은 신뢰성이 없는 인터넷을 통해 종단간에 신뢰성 있는 바이트 스트림을 전송하도록 특별히 설계되었다. TCP 서비스는 송신자와 수신자 모두가 소켓이라고 부르는 종단점을 생성함으로써 이루어진다. TCP에서 연결 설정은 3-way handshake를 통해 행해진다.

모든 TCP 연결은 전이중, 점대점 방식이다. 전이중이란 전송이 양방향으로 동시에 일어날 수 잇음을 의마하며 점대점이란 각 연결이 정확히 2 개의 종단점을 가지고 있음을 의미한다. TCP는 멀티캐스팅이나 브로드캐스팅을 지원하지 않는다.

