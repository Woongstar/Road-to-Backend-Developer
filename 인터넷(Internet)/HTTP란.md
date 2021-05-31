# HTTP란?

### 추천 사이트

- [생활코딩 HTTP](https://opentutorials.org/course/3385,"생활코딩")
- [위키피디아 HTTP](https://ko.wikipedia.org/wiki/HTTP,"위키피디아")

- [SeoYng님블로그](https://velog.io/@tjdud0123/HTTP-%EC%A0%95%EB%A6%AC)
- [MDNHTTP](https://developer.mozilla.org/ko/docs/Web/HTTP/Messages)



## HTTP

- Hyper Text Transfer  Protocol의 약자
- 웹서버와 웹브라우저간의 통신규약을 의미한다.



## HTTP 특징

- HTTP 클라이언트와 HTTP 서버에 의해서 해석이 된다.
- TCP/IP를 이용하는 응용 프로토콜(application protocol)
- HTTP는 연결 상태를 유지하지 않는 비연결성 프로토콜입니다. -> Cookie 와 Session 
- 요청/응답(request/response) 방식으로 동작

<img src="./img/http요청.png">

클라이언트(client) 즉, 사용자가 브라우저를 통해서 어떠한 서비스를 url을 통하거나 다른 것을 통해서 요청(request)을 하면 서버에서는 해당 요청사항에 맞는 결과를 찾아서 사용자에게 응답(response)하는 형태로 동작합니다.

- 요청 : client -> server
- 응답 : server -> client

<img src="./img/http네트워크.png">

```http
:authority: ko.wikipedia.org
:method: GET
:path: /wiki/HTTP
:scheme: https
accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
accept-encoding: gzip, deflate, br
accept-language: ko-KR,ko;q=0.9,en;q=0.8
cache-control: max-age=0
cookie: GeoIP=KR:49:Jeju_City:33.45:126.54:v4; kowikimwuser-sessionId=63fba94fec2c7a7178f8; WMF-Last-Access=31-May-2021; WMF-Last-Access-Global=31-May-2021; kowikiel-sessionId=4823e9321a30f9441330; kowikiwmE-sessionTickLastTickTime=1622431527885; kowikiwmE-sessionTickTickCount=10
referer: https://www.google.com/
sec-ch-ua: " Not A;Brand";v="99", "Chromium";v="90", "Google Chrome";v="90"
sec-ch-ua-mobile: ?0
sec-fetch-dest: document
sec-fetch-mode: navigate
sec-fetch-site: cross-site
sec-fetch-user: ?1
upgrade-insecure-requests: 1
# HTTP 위키피디아 Request 예시
```



**웹페이지에서 F12를 눌러 Network창에서 새로고침을 누르면 현재 HTTP의 Response와 Request등을 볼 수 있다.**



HTTP 메시지는 서버와 클라이언트 간에 데이터가 교환되는 방식입니다. 메시지 타입은 두 가지가 있습니다. 요청(*request)은* 클라이언트가 서버로 전달해서 서버의 액션이 일어나게끔 하는 메시지고, 응답(*response)은 요청*에 대한 서버의 답변입니다.

HTTP 메시지는 ASCII로 인코딩된 텍스트 정보이며 여러 줄로 되어 있습니다. Activity initiation 에서의 사람이 읽을 수 있는 정보들은 HTTP/1 메시지를 통해  ASCII로 인코딩된 텍스트 정보로 만들어 Binary framing을 진행합니다. Binary framing은 HTTP/2에서의 최적화와 성능 향상을 위해 여러 HTTP 프레임으로 나눠서 조합하는 것입니다.

웹 개발자가 손수 HTTP 메시지를 텍스트로 작성하지는 않고,  소프트웨어, 브라우저, 프록시, 또는 웹 서버를 통해 HTTP Request와 Response를 진행합니다.

<img src="./img/httprequest.png">



1. 시작 줄(start-line)에는 실행되어야 할 요청, 또은 요청 수행에 대한 성공 또는 실패가 기록되어 있습니다. 이 줄은 항상 한 줄로 끝납니다.
2. 옵션으로 HTTP 헤더 세트가 들어갑니다. 여기에는 요청에 대한 설명, 혹은 메시지 본문에 대한 설명이 들어갑니다.
3. 요청에 대한 모든 메타 정보가 전송되었음을 알리는 빈 줄(blank line)이 삽입됩니다.
4. 요청과 관련된 내용(HTML 폼 콘텐츠 등)이 옵션으로 들어가거나, 응답과 관련된 문서(document)가 들어갑니다. 본문의 존재 유무 및 크기는 첫 줄과 HTTP 헤더에 명시됩니다.

**HTTP 메시지의 시작 줄과 HTTP 헤더를 묶어서 요청 *헤드(head)라고 부르며*, 이와 반대로 HTTP 메시지의 페이로드는 *본문(body)*이라고 합니다.**

<img src="./img/reqres.png">

### HTTP Request

<img src="./img/requestheader.png">

