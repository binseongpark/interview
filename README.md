# 동기와 비동기의 차이
동기는 한 라인이 실행되고 나서 그 다음 라인이 실행되는 방식. 순차적으로 실행되며 이후라인들은 대기 중
비동기는 한 라인이 오래 걸리는 작업일 경우 뒷 라인들이 계속 대기상태로 있음. 앱의 경우 end-user 는 윈도우로 치면 응답없음, 웹페이지로보면 아무 액션도 안먹는 웹페이지가 뜨게 됨. 이런 것들 해결하기 위해 비동기적으로 그 라인의 실행결과를 받게하여 이후 라인들이 밀리지 않게 함

# mixed content
SSL 기반 웹사이트에서 http 기반의 콘텐츠가 발생 할 경우 http 콘텐츠를 차단한다는 경고 메세지

# SSL
Secure Sockets Layer. 암호화 기반 인터넷 보안 프로토콜

# CORS
다른 도메인, 프로토콜, 포트의 자원을 요청핧 때 http 요청을 제한함

# redux, vuex 사용하면서의 장점
개발 시 데이터 흐름을 한곳으로 흐르게 할 수 있어 문제를 찾기가 쉬워지는 듯 함. 데이터를 계속 내려주는 작업도 스트레스인데 상태 관리 라이브러리를 이용하면 그런 불편함을 없앨 수 있음. 

# DNS
domain name system. 호스트의 도메인 이름을 호스트의 네트워크 주소로 바꾸거나 반대로 네트워크 주소를 도메인 네임으로 바꾸는 작업을 수행해주는 데이터베이스 시스템.

# Promise, async/await
## Promise
promise 객체를 then 이나 catch 로 받아서 처리 할 수 있음
## async/await
promise 객체를 await 을 통해 반환값을 받을 수 있고 then 처럼 완료까지 기다려줌. then 같은 체이닝을 할 필요가 없어 코드 가독성이 좋아짐. 에러 핸들링을 받는 catch 같은 것은 따로 없어 try catch 문으로 감싸야 함

# 함수 선언식, 함수 표현식
함수 표현식은 호이스팅 영향을 받지 않음. 함수 선언식은 맨 위로 끌어올려짐. 표현식은 호이스팅이 되지 않아 다른 함수의 인자로 넘긴다던지 클로져로 사용
```js
function tabsHandler(index) {
    return function tabClickEvent(event) {
        // 바깥 함수인 tabsHandler() 의 index 인자를 여기서 접근할 수 있다.
        console.log(index); // 탭을 클릭할 때 마다 해당 탭의 index 값을 표시
    };
}
```

# 이벤트 버블링, 캡처링
## 버블링
위로 전파
## 캡처링
하위 요소로 전파.

# virtual dom 
메모리에 DOM 을 추상화한 객체를 두고 변경사항 발생 시 DOM 을 직접 수정하는게 아니라 virtual dom 을 통해서 달라진 부분 확인 후 변경된 부분만 렌더링 함

# this
자신이 속한 객체 또는 자신이 생성할 인스턴스를 가리키는 자기 참조 변수. arrow function 은 언제나 상위스코프의 this 를 가리킴. 일반함수는 어떻게 호출되는지에 따라 동적으로 결정됨.

# 깊은복사, 얕은복사
깊은복사는 객체의 실제값을 복사하고 얕은복사는 객체의 주소를 복사

# for, forEach
for는 동기, foreach 는 비동기 for를 돌다가 에러가 나면 그 이후 처리는 하지 못함
- forEach
배열에 대해 반복 작업
- for .. in
key 속성을 반복할 때 사용
- for .. of
iterable Object 에 사용. Array, Map, Set, String, TypedArray, arguments