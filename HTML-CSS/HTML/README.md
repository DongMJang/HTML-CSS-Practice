# HTML  
---

| | 블록 요소 (Block level) | 인라인 요소 (Inline)
--- | --- | ---  
너비 | 사용 가능한 최대 가로 너비 사용 | 필요한 너비만 사용
크기 지정 | 가능 | 불가능
대표적 요소 | div, h1, p | span, img
주로 쓰이는 용도 | 레이아웃 | 텍스트
width, height 기본값 | width: 100, height: 0 | width: 0, height: 0
margin, padding | 모든면 사용 가능 | 양 옆만 사용 가능
연속 입력시 | 수직으로 쌓임 | 수평으로 쌓임

# 주요 범위
---
# `<html>`
> HTML 문서의 **범위**를 설정
> 모든 다른 요소는 `<html>` 요소의 **후손**이어야 함

속성 | 의미 | 값 
--- | --- | ---
lang | 문서의 언어 | ko, en, es ...  
# `<head>`  
> HTML 문서의 **정보**를 설정  
# `<body>`  
> HTML 문서의 **구조**  
---
# 메타데이터  
## 스타일, 스크립트, 각종 소프트웨어의 탐색 및 렌더링을 도와줄 데이터 등 페이지에 대한 정보

# `<meta/>`
> (`<link/>`,`<style>` 같은) 기타 메타데이터 요소로 나타낼 수 없는 메타데이터를 **나타내기** 위해 설정

속성 | 의미 | 값 
--- | --- | ---
charset | 문자인코딩 방식 | UTF-8(조합형), EUC-KR(완성형), ...
name | 메타 데이터의 이름 | author, description, ...
http-equiv | 서버/사용자 에이전트의 작동방식 변경에 대한 지시 | refresh,X-UA-Compatible, ...
content | name, http-equiv 의 값
# `<title>`
>  브라우저의 **제목** 표시줄 또는 페이지 탭에 보여지는 문서의 **제목**  
> **텍스트**만 포함 가능 태그 포함시 무시
# `<link/>`
> 현재 문서와 외부 리소스의 **관계**를 명시
> **stylesheet**를 연결할 때 가장 많이 사용, 다른 여러가지로 쓸 수 있음

속성 | 의미 | 값 
--- | --- | ---
rel | 현재 문서와 외부 리소스와의 관계 | stylesheet, icon, ...
href | 외부 리소스의 URL | URL
type | 외부 리소스의 MIME 타입 | text/css, image/x-icon, ...

# `<style>`
> 문서나 문서 일부에 대한 **스타일 정보**를 설정
> 스타일은 외부 스타일 시트에 작성하고 `<link>`로 연결이 **효율적**

속성 | 의미 | 기본값 
--- | --- | ---
type | MIME 타입 | text/css
 
 # `<base>`
 > 문서 안의 모든 상대 URL이 사용할 **기준 URL**을 지정
 > 문서에는 **하나**의 `<base>`요소만 존재 가능
 
 속성 | 의미 | 값 | 기본값 
--- | --- | --- | ---
href | 기준 URL | URL
target | A 요소처럼 target 속성을 사용하는 요소의 기본값 | _self, _blank | _self
---
# 콘텐츠 구분  

# `<header>`
>문서의 **header**를 설정
**소개 및 탐색**에 도움을 주는 콘텐츠 (로고, 제목, 검색 등)
display: block

![image](https://user-images.githubusercontent.com/77039437/104091344-230a2d00-52c0-11eb-9fc4-2808378a3ba6.png)



# `<footer>`
>문서의 **footer**를 설정
가장 가까운 **구획 콘텐츠**나 **구획 루트** (구획의 작성자, 저작권 정보, 관련 문서)
display: block

![image](https://user-images.githubusercontent.com/77039437/104091377-5f3d8d80-52c0-11eb-8288-3bf2f4facefd.png)

# `<h1>`

<img width="306" alt="GitHub-h1~" src="https://user-images.githubusercontent.com/77039437/104170879-2975e180-5445-11eb-9d9e-0b9ecefecdd3.png">


# `<main>`
 >문서의 **핵심 주제**
 애플리케이션의 **핵심 기능성**에 대해 부연 또는 직접적으로 연관된 콘텐츠
 한 문서에 하나의 `<main>` 요소만 포함 가능
 display: block (Internet Explorer)에서 호환 불가

 <img width="1361" alt="GitHub-main" src="https://user-images.githubusercontent.com/77039437/104170302-41993100-5444-11eb-9d08-dce512105cca.png">


# `<article>`
>**독립적**으로 구분되거나 재사용 가능한 영역을 설정
글, 매거진/신문의 기사, 블로그 글 등
display: block

<img width="302" alt="GitHub-article" src="https://user-images.githubusercontent.com/77039437/104171115-87a2c480-5445-11eb-868e-3a726f35df44.png">


# `<section>`
>문서의 **일반적인** 영역을 설정 (제목을 가지고 있는)
일반적으로 **`<h1>`~`<h6>`** 를 포함하여 식별
display: block

# `<aside>`
>문서의 **별도** 콘텐츠를 설정
**광고**나 **기타 링크** 등의 사이드바를 설정(콜아웃 박스)
display: block

# `<nav>`
>다른 페이지 링크를 제공하는 영역을 설정
메뉴, 목차, 색인
display: block

<img width="1177" alt="GitHub-nav" src="https://user-images.githubusercontent.com/77039437/104171890-b4a3a700-5446-11eb-93df-07a6829ae22c.png">

# `<address>`
> `<body>,<aritcle>,<footer>` 등에서 연락처 정보를 제공하기 위해 포함하여 사용
(메일 프로그램 열림)
display: block

# `<div>`
>의미가 없는 콘텐츠 영역을 설정
display: block