##### 1. 4계층

(a) 에러 복구

(b) 흐름 제어

(c) 애플리케이션

##### 2. 커넥션

`(1)`

커넥션은 가상 통신로이다.

##### 3. 윈도우 제어

(1) 윈도우 제어(흐름 제어)

(2) 시퀀스 번호

(3) RTT

(4) 확인응답 번호

##### 4. 포트 번호

`(4)`

(1) 포트 번호를 통해 데이터의 송수신 대상 애플리케이션을 결정한다.

(2) 포트와 애플리케이션을 접속하는 기능을 소켓이라고 한다.

(3) 서버 애플리케이션은 사전에 정해진 번호를 사용하는데, 이것을 웰 노운 포트라고 한다.

##### 5. TCP/UDP

(1) `정확성` : TCP는 확인응답을 통해 정확/확실하게 정보를 전달한다. UDP는 그 반대로 아무것도 하지 않는다.

(2) `응답까지 걸리는 시간` : TCP는 오래 걸린다. UDP는 고속이라는 특징이 있다.

(3) `전송 가능한 데이터의 양` : TCP는 오래 걸리기 때문에 같은 시간 내에 보낼 수 있는 데이터의 양이 비교적 적다. UDP는 전송 효율이 높기 때문에 많은 양의 데이터를 보낼 수 있다.

(4) `용도` : TCP는 웹, 메일, 파일 공유 등 데이터를 누락시키고 싶지 않은 서비스에 많이 사용한다. UDP는 동영상 스트리밍 배포 또는 브로드캐스트가 필요한 애플리케이션 등에 사용된다.

##### 6. 네트워크 주소 변환(NAT)

NAT란 클래스리스 어드레싱을 통해 사설 IP주소를 글로벌 IP 주소로 변환하는 것이다. NAT는 인터넷에 접속하는 컴퓨터가 너무 많기 때문에 글로벌 IP주소가 부족해 사용된다. 단점은 보유하는 글로벌 IP 주소 수 이상의 호스트는 인터넷에 동시에 접속할 수 없다는 것이다.

##### 7. NAPT

`(3)`

정적 NAPT를 사용한다.

##### 8. 5계층

(a) 세션

(b) 다이얼로그 제어

##### 9. 6, 7계층

`(4)`

(1) 6계층은 표현계층이라고도 하며, 하드웨어와 OS에 따른 차이를 없애는 역할을 한다.

(2) 6계층에서는 압축이나 암호화 등의 작업도 수행이 가능하다.

(3) 7계층은 애플리케이션의 목적에 따라 네트워크 서비스를 제공한다.

##### 10. OSI 참조 모델

(a) 신호

(b) CSMA/CD

(c) 어드레싱

(d) 라우팅

(e) 세션

(f) 변환


