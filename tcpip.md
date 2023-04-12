# 1
IP 프로토콜 위에서 실행되는 전송 계층 프로토콜은 연결형 서비스를 지원하는 TCP와 비연결형서비스를 지원하는 UDP, 두 종료로 구분한다. 이때 TCP는 UDP와 달리 신뢰성있는 데이터 전송을 보장한다. 

TCP는 신뢰할 수 있는 데이터 전송을 보장하기 위해서 데이터 전송 시 각 패킷에 시퀀스 번호를 할당한다. 데이터를 받는 쪽에서는 보낸 쪽에서 ACK(Acknolwedge, 확인응답) 메세지를 다시 전송하여 각 패킷의 수신을 확인한다. 보낸 사람은 다음 패킷을 보내기 전에 ACK 메세지를 기다려 패킷이 올바른 순서로 수신되고 있는지를 확인한다. 이때 누락된 패킷이 있다면 재전송한다. 이를 통해 데이터 전송 순서를 유지하여 안정적이고 신뢰가능한 데이터 전송이 가능해진다.

TCP에서는 데이터가 전송되고, 이후 메세지가 교환되는 동안 양측이 계속 연결을 유지한다. 처리해야하는 작업량이 많기 때문에 UDP보다 속도가 느리다. 그래서 스트리밍, 온라인 게임 등 타이밍이 중요한 작업에는 적절하지 않고, 높은 안정성이 필요한 경우 적합하다.
# 2
TCP/IP는 송신자가 수신자에게 IP 주소를 사용하여 End-to-End로 규약(ACK/NACK)에 따라 데이터를 전달하고 그 데이터가 제대로 갔는지, 받았다고 연락이 오는지 등을 확인하며 신뢰성 있는 통신을 할 수 있도록 합니다.
# 3
시스템에 상관없이 서로의 시스템이 연결될 수 있도록 만들어주는 모델인 OSI을 4개 레이어로 만들어 사용한다. 
1. Application Layer : 네트워크를 사용하는 응용프로그램으로 이루어진다.
2. Transport Layer : 데이터를 전송하기 위한 일을 하는 계층. 각 시스템을 연결하고 TCP를 이용해 데이터를 전송한다. (전송 목적지 지정, 오류없이 전송)
3. Internet Layer : 데이터를 정의하고 데이터의 경로를 배정하는 일(라우팅)을 담당. 데이터 라우팅을 위해 IP를 사용한다. (단일 주소 지정방식이 필요해 IP 주소를 사용함)
4. Physical Layer : 하드웨어. 실제 데이터 송수신 담당, 물리 주소를 사용한다.
이 4개 레이어를 통해 데이터를 주고받는다.
사용자가 브라우저 같은 Application Layer를 통해 데이터를 특정 서버에 요청하면, 이 요청을 TCP 패킷으로 변환하여 Transport Layer에 전달하고, Internet Layer를 통해 IP 패킷을 만들어 Physical Layer로 전달한다. 연결을 통해 특정 서버의 Physical Layer로 패킷이 전달되면, 이는 그 서버의 Internet Layer에서 수신자가 자신의 IP주소가 맞는지 판별, 맞다면 Transport Layer로 패킷을 전달한다. 전달받은 TCP 패킷을 해석하여 필요한 데이터를Application Layer에 요청하는데, 이 과정에서 패킷의 순서를 재조합하거나 누락된 패킷이 있을 경우 재전송을 요청한다. 이처럼 데이터 손실을 자체적으로 처리하기 때문에 데이터의 신뢰성을 확보할 수 있다. 이렇게 특정 서버의 Application Layer 에서 데이터를 확보하면 다시 Transport Layer, Internet Layer의 역순서를 거쳐 다시 똑같은 방법으로 사용자의 Application Layer에 데이터가 도착하게 된다.
# 4
먼저 TCP/IP란 뭘까? TCP/IP는 인터넷 프로토콜 스위트로, 인터넷과 이와 유사한 컴퓨터 네트워크 사이에서 정보를 주고받는 데 이용되는 통신 프로토콜의 모음이다. 예전에 우리가 우편 서비스를 이용하려면 정해진 규칙에 따라 직접 봉토에 이름과 주소를 쓰고 우표를 붙여서 우편함에 넣었다. 이러한 규칙은 우체부가 우편을 처리하기 용이했다. 유사하게 인터넷상에서도 정보의 전송 수신을 위해서는 규칙이 존재한다. 이러한 규칙을 TCP/IP 모델이라고 부른다. TCP/IP는 우리가 온라인상에서 안전하고 효율적으로 데이터를 전송할 수 있도록 규칙을 정의하고있다. 
TCP/IP모델은 두개의 기기간에 데이터를 전송하는 것을 담당하고 있다. 마치 대중교통처럼 전송할 데이터를 개별 패킷으로 잘개 쪼개어 개별적으로 전송한다. 모든 데이터 교환에는 2개의 기기만 개입된다. 
  이제 TCP/IP가 reliable communication 기능을 구현하는 작동 원리에 대해 알아보자.
TCP는 6가지 방식으로 communication기능을 reliable하게 한다. 첫번째, End-to-End이다. 인터넷 상에서는 여러 패킷을 거쳐 정보가 전달되는데, 중간에 거치는 패킷이 어떤 과정을 거치는지에 관계없이 출발 도착을 중요시한다. 이로인해 과정이 복잡하던 간단하던 목표인 정보전달은 확실히 가능해지는 것이다. 두번째, ANK이다. acknowledge의 줄임말로, 전송한 데이터가 도착했다고 알려주는 것이다. 세번째, NACK이다. 전송한 데이터가 도착하지 않았다고 알려주는 것이다. 중요한 정보를 상대가 받았는지 못받았는지 알아야 reliable한 communication이 된다. 네번째, Timeout and Retransmission이다. 송신자가 정보를 보냈는데, 수신자가 정보를 받았는지 안받았는지 답이없다면, 송신자는 합의 없이 정보를 다시 보낸다. 상대가 답이 없어도 정보를 보내는 것이 목적이기 때문에 불확실하다면 다시 보내는 것이다. 다섯번째, Handle Mis-sequenced Packet(sequence number)이다. 예를 들어 12345를 송신자가 순서대로 보냈다고 가정하자. 3의 루트가 멀어서 수신자는 12453의 순서대로 받았다. 그럼에도 수신자는 다시 순서를 맞출 수 있다. 정확한 정보전달이 가능해지는 것이다. 여섯번째, Handle Duplicated Packet이다. Timeout and Retransmission으로 송신자가 같은 정보를 두번 보냈다고 하자. 예를 들어 늦는 3을 받지 못하것으로 인지해 123453을 보낸다. 수신자는 124533을 받게 되고 3이 두번 왔기에 중복되는 하나를 버릴 수 있다. 이렇게 여섯가지 규칙에 따라 통신을 주고받는다. 이러한 방식을 사용하면 정보의 누락없이 정확하게, 그리고 서로 받았는지 못받았는지 반응을 해주며 reliable한 communication이 가능해지는 것이다.
# 5
packet switching은 여러 경로를 거쳐서 packet을 source로 부터 destination까지 전달하게 된다. 따라서 우선 Internet layer에서는 IP protocol을 사용하여 각 패킷이 출발지로부터 목적지까지 잘 도착하도록 라우팅을 해준다. 여기서는 패킷을 효율적으로 보낼 수 있는 경로를 설정하기 위해 라우팅 알고리즘을 사용한다. TCP (Transport Control Protocol)는 transport layer의 protocol인데, acknowledgement 정보를 사용하여 패킷이 잘 전달되었는지 확인하고, 모든 패킷들의 sequence 정보를 저장하여 패킷이 올바른 순서로 전달되도록 한다. 잘못된 순서로 패킷이 전달되는 경우를 mis-sequenced packet이라고 하는데, TCP는 이러한 것을 detection하고 해결할 수 있도록 설계된 protocol이다. TCP는 이외에도 Timeout이나 Retransmission 등의 기능을 제공하여 결국 end-to-end에서의 reliable한 connection을 가능케 한다.
# 6
TCP IP의 reliable communication 의 실체는 TCP IP의 transport layer이다. Transport layer는 인터넷상에서 데이터를 전송하는 과정에서 데이터의 송수신을 관리하는 역할을 담당한다. TCP IP는 TCP 프로토콜을 이용하여 데이타를 전송한다. Transport Layer에서는 두 가지 프로토콜이 사용된다. Transmission Control Protocol(TCP)과 User Datagram Protocol(UDP)이다. TCP 프로토콜은 데이터의 정확성과 신뢰성을 보장하기 위해 설계된 프로토콜이다. 이 프로토콜은 데이터를 보낼 때 먼저 세션을 설정하고, 세션을 유지하면서 데이터를 보내고, 데이터의 정확성을 확인하고, 세션을 종료하는 과정을 거친다. 이러한 과정을 통해 TCP는 데이터 전송의 안정성과 신뢰성을 보장한다. 이와 달리, UDP 프로토콜은 데이터의 손실이나 중복 등의 오류를 보장하지 않는다. UDP는 간단하고 빠른 데이터 전송을 위해 사용되며, 데이터 전송 속도가 빠르고 부담이 적은 서비스에 적합하다.
# 7
TCP와 IP는 인터넷에서 데이터를 전송하는 데 사용되는 프로토콜으로, TCP는 전송 제어 프로토콜이며, IP는 인터넷 프로토콜이다.

TCP는 reliable communication을 제공하기 위해 다음과 같은 원리를 사용한다.
먼저, 데이터 세그먼트를 보낼 때, 수신 측에서 확인 응답을 보내기 전까지는 세그먼트를 계속해서 재전송하고 이를 통해 세그먼트의 손실이나 손상을 탐지하고 복구할 수 있다.
그리고 데이터 세그먼트를 보낼 때, 각 세그먼트는 일련번호를 가지고 있다. 수신 측에서는 이 일련번호를 사용하여 세그먼트의 순서를 추적하고, 누락된 세그먼트를 재전송할 수 있다.
또한 TCP는 흐름 제어를 통해 데이터 전송 속도를 조절하고 수신 측에서는 자신의 버퍼 용량을 넘어서는 데이터를 수신하지 않도록 TCP 연결의 윈도우 크기를 조정한다.
마지막으로 TCP는 혼잡 제어를 통해 네트워크의 혼잡 상황을 탐지하고 데이터 전송 속도를 조절하며, 혼잡 상황이 발생하면 TCP는 전송 속도를 감소시켜 혼잡 상황을 완화한다.

IP는 각 패킷에 대한 주소 정보를 제공하고, 패킷을 목적지로 전달한다. IP는 데이터 전송의 신뢰성을 보장하지 않지만, 데이터의 분할과 재조립을 처리하여 큰 데이터 파일을 전송할 수 있도록 한다.
TCP는 IP와 함께 사용되어, 데이터 전송의 신뢰성을 보장하고, IP의 한계를 보완한다.
# 8
IP는 인터넷에서 데이터를 전송하는 데 사용되는 프로토콜입니다. IP는 데이터그램(Datagram)이라는 패킷 단위로 데이터를 전송합니다. IP는 전송 중에 패킷 손실, 중복, 순서 변경 등과 같은 문제를 처리하지 않습니다.

반면에, TCP(Transmission Control Protocol)는 IP 위에서 작동하는 프로토콜로, 데이터의 신뢰성을 보장합니다. TCP는 데이터를 전송하기 전에 연결을 설정하고, 전송이 완료될 때까지 연결을 유지합니다. 이 때, TCP는 전송 중에 발생할 수 있는 문제들을 처리합니다. 

TCP와 IP는 함께 동작하여 데이터의 전송 경로를 결정하고, 데이터를 신뢰성 있게 전송합니다. IP는 데이터그램을 전송하고, TCP는 이를 관리하여 데이터의 신뢰성을 보장합니다. 이러한 방식으로 TCP와 IP는 reliable communication 기능을 만들어냅니다
# 9
TCP/IP 프로토콜 스택은 인터넷에서 데이터 전송을 관리하기 위한 프로토콜 집합이다. TCP/IP                                                                                                                                             프로토콜 스택은 물리적으로 연결된 호스트 간에 데이터를 전송하기 위한 표준 프로토콜을 제공한다.

TCP/IP의 reliable communication 기능을 만들어내는 원리는 첫번째로 TCP 프로토콜은 데이터를 작은 조각으로 나누어 전송하는 것이다. 각 패킷에는 시퀀스 번호가 할당된다. 이를 통해 수신측에서 패킷의 순서를 확인할 수 있다. 수신측에서는 수신한 패킷의 순서를 확인하고 응답을 전송합니다. 송신측은 수신측으로부터 확인 응답을 받지 못하면 패킷을 다시 전송한다. 송신측은 일정 시간동안 확인 응답을 받지 못하면 패킷을 재전송한다. TCP는 오류 제어 및 흐름 제어를 위해 여러 가지 기술을 사용한다. 이를 통해 데이터의 손실을 최소화하고, 데이터 전송을 더욱 신뢰성 있게 만든다.
# 10
TCP 프로토콜 자체가 전송된 모든 것이 수신 측에서 전달되었는지 확인한다. TCP는 손실된 packet의 재전송을 허용하여 전송된 모든 데이터가 수신되도록 한다.
# 11
Packet switching은 네트워크에서 데이터를 전송하는 방식 중 하나로, 데이터를 작은 단위인 패킷(packet)으로 분할하여 전송하는 방식입니다. IP와 TCP 프로토콜은 이러한 패킷 switching 방식을 기반으로 데이터를 전송하는데 사용됩니다.

IP는 인터넷 프로토콜의 약자로,Packet switching 방식을 기반으로 하는 네트워크 프로토콜입니다. IP 프로토콜은 데이터를 패킷으로 분할하고, 목적지 주소를 지정하여 네트워크를 통해 다양한 경로로 패킷을 전달합니다. IP 프로토콜은 라우팅 기능을 제공하여, 패킷이 목적지까지 가장 빠르게 전달될 수 있도록 합니다. 하지만 전달되는 도중에 일부 패킷이 손실될 수 있습니다. 그래서 이 단점을 보완하기 위한 TCP가 있습니다. 

TCP(Transmission Control Protocol)는 인터넷 상에서 데이터를 신뢰성 있게 전송하기 위한 프로토콜 중 하나입니다. 먼저, TCP는 ENd to end 프로토콜로 송신자와 수신자가 서로 통신해서 라우터는 그 연결을 방해하지 않습니다. 
데이터가 제대로 전달되었는지 알려주는 ACK, 수신자가 데이터 패킷을 제대로 받지 못 했을 경우 보내는 NACK, 패킷을 보냈는데 일정 시간 안에 ACK가 오지 않으면 재전송하는 Timeout and Retransmission 기능, TCP가 부여한 데이터의 일련 번호의 순서가 틀리다면 잠시 작업을 중단하게 만들어서 순서에 맞게 데이터를 작업하게 도와주는 Handle Mis-requenced Packet 기능, 중복된 데이터 패킷을 수신자가 삭제하게 만드는 Handle Duplicated Packet 기능으로 데이터가 제대로 전송될 수 있도록 돕습니다. 

위처럼 IP와 TCP는 송신자와 수신자 간에 데이터의 손실, 왜곡 또는 중복 등의 문제가 발생하지 않도록 보장하는 통신 방식인 Reliable communication을 구현합니다.
# 12
TCP와 IP는 인터넷에서 데이터를 교환하는 데 사용되는 네트워크이다. TCP는 reliable communication을 위해 ACK와 NACK라는 응답 메세지를 통해 패킷이 목적지까지 잘 전송되었는지 확인한다. 만일 응답 메세지를 통해 데이터 패킷이 잘 전달되지 않았다는 것이 파악된다면 재전송한다. IP는 데이터 패킷을 라우터로 전송하고, 라우터는 패킷을 다른 라우터로 전송하거나 최종 목적지로 전송합니다. 이 때 라우터는 패킷에 나타나있는 목적지의 IP 주소를 바탕으로 효율적인 경로로 데이터 패킷을 전달하는 라우팅 과정을 거친다.
# 13
TCP/IP 는 인터넷 네트워크의 핵심 프로토콜이며 컴퓨터 간의 주고받는 메세지를 전송할 때 에러가 발생하지 않도록 알맞은 크기로 나뉘어져 전송하고 이를 받아서 다시 원래의 정보로 변환하는 것을 약속하는 것이다. 이때 TCP는 데이터를 보낼 때 각각의 패킷에 시퀸스 번호와 확인 응답 번호를 포함해 세분화한다. 데이터를 보낸 후 기다린 후에 응답을 받지 못한 패킷은 재전송한다. 또한 흐름 제어와 혼잡제어 기능을 이용하여 네트워크의 혼잡을 줄이는 역할을 한다.이렇게 TCP는 데이터의 흐름 관리와 정확성을 확인한다. IP는 패킷을 전달하는 역할로 데이터를 한 장소에서 다른 장소로 정확히 옮겨줌으로서 패킷을 목적지까지 전송하는 역할을 담당한다. 
TCP/IP는 4개의 계층이 존재하는데 이는 프로토콜이 적용되는 특정한 조건이며 효율적으로 통신하고 데이터를 전송할 수 있게 한다. 첫번째는 응용 계층이다. 응용 계층은 사용자가 네트워크에 접근할 수 있도록 하며, SMPT HTTP FTP DHCP SNMP등이 존재한다. 두번째는 전송계층이며 전송을 담당하는 계층이다. 여기에는 TCP, UDP가 있다. 세번째는 인터넷 계층 네트워크 간 데이터 패킷 전송을 관리하며 ip 뿐만 아니라 ARP, IGMP, ICMP가 있다. 네번째는 데이터 링크 계층으로 네트워크 인터페이스 계층이라고도 부르며 데이터가 원하는 IP주소에 도달할 뿐만 아니라 해당 네트워크 내의 연결된 기기에 연결되어 있는지 확인한다.
# 14
TCP는 End-to-End를 보장한다. IP는 라우팅 과정을 통해 최적의 경로를 찾아 패킷을 전송하고, TCP는 ACK라는 긍정 응답 또는  NACK라는 부정 응답을 통해 목적지로 설정한 노드에 데이터가 제대로 도착했음/하지 않았음을 알려준다. 제시간에 도착하지 않으면(Timeout) 재전송을 하고(Retransmission), 순서가 제대로 맞추어지지 않은 패킷들이 있을 경우 sequence number대로 재배치한다. Duplicated packet이 있을 경우 그 또한 처리하며, 이러한 데이터 송신 및 수신 과정을 인터넷에 연결된 컴퓨터에서 실행되는 프로그램 사이에서(출처: 위키백과) 진행함으로써 reliable communication 기능을 수행한다.
# 15
tcp/ip는 신뢰성있는 통신을 가능하게 하기 위해 사용하는 방법 중 하나는 3-way handshake 이다. 이 방법은 클라이언트와 서버 사이에서 통신을 시작할 때 사용되는데 클라이언트가 서버에게 연결을 요청하면 서버가 확인 메세지를 보내고 클라이언트가 다시 확인메세지를 보내야 연결이 확립된다. 이 방법에서는 양쪽이 확인 메세지를 보내기 전에는 연결을 변경시키지 않아 신뢰성 있는 통신을 가능하게 한다.
# 16
IP는 데이터를 수신지에 전달하여 데이터를 분할하고 재조립하는 기능을 한다. 또한 큰 데이터를 여러 개의 작은 패킷으로 분할하여 전송할 수 있다. IP는 데이터의 신뢰성을 보장하지 않는다는 단점을 가지고 있어 TCP가 이를 보완해준다. TCP는 IP 프로토콜 위에서 동작하여 데이터의 신뢰성을 보장하는 역할을 한다. TCP는 다음 4가지 순서를 통해 reliable communication을 가능하게 한다. 먼저 ‘연결 설정과 해제’에서TCP는 연결 설정과 해제를 통해 데이터 전송의 신뢰성을 보장한다. 두번째로 ‘순서 제어’에서 TCP는 데이터의 순서를 제어하여 전송된 데이터의 순서를 보장한다. 세번째로 ‘데이터 전송 확인’에서 TCP는 데이터의 전송을 확인하고 손실된 데이터를 재전송한다. 마지막으로 ‘윈도우 제어’에서 TCP는 수신자의 상태에 따라 데이터의 전송 속도를 조절한다. 이를 통해 데이터의 신뢰성을 보장하고 손실된 데이터를 재전송하여 reliable communication을 가능하게 한다.
# 17
IP를 사용해서 데이터를 전송해 출발지에서 도착지까지 가도록한다. 이때 IP는 말그대로 전달만 할 뿐 제대로 도착했는가에 대한 책임을 지지는 않는다. 이떄 TCP를 사용해 정확도를 높인다. 보낸 데이터가 잘 갔는지 확인하고 알려주는 가능을 하는 것이 TCP이다. ACK나 NACK, Timeout and retransmission 등과 같은 정보를 알려줌으로서 단순히 데이터를 보내고 방치하는 것이 아니라 데이터가 온것에 대해 믿음을 줄 수 있는 reliable communication이 가능해지는 것이다.
# 18
TCP와 IP가 신뢰할 수 있는 통신이 가능한 이유는 네트워크를 통한 통신 과정에서 데이터가 손실되거나 변형되지 않도록 보장해주기 때문이다.
1. TCP는 데이터를 작은 블럭(패킷)으로 분할해서 IP로 전송하기 때문에 데이터의 크기가 커도 지연이나 손실이 발생할 가능성이 적다.
2. TCP는 데이터에 순서 번호를 붙여서 IP로 전송한다. 데이터를 받는 쪽에서는 그 번호를 확인하여 데이터의 순서를 보장할 수 있기 때문에 데이터가 변형되지 않는다.
3. TCP는 데이터 패킷을 전송한 이후 일정 시간 안에 받는 쪽에서 응답이 없으면 그 패킷을 재전송한다. 이를 통해 전송 과정에서 데이터가 손실되어도 다시 전송하여 보완할 수 있다.
4. TCP는 데이터를 전송하는 속도를 제어하여 받는 쪽의 처리 능력을 초과하지 않도록 한다. 이를 통해 받는 쪽에서 데이터를 완전하게 처리할 수 있다.
5. TCP는 전송 중에 발생한 에러를 검출하여 복구할 수 있는 기능이 있다. 이를 통해 데이터를 완전하게 주고받을 수 있다.
# 19
일부 선이 끊어지더라도 다시 연결할 수 있도록 다중망을 이용하고 데이터를 잘게 잘라서 보내고 목적지에서 점검을 하고 순서대로 배열하는 패킷통신을 사용하고 이는 4계층으로 나뉩니다.
우선 응용 계층에서는 네트워크 메시지를 지원하고 담당해서 얻은 데이터를 전송계층으로 보냅니다.
전송계층은 프로세스 간의 통신을 담당하고 전송 과정에서 발생하는 오류를 제어하는 계층으로, 데이터가 전송되는 도중  손실 되는 데이터를 방지하기 위해 각각 포트번호를 덧붙여서 네트워크계층으로 내려 보냅니다. 
네트워크 계층은 목적지까지 전체적인 전송 경로를 계획 계층으로 상대방의 'IP주소'를 덧붙이고 전송 경로를 계획해놓습니다. 이후, 다시 나눠서 데이터 링크 계층으로 내려보냅니다.
데이터 링크 계층에서는 IP주소만 가지고는 실제로 데이터를 전송할 링크를 파악할 수 없고, 파악하려면 'MAC주소'가 필요한데, IP주소를 가지고 MAC주소를 알아내는 프로토콜을 통해 프레임 단위로 묶은 후 물리계층으로 내려보냅니다.
물리계층은 한 프레임씩 링크를 통해 상대방에게 전달하는 방식으로 TCP/IP 계층이 이루어집니다.
# 20
1. IP는 node간의 데이터 패킷을 전송하기 위한 주소를 의미한다. 주소번호를 사용하여 각각의 node를 구분하고, 목적지를 찾아가게 한다.
2. IP가 데이터 패킷을 전송하기 위한 주소라면, TCP는 IP 프로토콜 위에 존재하는 프로토콜으로, 데이터 패킷을 reliable communication 하게 하는 핵심이다.
3. 서버와 클라이언트간에 데이터를 전송하기 전에 데이터는 패킷으로 만들어진 후 네트워크를 통해 전달된다.
4. 이 과정에서 패킷의 순서가 뒤섞이거나 일부가 누락 되는 손실이 발생할 수 있는데, 이때 TCP의 기능이 안정적인 데이터 전송을 지원한다.
5. 먼저, 패킷의 순서가 뒤섞이는 것을 방지하기 위해 TCP는 패킷에 일련번호를 줌으로써 안정적으로 순서를 재조합할 수 있도록 해준다. 둘째로, 패킷 일부가 누락되는 손실을 방지하기 위해서 TCP는 패킷이 빠졌을 경우 재전송을 요청할 수 있다.
6. 이처럼 IP 프로토콜의 기능을 통해 주소번호로 node를 구별하여 클라이언트의 node로 정확하게 전달, TCP 프로토콜의 기능을 통해 패킷을 안정적으로 원하는 지점에 전달할 수 있게 되는 것이다. 결과적으로 reliable communication이 가능하게 된다.
# 21
IP는 기기간 네트워크 사이에서 데이터를 작은 패킷 형태로 쪼개서 보내는데 사용하지만 목적지에 정확하게 도착했는지 알 수 없다. 반면에 TCP는 네트워크가 순서대로 잘 전달됐는지 데이터를 보내준다. 만약 송신 과정에서 데이터가 유실되었다면 TCP가 자동적으로 전달에 성공할 때까지 재송신한다. 따라서 IP가 데이터를 작은 패킷 형태로 쪼개고 패킷에 주소를 지정하여 최적의 경로를 사용하여 네트워크를 통해 전달하는 기능과 TCP가 패킷이 정확히 전달되었는지를 알려주는 기능이 함께 작동함으로써 reliable communiction이 구현된다.
# 22
한 클라이언트에서 발생한 데이터가 상대방 컴퓨터 혹은 서버로 전달되기 위해서는 표준화 된 어떠한 약속 혹은 절차를 따라야 한다. 보내는 쪽에서는 데이터를 안전하고 정확하고 신속하게 규격화, 즉 포장하는 방법이 필요하고, 받는 쪽에서는 그 데이터를 안전하고 정확하고 신속하게 해석하는 방법이 필요한 것이다. 그런 기술적 약속을 포로토콜이라고 한다. TCP는 전송 제어 프로토콜 (Transmission Control Protocol)의 약자이며 한 기기에서 다른 기기로 데이터 전송하는 것을 담당한다. IP는 인터넷 프로토콜(Internet Protocol)의 약자이며 이 프로토콜은 데이터의 조각을 최대한 빨리 대상 IP 주소로 보내는 역할을 표시한다.
# 23
TCP/IP는 클라이언트와 서버를 연결하고 데이터 패킷을 목적지까지 전달한다.  IP는 인터넷 상에서 패킷을 전달,  TCP는 패킷이 잘 도착했는지 확인하고 그렇지 않을 시에는 재전송한다. 또한 보내는 순서, 속도 등을 제어해서 목적지에 데이터가 효과적으로 갈 수 있게 한다. 이러한 방법을 통해 TCP/IP는 reliable communication을 이룬다.
# 24
Connection-oriented : TCP는 통신을 시작하기 전에 두 개의 단말 사이에 연결을 설정합니다. 이를 통해 통신의 시작과 종료를 명확하게 구분하며, 데이터의 신뢰성을 높입니다.
Packet acknowledgment : TCP는 데이터를 작은 패킷으로 나누어 전송합니다. 수신자는 패킷을 받으면 확인 ACK을 보내 송신자에게 패킷이 제대로 도착했음을 알립니다. 만약 ACK를 받지 못하면 송신자는 해당 패킷을 다시 전송합니다.
Sequence control : TCP는 각각의 패킷에 일련번호를 부여하여 순서를 관리합니다. 수신자는 패킷을 받은 순서대로 재조립하여 원래의 데이터를 복원합니다.
Flow control : 수신자가 송신자에 비해 처리 속도가 느릴 경우 데이터의 빠른 전송으로 인해 수신자가 넘치게 될 수 있습니다. TCP는 수신자로부터의 윈도우 크기정보를 이용하여 데이터의 전송 속도를 조절하여 데이터의 오버플로우를 방지합니다.
Retransmission : 패킷이 손실되거나 손상되었을 경우, 수신자는 재전송 요청을 보내거나 손상된 패킷을 버림으로써 정확한 데이터의 전송을 보장합니다.

IP는 인터넷상에서 패킷을 라우팅하는 역할을 담당하며, 패킷의 출발지와 목적지를 지정합니다. TCP와 함께 IP는 데이터의 신뢰성과 안정성을 보장하기 위해 협력하여 동작합니다. TCP가 데이터의 신뢰성을 담당하고, IP가 패킷의 라우팅을 담당하여 데이터가 목적지에 정확하게 전달되도록 합니다.
# 25
TCP는 한쪽으로부터 다른 쪽으로의 데이터 전송을 담당하는데, 잘못 배열된 패킷의 순서를 맞추거나 반복되는 패킷을 정리하는 역할을 한다. 만약 timeout된 데이터가 있다면, TCP가 그 패킷의 재송신을 담당한다. IP는 그 사이의 라우팅을 담당한다. 이렇게 TCP와 IP가 결합되고, TCP/IP 4계층의 각 계층에서 데이터를 주고받아 reliable communication 기능을 만들어낸다.
# 26
TCP(Transmission Control Protocol)는 데이터를 작은 블록으로 나눠 전송하는데, 각각의 블록에는 전송되는 순서와 오류 여부를 확인해주는 일련번호와 체크섬이 포함되어 있다. 수신자에게서 데이터 블록이 정확히 수신 되었는지 확인하고자 수신 확인 메시지를 보낸다. 그 과정에서 손실 되거나 손상된 블록이 감지되면 동일한 블럭을 다시 전송한다. 그리곤 네트워크에서 전송되는 순서와 수신자가 받은 순서가 다를 수 있기 때문에, 수신자가 받은 블록을 일련번호 순서대로 재조정한다. 이 모든 과정에서 TCP는 수신자의 대역폭 및 처리 속도에 따라 전송 속도를 조절한다.

IP(Internet Protocol)는 데이터 블록을 안전하게 수신자에게 전달하기 위해 여러 개의 라우터를 통해 전달하는 과정을 수행한다. IP는 다양한 기기와 라우터에 대한 고유한 IP 주소를 사용하여 데이터 블록을 수신자에게 전송하는데, IP 주소는 32비트 또는 128비트 길이의 이진수로 표시된다. 라우터를 사용하여 데이터 블록을 전송할 때, 라우터는 수신자의 IP 주소를 사용하여 다음 라우터로 데이터 블록을 전달한다. 이 과정을 반복하여 데이터 블록이 목적지에 도달할 때까지 라우팅한다. 만약 데이터 블록이 링크의 최대 전송 단위(MTU)보다 큰 경우 데이터 블록을 더 작게 나눈다. 이때 각 더 작게 만들어지는 블록에는 일련번호와 체크섬 값이 포함되어 있다. 또, IP는 각 데이터 블록의 체크섬 값으로 데이터의 무결성을 검사한다. 데이터 블록에 오류가 있으면 IP는 그 블록을 폐기한다. IP는 데이터 블록을 신뢰성 있게 전송하지는 않지만, TCP와 함께 사용될 때 데이터의 신뢰성을 보장하는 데 중요한 역할을 한다.
# 27
TCP와 IP는 인터넷에서 데이터를 전송하기 위한 프로토콜(통신 규약 및 약속)을 의미한다. 
reliable communication이란 데이터 전송 시 데이터의 손실, 중복, 불일치 등의 문제를 해결해 안정적인 데이터 전송을 보장하는 기능을 말한다. 즉, 믿을 수 있는 통신이다. 이를 위해 TCP는 전송 중인 데이터를 일정 크기의 패킷(데이터를 일정한 크기로 자른 단위 / 인터넷에서 정보를 전달하는 단위)으로 분할하여 다음 TCP 계층에서 재조립한다. IP는 Internet Protocol의 준말이다. 인터넷에서 컴퓨터의 위치를 찾아 데이터를 전송하려면 IP를 지켜야 한다. 전 세계의 수많은 컴퓨터들이 서로를 분리하며 인터넷을 하기 위해서 각자에 주소를 부여하는데 이것이 바로 IP 주소이다. IP는 패킷을 올바른 곳으로 전달하는 역할을 한다.
# 28
Tcp와 ip는 인터넷을 구성하는 주요한 프로토콜로, reliable communication(신뢰성 있는 통신)기능을 구현하여 인터넷에서 데이터를 안정적으로 전송하는데 중요한 역할을 한다. 먼저, Tcp 통신에서 신뢰성 있는 통신 기능을 구현하는데 핵심이 되는 것은 sequence number와 ack패킷이다. Tcp에서는 데이터 패킷의 기본단위인 세그먼트에 기준 번호를 부여하고 데이터를 전송한다. 이때의 기준번호를 sequence number라고 부르고, 수신측은 이 번호를 이용하여 중복된 자료는 폐기하고, 순서가 바뀌어서 수신되는 경우 이를 순서대로 재구성할 수 있게 되는 것이다. 이후 ack 패킷을 통해 송신자가 보낸 패킷을 수신자가 받았는지 확인 후 다음 패킷을 보낸다. 만약 ack 패킷을 받지 못했다면 패킷을 재전송하여 오류를 제어한다.  다음으로, ip는 라우팅을 통해 신뢰성 있는 통신 기능을 구현한다. ip 라우팅이란 주어진 ip 패킷을 ip 헤더에 있는 목적지 주소까지 전달하는 것을 말한다.
# 29
TCP와 IP는 각각 transport layer, internet layer에서 사용되는 프로토콜입니다.
Transport layer는 Application layer에서의 요청을 패킷으로 만들어 전송되기 쉽게 만듭니다.
이것이 TCP 패킷입니다.
그 후 인터넷 상에서 원하는 곳으로 패킷이 전송되어지게 하기 위해 Internet layer에서 패킷에 IP를 부여해 IP패킷으로 만듭니다.
라우팅 완료한 패킷은 Physical layer를 거쳐 라우터가 있는 Internet을 통해 수신하는 곳의 Physical layer로 이동하고
수신하는 곳의 Internet layer로 보내져 IP를 확인합니다.
그런 다음 수신하는 곳의 Transport layer에서 수신한 패킷을 재조합하며 흐름과 혼잡함을 제어하여 신뢰성을 확보합니다.
그 뒤 수신하는 곳의 Application layer로 데이터를 보내 양 측의 소통이 이루어집니다.
# 30
IP는 데이터를 패킷 단위로 나누고, 각 패킷에 목적지 주소와 출발지 주소를 할당하여 인터넷을 통해 전송한다. 그러나 IP는 전송 중 패킷이 손실되거나 순서가 바뀌는 등의 문제를 처리하지 않기 때문에, 이러한 문제를 해결하기 위해 TCP는 IP 위에 구현된다.
TCP는 데이터를 세그먼트라는 단위로 나누어 전송하며, 각 세그먼트는 시퀀스 번호와 확인 응답 번호를 포함한다. 시퀀스 번호는 전송된 세그먼트의 순서를 나타내며, 확인 응답 번호는 수신 측에서 이전에 받은 세그먼트의 시퀀스 번호를 보내면서 데이터의 도착 여부를 확인한다. 데이터를 전송할 때, TCP는 각 세그먼트를 전송하고, 수신 측에서는 확인 응답을 보내 전송이 제대로 이루어졌는지 확인하고, 만약 세그먼트가 손실되었다면, 손실된 세그먼트를 재전송한다. 또한, 순서가 바뀐 세그먼트를 재조립하여 올바른 순서로 데이터를 보낸다.
# 31
﻿TCP/IP는 컴퓨터 간의 데이터를 전송하는 데 안정적이고, 순서대로, 에러 없이 통신하기 위해 만들어진 프로토콜이다. TCP/IP가 안정적으로 소통 기능을 구현할 수 있게 하는 작동 원리를 크게 다섯 가지로 나누어 볼 수 있다고 생각한다. 첫 번째로 패킷을 사용한다. 패킷이란 네트워크를 통해 전송하기 쉽도록 자른 데이터의 전송단위이다. 두 번째로 TCP/IP는 ACK(확인 응답 패킷)을 통해서 전송된 패킷이 다른 곳으로 잘 전송이 됐는지 알 수 있게 한다. 세 번째로 데이터가 와야하는데 오지 않을 경우 합의 없이 다시 데이터를 보내는 Timeout and Retransmission을 한다. 네 번째로 각 패킷에 부여된 번호(sequence number)가 순서가 틀리게 올 경우 순서를 올바르게 맞춰주는 Handle Mis-sequenced Packet을 한다. 다섯 번째로 같은 번호가 중복으로 들어 올 경우 중복이 되지 않게 처리하는 Handle Duplicated Packet을 한다. 이렇게 다섯 가지의 방법으로 데이터를 처리해 TCP/IP는 안정적인 소통을 구현하고 있다.
# 32
TCP는 그 특성상 자신이 보낸 데이터에 대해서 상대방이 받았다는 의미의 응답 패킷을 다시 받아야 통신이 정상적으로 이뤄졌다고 생각한다. 
그래서 만약 자신이 보낸 데이터에 대한 응답 패킷을 받지 못하면 패킷이 유실되었다고 판단하고 보냈던 패킷을 다시한번 보낸다. 이것이 timeout and retransmission이다.TCP가 이렇게 reliable communication을 형성할 수 있다.
 '신뢰성 있는' 이라는 표현을 통해 알 수 있는 것처럼 데이터를 주고 받는 두 종단 간에 데이터를 주고 받음이 확실해야 한다. End to End 방식이다.
보낸 쪽에서는 내가 보낸 데이터를 상대방이 받았다는 응답을 보내야만 나머지를 보낼 수 있다.
이를 통해서 TCP를 통해 주고 받은 데이터는 정확한 데이터라고 확신하게 된다.
 이렇게 Tcp와 Ip는 호스트 내 프로세스 상호 간에 신뢰적인 연결 지향성 서비스를 제공해준다. 패킷 손실, 중복, 순서바뀜 등이 없도록 보장해주면 TCP 하위 계층인 IP 계층이 정보를 전달하는 형식의 신뢰성 형성이다.
# 33
TCP와 IP가 함께 작동하여 reliable한 communication을 제공한다. 우선, IP는 인터넷을 통해 장치 간에 데이터 패킷을 라우팅한다. IP가 신뢰할 수 있는 통신을 보장하기 보다는 패킷을 최대한 전달하는 역할을 하는 것이다. 반면, TCP는 한 장치에서 전송된 데이터가 다른 장치에서 올바르게 수신될 수 있도록 하여 통신에 신뢰성을 부여한다. 데이터를 작은 부분으로 나누고 각 부분에 시퀀스 번호를 매겨 데이터를 재구성한다. 전송 중 데이터의 일부가 손실되거나 손상될 경우, 수신 장치는 전송 장치에 누락된 번호를 재전송하도록 요청할 수 있다. TCP는 모든 데이터가 수신됐는지 확인한다. 데이터를 수신했다면 수신됐음을 나타내는 확인 신호를 송신 장치로 다시 보낸다. 수신 확인이 안 됐다면 데이터를 재전송하는 것이다. 또한, TCP는 너무 많은 데이터로 네트워크 과부화가 걸리지 않도록 흐름을 제어할 수 있다. 전송한 데이터의 처리를 부추기거나 전송 속도를 늦추는 것이다. 이러한 TCP와 IP를 통해 데이터가 정확하고 효율적으로 전달될 수 있게 한다.
# 34
TCP IP 레이어에서는 IP가 데이터 패킷을 라우팅하고 TCP가 데이터의 신뢰성을 보장한다.
TCP가 reliable communication 기능을 만들어내기 위해서 송수신 양측에서 데이터 통신을 확인할 수 있는 다양한 메커니즘을 사용한다.

ACK (Acknowledgment): 수신측이 데이터를 정상적으로 받았다는 응답 신호이다. 송신측은 데이터를 보내고 ACK를 기다리며, ACK가 수신되면 다음 데이터를 전송한다. ACK를 통해 송신측은 데이터가 제대로 전달되었는지 확인한다.

NACK (Negative Acknowledgment): 수신측이 데이터가 손실되었음을 알리기 위해 사용한다. 데이터를 받지 못한 경우에 NACK를 송신측에 전송하여 데이터의 재전송을 요청할 수 있지만 송신측에서 Timeout and Retransmission을 하는 경우가 많아 많이 쓰이지는 않는다.

Timeout and Retransmission: 송신측에서는 데이터를 전송한 후 일정 시간 동안 ACK를 기다린다. 시간내에 ACK가 도착하지 않으면 송신측은 데이터의 손실을 가정하고(Timeout) 데이터를 재전송(Retransmission)한다.

Handle Mis-sequenced Packet (sequence number): TCP는 데이터에 일련 번호(sequence number)를 부여하여 데이터의 순서를 지정한다. 수신측은 데이터가 순서대로 도착했는지 확인하고 순서가 맞지 않으면 재정렬한다.

Handle Duplicated Packet: 중복된 패킷이 도착하는 경우, 임의로 중복된 패킷을 제거하고 한 번만 처리한다. TCP는 이를 통해 중복 데이터의 처리를 방지한다.