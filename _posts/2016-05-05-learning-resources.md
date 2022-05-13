---
layout: post
title: "JavaScript 내장함수"
author: "Jinha"
categories: JavaScript
tags: [Study,JavaScript]
image: arctic-2.jpg
---

다시 한번 JavaScript 스터디를 도전하면서 만든 내장함수 사전


String
======

####.length
글자길이 반환   

####.indexOf("찾을 글자")
해당 글자의 인덱스 반환
####.lastIndexOf
해당 글자의 뒤에서부터의 인덱스 반환
####.slice(시작인덱스, 끝인덱스)
잘라서 반환
인덱스 값은  - 로 주면 뒤에서 부터 셈
####.subString(시작인덱스, 끝인덱스)   

####.substr(시작인덱스, 길이)   

####.replace("바꿀 문자열", "새문자열")   

####.replace(/바꿀 문자열/g, "새문자열")
모든 문자 찾아서 적용
####.replace(/바꿀 문자열/i, "새문자열")
대소문자 구분 안하고 찾음
####.toUpperCase()
모두 대문자로
####.toLowerCase()
모두 소문자로
####.concat(결합할 문자열)
문자열 결합
####.trim
앞뒤 공백 삭제
####.padStart(앞에 몇자리를 만들지, 넣을 글자)
스트링의 글자수를 맞춰주기
####.padEnd(뒤에 몇자리를 만들지, 넣을 글자)

####.charAt(찾을 문자열 인덱스)
찾은 문자열을 반환
####.split(기준 문자)
기준문자를 기준으로 스트링을 잘라서 배열로 만들어줌    

***

Number
======

####.toString
숫자를 문자열로 변경
####.toFixed(소수점 자리수 지정)
지정된 소수점 자리수까지 반올림으로 표기
####.toPrecision(소수점 자리수 지정)
정수까지포함해서 지정된 소수점 자리수까지 표기
####.Number(숫자로 바꿀 무언가)
내용을 숫자로 바꿔줌   
앞뒤 공백을 제외하고 알아서 바꿔줌   
변경불가할때는 NaN(Not a Number)로 반환
####.parseInt(정수로 바꿀 무언가)
내용을 정수로 바꿔줌   
소수점은 버림   
바꿀것이 많으면 첫번째것만 바꿈   
바꿀수 없는것이 앞에 있으면  NaN
####.parseFloat(실수로 바굴 무언가)
내용을 정수로 바꿔줌   
바꿀것이 많으면 첫번째것만 바꿈   
바꿀수 없는것이 앞에 있으면  NaN

***

Boolean 내장 함수
======

new Boolean() 같은 생성자로 값을 지정할 경우 지정된 값의 타입은 객체가 된다
```javascript
var x = true
var y = new Boolean(true)

console.log(x === y) //false
consile.log(typeof x) //boolean
consile.log(typeof y) //object
```

***
Array
======
####.toString()
문자열로 리턴
####.join(<String>)
배열의 각 요소 사이를 string으로 연결해서 리턴
####.push(<Type>)
배열의 마지막에 요소를 추가
####.pop()
배열의 마지막 요소를 제거, 제거한 요소를 리턴
####.shift()
배열의 첫번째 요소를 제거, 제거된 요소를 리턴
####.unshift()
배열의 첫번째에 요소를 추가
####.splice(<Number>, <Number>, <Type>...)
시작위치, 삭제할 요소 수 에 요소 추가
####.concat(<Array>)
기존 배열 뒤에 다른 배열을 이어붙여서 리턴
####.slice(<Number>, <Number>)
시작점, 끝점을 잘라서 리턴
####.sort()
알파벳 순으로 정렬, 숫자의 경우 sort 안에 정렬함수를 넣어 사용
####.reverse()
역순으로 정렬해서 리턴
####.filter()
인자로 함수, 조건에 맞는 요소만 넣은 배열을 리턴
####.reduce(<Function>)
function에 accumulator, currentValue, index, array 인자로 사용
####.map(<Function>)
배열을 가지고 다른 값을가진 배열을 생성할수있음

***
Date
===
생성자: new Date()

####.getFullYear()
현재 년도
####.getMonth()
현재 월
####.getDate()
현재 날짜
####.getDay()
현재 요일의 index
####.getHours()
현재 시간
####.getMinutes()
현재 분
####.getSeconds()
현재 초
####.getTimezoneOffset()
분단위로 리턴

get 뒤에 UTC를 붙이면 UTC기준의 시간를 가져온다   
*ex) .getUTCMonth()*

글로벌 서비스를 준비 할 때는 타임존 고려   
**UTC+0** 과의 시차를 고려해서 클라이언트단에서 나오게 끔하기

[moment.js](https://velog.io/@dojunggeun/JavaScript-Moment.js%EB%A5%BC-%EC%9D%B4%EC%9A%A9%ED%95%98%EC%97%AC-Date-Time-%EA%B4%80%EB%A6%AC%ED%95%98%EA%B8%B0)   
원하는 방식으로 날짜,시간을 분석, 검증, 조작, 표시할수 있는 라이브러리
국가마다 다른 시간대를 상대적으로 쉽게 해결


***
Math
===

####.round(<Number>)
반올림
####.ceil(<Number>)
올림
####.floor(<Number>)
내림
####.trunc(<Number>)
소수점 버림(정수부만 리턴)
####.sign(<Number>)
음수면 -1, 양수면 1, 0이면 0 리턴
####.pow(<Number>, <Number>)
앞숫자의 뒷숫자제곱
####.sqrt(<Number>)
루트
####.abs(<Number>)
절대값반환(양수로 반환)
####.max(<Number>...)
최댓값 리턴
####.min(<Number>...)
최소값 리턴
####.random()
0~1사이의 숫자 리턴

***

JSON
===
JavaScript Object Notation   

서버에서 웹페이지로, 웹페이지에서 서버로 데이터를 전송할 때 자주 사용하는 포맷   
포맷이 엄격한 편   

아래와 같은 포맷을 지켜야 함
```javascript
var = data = {
    “employees” : [
        {”firstName” : “John”, “lastName” : “Doe”},
        ]
    }
```

####JSON.stringify()
오브젝트를 문자열로 변환

####JSON.parse(<String>)
문자열을 오브젝트로 변환

서버에서 data를 주고받을때 문자열로 주고받게 된다.   
때문에 서버에서 받은 data를 사용하려면 parse를 해서 Object로 바꿔줘야한다.   
그리고 다시 서버로 data를 줄때 stringify로 문자열로 바꿔서 전송한다.

***

Window 객체
===

####.alert(<String>)
메세지창을 띄움
####.confirm(<String>)
취소, 확인 버튼있는 메세지창을띄우고 boolean 값을 리턴
####.prompt(<String>)
input 가능한 메세지창 띄움, 확인 - input 값 리턴, 취소 - null 리턴
####.open(<String>)
문자열 url을 새창으로 띄움
####.print(<String>)
현재 페이지를 인쇄하는 창을 띄움
####.setTimeout(<Function>, <Number>)
실행부, 밀리세컨드, 지정된 시간 후 함수실행(1회)
####.setInterval(<Function>, <Number>)
지정된 시간마다 함수실행
####.clearInterval(<Function>)
interval 함수를 종료


***

크롬 개발자도구 console
===

####.log()
콘솔에 출력
####.info()
콘솔에 정보 출력(log과 비슷하지만 다르다고함)
####.warn()
콘솔에 경고문구를 출력
####.error()
콘솔에 에러문구를 출력
####.table()
콘솔에 표 형식으로 출력
####.time() .timeEnd()
time과 timeEnd 사이의 소요시간 출력

*브라우저 요소 선택 : ctrl + shift + c / command + shift + c*
