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