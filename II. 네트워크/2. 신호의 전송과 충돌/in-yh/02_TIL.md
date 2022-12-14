#### 제11회  1계층의 역할과 개요

* 1계층의 역할 : ''케이블''(파이프)이 연결되어 있는 기기에 ''신호''(데이터)를 전달하는 것(몇 가지 규격과 규칙 정해져 있음)

  cf) 2계층 이상 : 데이터를 보내기 전에 어떤 것을 할지, 데이터가 도달한 뒤에 어떤 것을 할지

* 케이블(통신 매체)의 종류

  * 유선

    * 동선 : 전기신호 사용, UTP (일반적)

      cf) UTP : 두 개가 한 쌍인 동선 네 쌍으로 이루어짐, 일반적으로 LAN에서 사용되는 케이블(굽히기 쉬운 편이라 좁은 곳에 배선하기 수월)

    * 광파이버 : 광신호 사용, 신호의 안정과 통신속도에서는 뛰어나지만 굽히기 어려움

  * 무선

* 네트워크에 사용되는 기기 : 케이블, 신호, 인터페이스

  * 인터페이스 
    * 케이블에 신호를 보내고 받는 기계, 컴퓨터와 케이블의 중개역(신호를 케이블로 보내고 전달된 신호를 받는 역할)
    * 컴퓨터가 보내고 싶은 데이터를 케이블에 맞는 신호로 변환해서 케이블로 보내고, 케이블에서 보내온 신호를 컴퓨터에서 사용하는 데이터로 변환하는 기계
    * 컴퓨터에서 사용되는 인터페이스로는 LAN용 케이블에 접속하기 위한 'NIC'가 일반적
    * PC에 대부분 NIC 부착되어 있음
  * DCE
    * WAN은 NIC를 부착하지 않고, DCE(회선종단기기)라는 신호 변환기를 사용 (PC의 인터페이스에서 DCE로 신호를 보내면 DCE가 WAN의 케이블에 맞는 신호로 다시 변환)

<hr>

#### 제12회  신호와 충돌

* 데이터 : 컴퓨터상에서의 리소스를 공유하기 위한 정보, 비트로 표현
* 인터페이스 : 비트를 신호로, 신호를 비트로 변환하는 기기
* 신호
  * 종류
    * 아날로그 신호 : 파장, 연속적
    * 디지털 신호 : ON&OFF, 비연속적, 압도적으로 많음(0과 1로 되어 있는 비트는 표현하기 쉬운 디지털 신호로 사용)
  * 통신속도 : 신호의 형태와 전송방법에 따라 통신속도 결정
    * bps : 1초 동안 전해지는 비트 수
    * 통신속도(bps) = 1초 동안의 신호의 횟수 * 1회 신호의 비트수(신호 한 번으로 1비트, 2비트...)
  * 문제 (3가지)
    * 감쇠
      1. 원인 : 긴 케이블을 지나는 동안 신호 약해짐 
      2. 해결 : 증폭이라는 처리를 하는 기계 설치 필요
    * 노이즈·간섭
      1. 원인 : 근처에 고온 물체가 있다거나(열 잡음), 신호를 보내는 또 다른 케이블이 있다거나(크로스 토크 : 신호 누설), 번개나 무선 등 전자파가 발생하는 물체가 있다거나.. 등
      2. 해결 : 케이블에 특수 가공을 해서 신호 망가지는 것을 방지(케이블에 ''실드'' 처리), 광파이버 사용(광신호(빛)는 이런 전기적인 요인에 영향 없음)
    * 충돌
      1. 원인 : 멀티액세스 네트워크(허브 연결) 등에서 발생, 신호가 보내지고 있는 도중에 다른 신호를 보내는 경우에 발생
      2. 해결 : 신호를 보내는 타이밍을 서로 엇갈리게 하는 방법, 신호가 지나는 길을 나누는 방법(2계층 관련)

<hr>

#### 제13회  허브

* 허브에 케이블로 연결되어 있는 기기는 동일 케이블에 연결되어 있는 것하고 같은 취급을 받는다.

* 포트 : 허브의 케이블 삽입구, 개수는 4, 6, 8, 16, 32 등이 있다.

* 기능

  * 신호의 증폭과 재생, 감쇠에 의해 붕괴된 신호를 본래의 형태로 증폭·재생

    cf) 리피터 : 증폭만 하는 기계, 허브처럼 케이블을 많이 연결할 수는 없음

  * 복수의 기기를 연결해서 네트워크를 구축하는 기능, 허브에 연결되어 있는 기기끼리 신호 주고 받을 수 있음

    cf) 연속접속 가능 : 허브와 허브를 연결하는 접속으로 신호가 도달하는 범위를 넓힐 수 있다.

* 문제점

  * 허브는 수신한 신호에 대해 어떤 제어도 하지 않는다(증폭, 재생 제외)
  * 플러딩 : 허브는 수신한 포트 이외의 모든 포트에 수신한 신호를 송신함 => 충돌 가능성 UP
  * 충돌 도메인 : 충돌이 발생할지도 모르는 범위, 허브로 연결되어 있는 컴퓨터는 같은 충돌 도메인에 있게 됨
  * 충돌 도메인은 작아야만 한다. 그러나 반드시 다수의 컴퓨터가 필요한 경우도 있는데.. => "스위치" 필요!

<hr>

#### 제14회  2계층의 역할과 개요


* 충돌을 막기 위해서는 ''송신하는 타이밍을 엇갈리게 하는 방법''을 생각해야 하는데 이것은 ''신호를 보내기 전'' 얘기 / ''신호가 도달한 후''에도 생각해야 할 것이 있음 => ''신호의 송신 전이나 수신 후에 바르게 데이터를 송수신하는 순서'' 필요
* 데이터를 보내기 전에 어떤 일을 할지, 데이터가 도달한 후에 어떤 일을 할지를 생각해야 함

* 2계층의 역할 : 신호가 닿는 범위에서의 데이터 전송에 관한 규정

  cf) 신호가 닿는 범위 : 멀티액세스 네트워크라면 허브로 연결되어 있는 기기 전체, 포인트 투 포인트 네트워크라면 서로 연결되어 있는 두 대(컴퓨터와 라우터, 라우터와 라우터 사이), 즉, ''세그먼트 범위''에서의 데이터 전송

  cf) 세그먼트를 넘는다는 것은 패킷 교환기인 라우터를 통해서 별도의 세그먼트로 데이터를 보낸다는 의미인데 이건 3계층에서 생각! 

* 1계층에서 다루는 신호랑 케이블 등에 따라 2계층의 규격이 달라짐

  * LAN용 : 실제 현장에서 이 지식이 가장 필요!, LAN의 사실표준인 ''이더넷''이라는 규칙이 있음

  * WAN용

    cf) 3계층 이상의 계층에서는 LAN이나 WAN이나 동일한 규칙을 사용

* 프레이밍

  * 프레이밍 : 1계층에서 주고받는 신호를 비트화해 거기에 의미를 갖게 하는 걸 말함

  * 프레이밍을 시행함으로써 송수신되는 비트열에 의미를 주어 데이터로 취급할 수 있게 함

  * 비트열에 프레임 포맷을 적용시켜 송수신되는 비트에 의미가 생긴다 = 프레임화 한다.(프레이밍)

    cf) 프레임 : 2계층의 PDU

  * 프레이밍에서는 제일 먼저 ''프리엠블''이라고 불리는 '지금부터 프레임이 시작된다는 신호'를 함, 수신측에서는 이 프리엠블을 수신하면 '이제부터 프레임 신호가 오겠군' 판단

    * 비트를 읽는 타이밍이 송신측과 수신측 양쪽에서 일치해야 해, 어긋나면 수신측이 비트 중간에 읽기 시작할지도 모름
    * 동기 통신 : 타이밍을 맞추는 방법으로는 클락 신호라고 부르는 타이밍을 맞추는 신호를 계속해서 보내는 방법이 있다. => 이 방식에서는 프리엠블은 사용하지 않음. 항상 신호를 보내는 수고가 필요하기 때문에 별로 사용하지 않음.
    * 비동기 통신 : 데이터 통신 직전에 프리엠블을 보내 타이밍을 맞추는 방식
    * 패킷 교환 방식에서는 프리엠블 방식이 일반적

<hr>

#### 제15회  2계층 주소와 이더넷

* 이더넷에서 어떻게 '신호가 도달하는 범위에서 데이터를 송수신하는지' 알아보자
  * 주소 : 데이터를 보내는 상대와 자신을 특정하는 데이터, 수신처와 송신처 주소
  * 어드레싱 : 이 주소를 어떻게 사용할지, 어떻게 배정할지
* 데이터 전송 방법(3종류)
  * 유니캐스트 : 1대1
    * 각각의 기기는 유니캐스트 주소를 적어도 한 개 갖고 있다.
    * 라우터처럼 복수의 인터페이스를 가진 기기는 인터페이스마다 유니캐스트 주소를 갖는다.
    * 유니캐스트 주소는 유일해야 함(같은 것이 없다.)
  * 브로드캐스트 : 1대 전체(세그먼트 내의 모든 기기)
  * 멀티캐스트 : 1대 다수(복수의 기기)
* MAC 주소
  * 이더넷에서 사용되는 주소, ''인터페이스에 지정된 고정 주소''
  * 48비트 값으로 4비트마다 16진수로 고쳐 쓴다.(12자리)
  * 선두 24비트는 벤더코드(인터페이스를 제조한 메이커의 번호, 어느 메이커가 만든)
  * 후반 24비트는 벤더 할당 코드(제조한 메이커가 붙인 번호, 몇 번째 인터페이스)

<hr>

#### 제16회  이더넷

* 캡슐화

  * MAC 주소를 사용해서 '누구로부터', '어디로'를 결정하는 건데 이 주소 정보를 헤더에 기술해서 송신하는 것

  * 이더넷 헤더 + 데이터그램 + 이더넷 트레일러 => 이더넷 프레임 (캡슐화) / 이더넷 프레임이 신호가 되어서 케이블로 전달

    cf) 이더넷 프레임 : 이더넷에서 사용하는 2계층 PDU

  * 헤더 : 수신처의 MAC주소, 송신처의 MAC주소, 페이로드(3계층 PDU)의 내용·종류를 식별하는 타입이 붙음
  * 트레일러 : 에러를 체크(FCS), 에러를 고칠 순 없고 에러가 있었던 프레임은 파기됨, 파기했다는 것은 송시측에는 알리지 않는다.

* 이더넷 동작

  * LAN에서는 허브를 사용한 멀티액세스 네트워크를 채용하는 경우가 많은데, 문제점이 플러딩과 충돌 발생이 있었다.
    * 플러딩 방지
      1. 이더넷에서는 수신한 프레임의 수신처 MAC 주소를 보고 자기에게 온 것 외의 다른 프레임은 파기 => 특정 수신처에만 도달하는 것이 아니라 자기가 수신처가 아닌 데이터는 안본다
      2. 허브에 의해 모든 기기에 도달한 프레임은 수신처 MAC 주소를 가진 기기 이외에는 파기한다.
    * 충돌 발생 방지
      1. 이더넷에서는 신호를 보내는 타이밍을 겹치지 않도록 비켜나게함으로써 되도록 충돌이 일어나지 않도록 ''CSMA/CD''라는 엑세스 제어를 시행
      2. 인터페이스에 연결되어 있는 케이블에 신호를 보내는 ''엑세스''를 ''제어''하는 것을 의미
      3. CS(신호 감지)는 누군가가 송신 중이라면 송신하지 않는다.
      4. MA(다중 액세스)는 아무도 송신하고 있지 않다면 송신할 수 있다.
      5. CD(충돌검사)는 송신 후에 충돌이 일어나면 다시 재수행한다.

<hr>

#### 제17회  스위치

* CSMA/CD는 충돌을 아예 막는 건 아님

* 충돌이 발생하지 않도록 하기 위해서는 1. 신호를 보내는 타이밍이 겹치지 않도록 엇갈리게 하는 방법 2. 신호가 지나는 길을 나누는 방법

* ''신호가 지나는 길을 나누기'' 위한 기기 : 스위치 (허브 대신 사용)

  cf) 복수의 포트를 갖고 있어 복수의 컴퓨터 연결 가능

* 어디에서 충돌이 일어나고 있는지가 포인트! LAN에서 사용되고 있는 UTP나 광파이버 케이블은 송신 신호, 수신 신호가 나뉘어 있다. 다시 말해, 케이블상에서는 충돌 발생하지 않는다.

* 충돌은 허브에서 발생!! 허브가 동시에 2개 이상의 기기로부터 신호를 수신하면 허브는 그것을 나누어서 보낼 수 없음 => 여기서 충돌 발생!!

* 스위치 안에서 수신한 프레임을 따로따로 보낼 수 있도록 처리해서 충돌을 막는 것!

  * MAC 주소 필터링 : 수신처가 ''다른'' 프레임이 동시에 스위치에 도달해도 충돌 일으키지 않게 함

    * 학습 

      1. 수신한 프레임의 송신처(보내는) MAC 주소와 ''수신한'' 포트의 대응을 ''학습''한다.(송신 주소를 받아보며 지금 이 포트에는 이 주소랑 연결되어 있어요! 또 다른 송신 주소를 받아보며 여기 포트는 이 주소네요! 이러면서 어드레스 테이블 만듦) => 학습 전이라면 허브와 같이 플러딩 하게 됨

      2. 스위치는 포트에 연결되어 있는 컴퓨터의 MAC 주소를 기억(이 포트에 이 MAC 주소를 가진 컴퓨터가 있습니다.)

         cf) 이 대응표를 ''어드레스 테이블''이라고 한다.

    * 스위칭

      1. 프레임을 수신한 스위치는 프레임의 수신처 MAC 주소를 보고 그 MAC 주소가 있는 포트를 찾아내 그 포트로부터만 프레임을 송신(위에서 학습한 어떤 포트에 어떤 주소가 있는지 알기 때문에 수신 주소가 들어오면 그 포트를 찾아내어 거기서만 송신 때림) => 송신하는 포트를 필터링 하기 때문에 'MAC 주소 필터링'이라고 함
      2. 수신처가 다른 프레임이 동시에 스위치에 도달해도 충돌은 발생하지 않게 됨

  * 버퍼링 : 수신처가 ''같은'' 프레임이 동시에 도달한 경우

<hr>

#### 제18회  전이중 이더넷

* 버퍼링 : 수신처가 ''같은'' 프레임의 충돌을 막는다.

  cf) 버퍼 : 일시적으로 데이터를 기록해 둘 수 있는 기억기기(메모리)

* 충돌할 것 같은 프레임을 버퍼에 일시적으로 저장해 두는 것!, 한 개는 송신하고 다른 한 개는 일시적으로 버퍼에 저장 & 첫 번째 프레임 송신이 끝나면 저장해 두었던 프레임을 송신시킴

* 버퍼의 용량이 부족하다고 판단되면 송신 중지

  * 백 프레셔 : 반이중, 충돌을 전하는 신호에 의해 송신 중단
  * IEEE802.3x : 스위치가 전이중 이더넷에 대응하면, PAUSE 프레임에 의해 송신 중단

* 충돌 도메인은 스위치에 의해 분할, 충돌 도메인은 작아야 하는데 스위치가 이것을 실현해서 데이터 통신의 효율을 높이는 것이다.

* 전이중 이더넷

  * 반이중 통신 : 누군가가 송신 중(자기는 수신 중)일 때는 송신 불가능, 자기가 송신 중일 때는 수신 불가능

    ex) CSMA/CD, 허브를 사용한 이더넷

  * 전이중 통신 : 동시에 송신과 수신을 할 수 있는 방식, 스위치를 사용한 경우에는 ''충돌을 염려할 필요가 없으므로'' CSMA/CD를 사용할 필요 없음, 전이중 통신을 할 수 있음, 스위치를 사용해 전이중 통신을 하는 것을 ''전이중 이더넷''이라고 함.

    ex) 스위치를 사용한 이더넷
