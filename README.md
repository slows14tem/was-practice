# FastCampus 10개 프로젝트로 완성하는 백엔드 웹개발(Java/Spring) 초격차 패키지 Online
## Part1. 나만의 MVC 프레임워크 만들기
### Ch04. 웹 애플리케이션 이해
#### 1. 계산기 프로그램 웹 애플리케이션으로 만들기
- 사용자 요청을 메인 Thread가 순서대로 처리하도록 하는 방법 : 작업을 main thread에서 처리하기 때문에 블럭이 생기면 다음 요청은 해당 요청이 끝날때까지 기다려야 함
- 사용자 요청이 들어올 때마다 thread를 새로 생성해서 사용자요청을 처리하도록 하는 방법 : thread를 생성하면 독립적인 스텍 메모리 영역을 할당 받는데 이 작업이 상당히 비싼 작업이라서 접속자가 많아지면 리소스 사용량이 폭증(서버 다운 가능성 생김)
- thread pool을 적용하는 방법 : 일정한 thread를 미리 만들어두고 재사용하는 개념으로 안정적인 서비스가 가능함
#### 2. HTTP 특징
- 무상태 프로토콜(StateLess): 서버가 클라이언트 상태를 유지하지 않음 (Keep-Alive 속성 사용하여 해결)
- 비 연결성(Connectionless): 서버가 클라이언트 요청에 대한 응답을 마치면 맺었던 연결을 끊어버림 (쿠키, 세션, JWT 등으로 해결)

##### HTTP가 stateless, connectionless인 이유
- http는 웹 상에서불특정 다수와  통신이 가능하도록 설계된 프로토콜이기 때문에 서버가 다수의 클라이언트와 연결을 유지하려면 리소스 낭비가 심해진다. state와 connect를 유지하지 않는 대신 더 많은 연결을 할 수 있도록 하는 것이 가능해 진다.
