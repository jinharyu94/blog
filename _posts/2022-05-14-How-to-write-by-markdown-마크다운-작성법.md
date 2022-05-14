---
layout: post
title: "How to write by markdown"
subtitle: "깃헙 블로그를 시작하며 정리한 마크다운 작성법"
author: "Jinha"
categories: study etc
tags: [study, markdown, github]
---

### github page와 markdown

외주 개발을 계속하다보면 조금씩이나마 개발에 관한 스터디는 계속 하게 되다보니 PM으로만 나를 소개하기에는 좀 많이 간거 같기도 하고, 그렇다고 개발자라고 소개하기에는 개발자 포지션은 전혀 아니라 애매했던 포인트.   

전부터 개발블로그를 좀 만들어보고싶다는 생각을 계속 해왔었는데, 개발자도 아니고 너무 오버아닌가.. 싶어서 미뤄왔었다.
세상엔 멋진 개발자들이 많고, 그 옆에서 함께 일할 수 있다는 것만으로도 행복하니까.   

스터디를 하다가 블로그에 공부한 내용을 공유하기로 했는데, 개발에 대한 글을 쓸 곳이 없어서 깃헙블로그를 하나 만들었더니,   
엥? markdown으로 글을 써야한다고? 찾아보니 기본적인 작성법은 많이 어렵지 않아서 다행이었지만 익숙하지 않으니 정리가 한번 필요해졌다.

***

# markdown

HTML로 변환할 수 있는 마크업언어이자 문서인 markdown. 문법이 간단해서 직관적으로 사용할 수 있다.   
많은 이들이 그렇듯 나도 github의 read me 파일을 접하면서 처음 .md파일을 만나게 되었는데, 매번 읽기만하고 쓰는 법을 몰라 직접 작성해본 적은 없었다.
이제부터는 직접 작성할 수 있으니, 간단한 부분은 굳이 직원들 손을 거치지 않고 직접 작성해야겠다.

## How to write

### 1. Header
># H1
>## H2
>### H3
>#### H4
>##### H5
>###### H6
>H1
>==
>H2
>--

```
# H1
## H2
### H3
#### H4
##### H5
###### H6
H1
==
H2
--
```
' ###을 붙인 후 띄어쓰기를 하지 않으면 git blog에 적용되지 않을 때가 있었다.'

### 2. BlockQuote
인용구. 내부에서 다른 markdown문법 사용가능
> BlockQuote 사용하기
>   > BlockQuote 사용하기
>   >   > BlockQuote 사용하기
```
> BlockQuote 사용하기
>   > BlockQuote 사용하기
>   >   > BlockQuote 사용하기
```


### 3. List
1. 순서있는 번호
2. 순서있는 번호
3. 순서있는 번호
```
1. 순서있는 번호
2. 순서있는 번호
3. 순서있는 번호
```
어떤 순서로 써도 순서대로 정렬됨

- 글머리 기호
  - 글머리 기호
    - 글머리 기호
- 글머리 기호
+ 글머리 기호
* 글머리 기호

```
- 글머리 기호
  - 글머리 기호
    - 글머리 기호
- 글머리 기호
+ 글머리 기호
* 글머리 기호
```
'-, +, * 을 혼용해서 써도 같은 결과. 들여쓰기로 단계구분'

### 4. Code Block
들여쓰기를 하거나 앞뒤로 "```"를 추가해 코드블럭을 만들 수 있다.   
시작하는 세개의 백틱 바로 뒤에 언어의 이름 선언하면 Syntax highlighing 사용가능.

```javascript
let syntax = 'javascript'
console.log(syntax) 
```

    ```javascript
    let syntax = 'javascript'
    console.log(syntax)
    ```

### 5. Horizontal line

***
---
--------
```
***
---
--------
```

### 6. Link
외부링크 추가하기   
[Git hub page](https://pages.github.com/)
```    
[Git bub page](https://pages.github.com/)
```

참조링크 추가하기   
[Git hub][githublink]   

[githublink]: https://pages.github.com/

```
[Git hub][githublink]   

[githublink]: https://pages.github.com/
```


### 7. Italic

*Italic Text*   
_Itaclic Text_

```
*Italic Text*   
_Itaclic Text_
```


### 8. Bold

**Blod Text**
__Blod Text__

```
**Blod Text**
__Blod Text__
```

### 9. Link Break

문장 뒤 세칸 띄어쓰기를 하면 줄 바꿈을 할 수 있다.

