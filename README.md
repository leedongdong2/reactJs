# reactJs

 React는 자바스크립트 라이브러리로 SPA(Single Page Application)을 위한 사용자 인터페이스를 구축하는데 사용된다.
 - 웹, 모바일 앱 등의 view layer를 처리하는 데 사용된다.
 - 페이지를 다시 로드하지 않고 데이터를 변경할 수 있도록 가상 돔(Virtual DOM)을 사용하여 웹 애플리케이션의 퍼포먼스를 최적화한 라이브러리이다.

 - 리액트는 컴포넌트 기반의 라이브러리이다.
 - 웹 페이지에서 컴포넌트는 화면을 이루는 작은 요소들이다.
 - 컴포넌트들은 여러 화면에서 사용될 수 있다. 즉 재사용성을 가지고 있다.
 - 컴포넌트의 종류는 클래스형과 함수형으로 나누어진다. 특징은 지금은 다음 정도만 알고 있자.
   1) 클래스형 : 프로퍼티, state와 함수 등을 포함 한다.
   2) 함수형 : state를 포함하지 않으며, 데이터를 받아 출력할 컴포넌트를 반환 한다.

 - 하기 1~5번을 각각 컴포넌트로 볼 수 있다.

 - DOM 업데이트를 추상화 시켜놓은 것 이다.
 - 브라우저에서 html을 열게되면 DOM을 만들게 된다. html코드의 특정 부분이 변경되면 전체 DOM을 새롭게 만들게되어 매우 비효율 적이다.
   이를 개선하기위해 리액트는 가상 DOM을 만들어 진짜 DOM과 비교한다. 그리고 변경된 부분만 진짜 DOM에 반영하는 방식으로 작업을 수행한다.
 - in-memory에 존재해서 실제 렌더되지 않는다.
 - Vue나 React에서 사용한다.

1.리액트 컴포넌트란!

 리액트로 만들어진 앱을 이루는 최소한의 단위

 - 기존의 웹 프레임워크는 MVC방식으로 분리하여 관리하여 각 요소의 의존성이 높아 재활용이 어렵다는 단점이 있었다. 반면 컴포넌트는 MVC의 뷰를 독립적으로 구성하여 재사용을 할 수 있고 이를 통해 새로운 컴포넌트를 쉽게 만들 수 있다.
 - 컴포넌트는 데이터(props)를 입력받아 View(state) 상태에 따라 DOM Node를 출력하는 함수.
 - 컴포넌트 이름은 항상 대문자!!로 시작하도록 한다. 
   (리액트는 소문자로 시작하는 컴포넌트를 DOM 태그로 취급하기 때문이다.

 - UI를 재사용 가능한 개별적인 여러 조각으로 나누고, 각 조각을 개별적으로 나누어 코딩한다.


<img width="414" alt="임포트" src="https://github.com/leedongdong2/springBootTest/assets/77323959/fd834d8d-dcda-4507-a136-a44f30195bb7">
<img width="194" alt="컴포넌트" src="https://github.com/leedongdong2/springBootTest/assets/77323959/bcd2ca2f-4a37-447e-8425-1cbd609dd0e0">
<br>
각각의 컴포넌트를 만들어 결합하여 화면을 구성한다.
<br>

2.프로퍼티란!
 - 프로퍼티, props(properties의 줄임말) 라고 한다.
 - 상위 컴포넌트가 하위 컴포넌트에 값을 전달할때 사용한다.(단방향 데이터 흐름 갖는다.)
 - 프로퍼티는 수정할 수 없다는 특징이 있다.(자식입장에선 읽기 전용인 데이터이다.)
 - 프로퍼티에 문자열을 전달할 때는 큰따옴표(" ")를, 문자열 외의 값을 전달할 때는 중괄호({ })를 사용 한다. 
<br>
<img width="235" alt="prop" src="https://github.com/leedongdong2/springBootTest/assets/77323959/c8276a04-1d4a-4134-83e4-52ce4389dd66">
<img width="206" alt="prop2" src="https://github.com/leedongdong2/springBootTest/assets/77323959/a3dc1d1c-d5c0-485d-9d30-fe74aca8789e">
<img width="78" alt="prop3" src="https://github.com/leedongdong2/springBootTest/assets/77323959/f62a5f73-7e4d-498c-941e-2f22eee2aa77">

 - 다수의 프로퍼티를 넘기는것도 가능하고 비구조화 할당도 가능하다
<img width="265" alt="prop4" src="https://github.com/leedongdong2/springBootTest/assets/77323959/495e83be-ab25-47ec-b9ab-3c2b60a1a685">
<img width="223" alt="prop5" src="https://github.com/leedongdong2/springBootTest/assets/77323959/e40b18af-3f85-4363-af69-d6da2e96be95">
<img width="93" alt="prop6" src="https://github.com/leedongdong2/springBootTest/assets/77323959/693adf50-76b2-43ac-9553-1589607bda70">

3.state란!

 - 일반적으로 컴포넌트의 내부에서 변경 가능한 데이터를 관리해야할 때에 사용 한다. 
 - 프로퍼티(props)의 특징은 컴포넌트 내부에서 값을 바꿀 수 없다는 것이었다.
   하지만 값을 바꿔야 하는 경우도 분명 존재하며, 이럴때 state라는 것을 사용한다.
 - 값을 저장하거나 변경할 수 있는 객체로 보통 이벤트와 함께 사용된다. 
 - 컴포넌트에서 동적인 값을 상태(state)라고 부르며, 동적인 데이터를 다룰 때 사용된다 볼 수 있다.


<img width="200" alt="useState" src="https://github.com/leedongdong2/springBootTest/assets/77323959/4d9ce13a-2a62-4b6b-8d1e-aeb291825527">
<img width="125" alt="useState2" src="https://github.com/leedongdong2/springBootTest/assets/77323959/f566bf66-39df-4ce8-b1d9-52f704c68ca7">
<img width="126" alt="useState3" src="https://github.com/leedongdong2/springBootTest/assets/77323959/213ccc1e-82cf-4015-9a68-2ee021654319">

4.map함수란!
 - 반복되는 컴포넌트를 렌더링하기 위하여 자바스크립트 배열의 내장 함수인 map()을 사용 한다.
 - 파라미터로 전달된 함수를 사용하여 배열 내 각 요소를 원하는 규칙에 따라 변환한 후 새로운 배열 생성 한다.
 - 문법
 - arr.map(callbackFunction, [thisArg])
 - arr.map(callbackFunction(currenValue, index, array), thisArg)
 1) callbackFunction : 새로운 배열의 요소를 생성하는 함수로서 다음 세가지 인수를 갖는다.
    ㆍcurrenVlaue : 현재 배열(arr) 내의 값들을 의미
    ㆍindex : 현재 배열 내 값의 인덱스를 의미
    ㆍarray : 현재 배열
 2) thisArg(선택항목) : callback 함부 내부에서 사용할 this 레퍼런스 를 설정한다.
<img width="343" alt="map" src="https://github.com/leedongdong2/springBootTest/assets/77323959/71503e63-b13e-4be8-93f3-91f14e56305b">
<img width="283" alt="map2" src="https://github.com/leedongdong2/springBootTest/assets/77323959/6964a8b8-6de3-4b58-8494-6bf225b1e1e3">
<img width="164" alt="map3" src="https://github.com/leedongdong2/springBootTest/assets/77323959/64abf94c-c2d3-4b09-a409-d7069a78fb2d">

5.이벤트 처리 방법!
- 컴포넌트에서 출력된 특정 DOM 객체에 이벤트 컴포넌트가 동작하기 위해선 DOM이벤트 프로퍼티를 사용해야 한다.
 - 우리가 흔히 쓰고 있는 HTML 엘리먼트의 이벤트들은 JSX내에서 'on + 이벤트명' 형태의 프로퍼티로 제공된다.

<img width="458" alt="map4" src="https://github.com/leedongdong2/springBootTest/assets/77323959/1e263cc3-1ea1-471a-88d1-dae5e0e575c2">
-문법
 - 소문자 대신 카멜 케이스(camelCase)를 사용한다.
 -JSX를 사용하여 문자열이 아닌 함수로 이벤트 핸들러를 전달한다.  -useState 사용에서 참고
 - React에서는 false를 반환해도 기본 동작을 방지할 수 없다.
 - 반드시 preventDefault를 명시적으로 호출해야 한다.
 
 ※혹시 함수명 뒤에 ()를 넣는 경우 ex) onClick={changeName()}
  changeName이라는 함수가 반환하는 값이 들어 가게 된다.
  이 함수에서 반환하는 값이 없다면 undefined가 들어가게 원하는 결과가 나오지 않을 수 있다
  
  6.리액트 라우터
  - 사용자가 요청한 URL에 따라 해당 URL에 맞는 페이지를 보여주는 것이라고 생각할 수 있다.
  - 리액트에서는 라우팅 관련 라이브러리가 많이 있는데, 이중 가장 많이 쓰이는 리액트 라우터(React Router)다.
  - 사용자가 입력한 주소를 감지하는 역할을 하며, 여러 환경에서 동작할 수 있도록 여러 종유의 라우터 컴포넌트를 제공한다.
  - 이중 가장 많이 사용하는 라우터 컴포넌트는 BrowserRouter와 HashRouter이다.
  - BrowserRouter : HTML5를 지원하는 브라우저의 주소를 감지 한다.
  - HashRouter 해시 주소(http://goddaehee.tistory.com/#test )를 감지 한다.
   - 웹 페이지에서는 원래 링크를 보여줄 때 a태그를 사용한다. 하지만 a태그는 클릭시 페이지를 새로 불러오기때문에 사용하지 않는다.
 - Link 컴포넌트를 사용하는데, 생김새는 a태그를 사용하지만, History API를 통해 브라우저 주소의 경로만 바꾸는 기능이 내장되어 있다.
 - 문법 : <Link to="경로">링크명</Link>
 - import { Link } from 'react-router-dom';

<img width="256" alt="REOUTE" src="https://github.com/leedongdong2/springBootTest/assets/77323959/96c1d58c-3387-40bf-a638-e5f9799d4457">
<img width="289" alt="WEF" src="https://github.com/leedongdong2/springBootTest/assets/77323959/0fc96b8f-ebaa-4e9b-8c43-68a60d0e2348">
<img width="81" alt="WEF2" src="https://github.com/leedongdong2/springBootTest/assets/77323959/68e3c74f-2f41-47d8-a7a0-1110660333f6">
<img width="74" alt="WEF3" src="https://github.com/leedongdong2/springBootTest/assets/77323959/ce201fe0-6841-4d93-be5c-0e6d62400920">

7.axios

-AJAX란, Javascript의 라이브러리중 하나이며 Asynchronous Javascript And Xml(비동기식 자바스크립트와 xml)의 약자이다. 
-브라우저가 가지고있는 XMLHttpRequest 객체를 이용해서 전체 페이지를 새로 고치지 않고도 페이지의 일부만을 위한 데이터를 로드하는 기법
-JavaScript를 사용한 비동기 통신, 클라이언트와 서버간에 XML 데이터를 주고받는 기술이다.
-정리하자면, 자바스크립트를 통해서 서버에 데이터를 요청하는 것이다.
-비동기 방식은 웹페이지를 리로드하지 않고 데이터를 불러오는 방식
-Ajax를 통해서 서버에 요청을 한 후 멈추어 있는 것이 아니라 그 프로그램은 계속 돌아간다는 의미를 내포하고 있다.
<br>
<img width="322" alt="axios" src="https://github.com/leedongdong2/springBootTest/assets/77323959/7bcf2f4c-c880-4f16-96c2-061b54493a94">
<img width="327" alt="axios2" src="https://github.com/leedongdong2/springBootTest/assets/77323959/7725f34b-b443-4398-81f7-b6b8445964e1">
<img width="72" alt="axios3" src="https://github.com/leedongdong2/springBootTest/assets/77323959/a2a467de-df8b-440c-9a5d-c0dd05dd1fcd">

8.react hook form (uesform)<br>
-form을 보다 쉽게 관리하기 위한 react hook 라이브러리다.<br>
-값의 변경, submit, 조회, 오류 검출 등의 기능을 상태 하나에 귀속되는 것이 아닌 form에 필요한 모든 상태를 
useForm 한번으로 처리가 가능하다.
-값의 변경 함수,올바른 값 체크 등에 필요한 반복되는 js를 줄여준다.
<br>
-필요한 기능들을 넣어 useform을 생성해준다.<br>
-<img width="281" alt="userform" src="https://github.com/leedongdong2/reactJs/assets/77323959/9f26c1b4-6fce-4991-a240-96009bce22aa">
<br>
-{..register}를 사용하여 name,value,onChageEvent,정규식등을 간단하게 해결가능하게 해준다.<br>
<img width="401" alt="userform2" src="https://github.com/leedongdong2/reactJs/assets/77323959/3025ecf6-de3d-456b-bac5-963ba8ad99c3">
<br>
-handleSubmit은 form을 submit 할 때 데이터를 핸들링 해주는 함수이다. <br>
-form의 validation을 해서 올바르면 데이터를 넘기고 올바르지 않으면 error를 나타낸다.<br>
-커스터마이징한 함수와 같이 쓸수도 잇다.<br>
-기본값으로 쓰려면 handleSubmit(onValid, onInvalid)로 써주면된다.<br>
<img width="373" alt="userform3" src="https://github.com/leedongdong2/reactJs/assets/77323959/d871ffec-ccb7-4b28-8004-ab134d857515">
