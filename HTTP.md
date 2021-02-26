##HTTP

:"HyperText Transfer Protocol"

#####- HyperText

:텍스트를 HyperText로 전환해서 네트워크상에서 송신가능하게 한다.
(www.google.com는 http없이는 그냥 텍스트일 뿐)

#####- Transfer Protocol

:'어떻게' 서버로 송신/수신 할 것인가?

#####- HTTP 구성

1. Start line(필수)

: 서버의 프로그램을 start시킨다.

- 서버측 url 도메인 이하의 params (ex: /search?q=tuna)
- http 버전정보, method(get,post,put,delete) // request
- http 버전정보, method, status(200, 404, 500등) // response

2. Headers

: 추가 정보들 담고있음 - 각 라인이 header임.

// request (위키피디아에 http header검색하면 request, response 필드 정보나옴)

- host(서버측 url도메인 www.google.com등), token
- Accept language : "정보 보낼때 어떤 언어로 보낼지에 대한것
  : application(타입)/javascript(서브타입)
- Authorization: 인증관련 credential
- Cache control
- Content Type: 프로그램에 송신하는 콘텐츠 타입 정의(xml인지, json인지 등)
- Date(보내는 날짜)

// response

- cookies(보내는 파일이 얼마나 큰지, 뭘 보내는지 등등 원하는 만큼 cookie보낼 수 있음)
- Cache-control(캐쉬 만료기한 등 캐쉬정보)
- Date(보내는 날짜)
- Expires(응답이 보내지고 난 후, 캐쉬가 만료되고 first version으로 리프레쉬 되는 기한)
- Server(서버 이름)

3. Blank line

: header와 body구분해주는 빈 라인.

4. Body

:post관련 데이터를 실어서 전송하는 곳(post request),
response data가 실려오는 곳(response)

- header에 명시된 content type 데이터를 주고받음

#####Idempotence(safe to repeat?)

GET(O), POST(X), PUT(O), DELETE(O)
