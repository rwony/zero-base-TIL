# Mission2

아래 요구사항을 모두 반영하여, **접근성 높은 데이터 테이블을 제작해보세요.**

과제는 본인의 깃헙에 작성한 후, 해당 글(미션2)에 링크를 제출하세요.

<br>

### 요구사항

1. 본인이 생각했을 때, 접근성이 좋지 않은 테이블이 있는 웹페이지를 선정 (현재 서비스 중인 웹페이지로 선정)
  - 서울특별시 웹 사이트 > 분야별 정보 > 버스·지하철·택시교통카드교통 요금 안내
  - [https://news.seoul.go.kr/traffic/traffic_price](https://news.seoul.go.kr/traffic/traffic_price)

<br>

2. 웹표준 준수 및 웹접근성 관점에서 기존 서비스의 문제점 분석
  - 페이지 내 모든 테이블을 `<div>` 태그 하나로 엮음으로써 웹 접근성 관점에서 관련성이 떨어진다.
  - `<caption>`이 존재하지 않으므로 표의 제목 및 요약정보를 알 수 없어 무엇에 대한 정보인지 알기 어렵다. (summary는 html5에서 지원하지 않기 때문에 caption만 언급)
  - `<th>`가 존재하지 않으며, scope 속성이 없기 때문에 열/행 구분이 어렵다.

<br>

3. 위 이슈를 WCAG 가이드라인에 맞춰 수정 계획 선정
  - 관련된 컨텐츠 중 페이지의 문맥에서 벗어나도 그 자체만으로 이해가되므로, semantic markup을 위해 `<div>` 대신 `<article>`, `<section>` 태그를 사용한다.
  - `<caption>`을 사용하여 표의 제목 및 요약 정보를 작성하여 웹 접근성을 높이고 table 요소의 가장 첫 번째 자식으로 오도록한다.
  - `<caption>`의 경우 화면에서는 보이지 않아야 하지만 스크린 리더는 읽을 수 있어야 하므로, 숨김 처리를 한다.
  - `<thead>` 요소를 사용하고 `<thead>` 태그 안에 `<th>` 태그를 사용하여 제목 셀을 명시함으로써 구조적 의미를 갖게 한다.
  - 웹 접근성을 위해 `<th>` 태그 안에 scope 속성을 넣어줌으로써 웹 접근성을 높인다.

<br>

4. 웹접근성 관련 체크리스트 작성
  - [ ]  모든 속성 값은 따옴표로 묶었는가?
  - [ ]  단일 태그의 마무리는 항상 '/>'로 하여 의도를 명확히 드러냈는가?
  - [ ]  charset을 지정하였는가?
  - [ ]  색상은 RGB 코드로 작성하였는가?
  - [ ]  코드 들여쓰기를 하였는가?
  - [ ]  <h>태그를 상황에 맞게 사용하였는가?
  - [ ]  표 형식을 나타낼 때 table 태그를 사용하였는가?
  - [ ]  사이즈는 px(픽셀) 단위를 주로 사용하였는가?
  - [ ]  HTML, CSS, Javascript가 분리되었는가?
  - [ ]  사용자가 예측하지 않은 기능이 실행되지 않도록 작업되었는가?
  - [ ]  자동 재생 배경음악을 적용 금지하였는가?

<br>

5. HTML/CSS를 활용하여 구현(자바스크립트는 선택사항)

<br>

6. 문법 검사 결과 제출

 - [https://validator.w3.org/unicorn/check?ucn_uri=https%3A%2F%2Felated-knuth-f9343a.netlify.app%2F&ucn_lang=ko&ucn_task=conformance#feed](https://validator.w3.org/unicorn/check?ucn_uri=https%3A%2F%2Felated-knuth-f9343a.netlify.app%2F&ucn_lang=ko&ucn_task=conformance#feed)
![check](https://user-images.githubusercontent.com/88661435/135985501-75a02f5f-eb57-46ad-9748-5986b1932e68.JPG)

<br>

7. 라이트하우스에서 접근성 및 SEO 관련 분석 리포트 제출

 - [https://googlechrome.github.io/lighthouse/viewer/?psiurl=https%3A%2F%2Felated-knuth-f9343a.netlify.app%2F&strategy=mobile&category=performance&category=accessibility&category=best-practices&category=seo&category=pwa&utm_source=lh-chrome-ext](https://googlechrome.github.io/lighthouse/viewer/?psiurl=https%3A%2F%2Felated-knuth-f9343a.netlify.app%2F&strategy=mobile&category=performance&category=accessibility&category=best-practices&category=seo&category=pwa&utm_source=lh-chrome-ext)
![check2](https://user-images.githubusercontent.com/88661435/135985633-7d6176ac-bb0a-478e-9cc1-f7a4dcecf13d.JPG)

<br>

8. 프로젝트 완료 후기(시행착오 및 성장기)

모든 사람들의 평등한 웹 사이트 이용을 위해서는 웹 표준 준수와 웹 접근성이 높아야한다. 부끄럽게도 기존에는 이 문제에 대해 중요하게 생각하지 못 했었다. 하지만 네카라쿠배 html을 공부하는 과정에서 강사님께서 재차 강조하시는 부분이었고, 공부하면서 얼마나 중요한지 깨닫게 되었다.

정말 많은 사이트들을 찾아봤는데, 먼저 공공기관이나 큰 포털사이트들은 웹 접근성 마크를 획득하여 홈페이지 하단에 게시해놓은 곳이 많았다. 그러던 중 서울시 홈페이지에서 데이터 테이블을 발견했는데, 테이블 각각에 대한 웹 접근성은 좋은 편이 아니었다. 그래서 이 사이트를 수정해보기로 결심했다.

테이블을 작성하면서 각각의 속성에 대하여 왜 써야하는지, 왜 시맨틱 마크업을 해야하는지를 깨달았다. 그리고 접근성을 고려한 CSS를 작성하는 것도 중요하다고 깨닫게 되었다. 눈에 보이는 것만이 전부가 아니기 때문이다. 

코드를 작성하는 몇 초, 몇 분의 시간이 누구에게는 큰 도움이 된다는 것을 생각하니 시맨틱 마크업이 얼마나 중요한지 다시 한 번 생각하게 되는 시간이었다.
