# Tag
- 정의 : html 문서를 이루는 문법적 표시
- 구성 : 여는태그 < > 와 닫는태그 </>가 있고 이 내부에 text content 등을 포함한다.
	내용없이 사용되는 태그도 있다.

## html을 구성하는 태그
- ```<head>```는 메타데이터가 담기는 곳이다.
- 구성
  - 페이지의 제목
  - 파비콘
  - 기타 메타정보(charset UTF-8, IE관련 호환정보, viewport)
  - css와 js 등의 코드와 링크
- ```<body>```는 html 문서의 내용을 나타낸다.

## 강조하기 위한 tag
- <i>i태그</i>와 <em>em태그</em>
- <b>b태그</b>와 <strong>strong태그</strong>
  - 이와같이 겉보기엔 같아도 용도가 다른 태그들이 있다.
  - i태그와 b태그는 css로 꾸밀 것을 표시하기 위한 용도이고 em태그와 strong태그는 강조하기 위해 사용된다.

## 가독성을 위한 태그이름 짓기
- 태그 위주나 class(id)위주로 태그의 이름을 지으면 선택자가 장황해지고 요소를 식별하기 어렵다.
- BEM (.Block__Element--Modifier)
  - 태그 위주에 요소와 수정사항을 넣는 방식이다.
  - 명확한 선택자로 중복 문제를 해소한다
  - 높은 가독성과 이해하기 쉬운 구조를 가진다
  - 예시) figure.card__image--soldout
    - card라는 Block을 공유하고 있는 태그중 figure태그이며 요소는 image이다. 변경사항으로는 이미 판매된 상품임을 표시하기 위해 soldout을 사용했다.

# Semantic Tags
- 페이지에서 해당 요소가 의미와 역할을 가진다.
- 시맨틱 태그의 유용성
  - 웹 접근성 개선 : 스크린 리더로 페이지를 보는 사람들이 정보를 찾기 쉬워진다.
  - SEO (Search Engine Optimization) : 검색엔진이 페이지를 분석할 때 각 정보의 종류를 파악하는데 도움이 된다.
  - 유지보수와 가독성 : 코드를 읽고 구조를 파악하기 쉽다.

## 웹페이지를 구성하는 semantic tags
- `<header>`
  - 페이지나 구획의 제목 역할을 하는 요소들
  - 로고, 제목, 검색창 등
- `<nav>`
  - 메뉴나 색인 등
- `<main>`
  - 페이지의 주요 내용 부분
  - 하나만 존재
- `<article>`
  - 페이지 내에서 재사용될 수 있거나 페이지로부터 독립적
- `<section>`
  - 페이지의 컨텐츠를 일정 단위로 나눌 때 사용
  - 더 작은 단위는 div
- `<aside>`
  - 사이드 바 등 주요내용과 간접적으로 연관된 컨텐츠를 포함
- `<footer>`
  - 관리자 및 페이지의 정보가 들어감

# Attributes
- 속성 또는 특성
- 태그의 동작을 설정 및 제어

# Flex
- 내부 요소를 flex방식으로 배치한다. 
- flex-direction
  - 내부 요소의 배치 방식을 정한다.
  - row : 옆으로 정렬
  - column : 아래로 정렬
  - row-reverse , column-reverse : 역으로 정렬
- flex-wrap
  - 내부 요소가 컨테이너를 넘어갈 때 이들을 여러줄에 걸쳐 나열할건지 넘어가서 쭉 이어 가게 할건지 정한다.
- justify-content
  - 메인 축에서 아이템을 정렬할 방식을 정한다.
  - flex-start, center, flex-end : 시작 중간 끝
  - space-(between, around, evenly) : 양쪽 정렬, 가운데 정렬, 균등하게 정렬
- align-items
  - 메인 축의 반대에서 아이템을 정렬할 방식을 정함
  - wrap으로 여러줄이 되면 align-content로 다양하게 정렬 가능
- gap
  - 간격을 설정

# Grid
- 2차원으로 수평, 수직을 동시에 영역을 나눌 수 있다.
- 자식요소를 겹치게 층을 지면서 자리를 잡도록 각 요소의 위치를 지정해 줄 수 있다.(규칙적이지 않은 것에 효과적)
- grid-template-columns 
	-	가로 그리드 영역 정의(몇 칸으로 나눌지)
	-	fr
		-	자동으로 비율 맞춰서 나누는 단위,  
			1fr 1fr 1fr 1fr 하면 4등분 해줌
- grid-template-rows
	-	세로 그리드 영역 정의 (몇 칸으로 나눌지)
- grid-column
	-	해당 요소의 가로 그리드 배치
	-	3칸 채울려면 1/4로 해야한다. (시작 선이 1번이기에)
- grid-row
	-	해당 요소의 세로 그리드 배치

# Media Query
- 반응형 웹을 만들어준다.
- 사용자마다 화면크기가 다른 것을 고려하여 디자인을 바꿔준다.

### 적응형 웹
- 모바일 환경인지 PC환경인지에 따라 다른 페이지를 보여준다.