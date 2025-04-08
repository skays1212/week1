- **웹**은 여러 컴퓨터가 서로 연결되어 정보를 공유하는 공간으로서 웹에서 컴퓨터가 서로 정보를 주고 받는 일반적인 형태는 **클라이언트-서버 패러다임**이다.

- **클라이언트**는 데이터의 생성/조회/수정/삭제 요청을 전송하고, **서버**는 요청대로 동작을 수행하고 응답을 전송한다.

- **프로토콜** : 네트워크 안에서 요청과 응답을 보내는 규칙

- 웹에서는 **HTTP**라는 프로토콜을 사용한다.

- HTTP으로 요청을 보낼 땐, **HTTP Method**와 **URL**이 필요하다.

- HTTP Method : 데이터를 다루는 방법(동사) {GET, POST, PUT, ..}

- URL : 다룰 데이터의 위치(목적어) {http://wwww.example.com/user/1/nickname}

### HTTP Method 종류

- GET : 데이터를 가져온다.(조회)

- POST : 데이터를 게시한다.(생성)

- PUT : 데이터를 교체한다. (수정)

- PATCH : 데이터를 수정한다. (수정)

- DELETE : 데이터를 삭제한다. (삭제)

### Path Parameter (URL의 일반화된 표현 방법)

**http://www.example.com/user/{user_id}/nickname**

- http <- 프로토콜(scheme)

- www.example.com <- 서버주소(domain)

- /user/{user_id}/nickname <-서버 내 데이터 위치(path)

path경로안에서 변할 수 있는 값은 {}로 변수명을 감싸준다.

### Query String

.com/post/search?page&keyword=hello

- /post/search <- 데이터 위치(path)

- ?page&keyword=hello <- Query String

path뒤에 query string의 시작은 '?'로 시작하며, '='를 기준으로 왼쪽에 있는 것이 key, 오른쪽이 value이며 '&'를 통해 key = value를 나열해준다.

### HTTP로 주고받는 데이터의 구조
- HTTP 헤더 -> 통신에 대한 정보 (언제, 누가 보냈는지, HTTP method 종류, 요청 경로 등)
- HTTP 바디 -> 주고 받으려는 데이터(json 형식)

### HTTP 상태 코드
- 200 -> 처리 성공
- 201 -> 데이터 생성 성공
- 400 -> 클라이언트 요청 오류
- 404 -> 요청 데이터 없음
- 500 -> 서버 에러

### 프론트엔드와 백엔드
**프론트**는 화면에 채울 컨텐츠 데이터를 백엔드에게 요청.
**백엔드**는 DB에서 가져온 컨텐츠 데이터를 프론트에게 응답.

### API
- 어플리케이션에서 원하는 기능을 수행하기 위해 어플리케이션과 소통하는 방법을 정의한 것.

### 백엔드 API
- 프론트가 백엔드에 요청을 보낼 때 어떤 http method, url을 사용해야 하는지 정의한 것.
- 각 요청에 대해 어떤 응답을 보내는지 정의한 것.

### REST API
- REST 아키텍처를 따르도록 설계한 API
  #### REST API 규칙(큰 틀에서의)
  - URL : 조작할 데이터 (명사)
  - HTTP method : 데이터에 대한 행위 (동사)
 
---
## week1 과제
### 로그인
- 로그인 : POST /login
- 로그아웃 : POST /logout

### 회원가입
- 회원가입 : POST /register

### 좋아요
- 좋아요 : POST /like
  
### 할 일
- 할 일 전체 조회 : GET /todo/list
- 할 일 생성 : POST /todo
- 할 일 수정 : PATCH /todo/{todo_id}
- 할 일 삭제 : DELETE /todo/{todo_id}
- 할 일 체크 : POST /todo/{todo_id}/check
- 할 일 체크해제 : POST /todo/{todo_id}/uncheck

### 친구 기능
- 친구 찾기 : GET /friend/{friend_id}
- 친구 팔로우 : POST /friend/{friend_id}
- 친구 언팔로우 : Delete /friend/{friend_id}
- 나의 친구 리스트 조회 : GET /friend/list
- 특정 친구의 할 일 조회 : GET /friend/{friend_id}/todo/list

---
(https://github.com/skays1212/week1/blob/main/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202025-04-09%20003608.png)

