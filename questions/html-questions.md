# HTML Questions:

* What does a `doctype` do?
  - 브라우저가 문서를 해석할 때 어떤 표준을 따를것인가에 대한 선언.
  - doctype이 있을경우 standard, 없을경우 quirk모드로 문서를 해석.
  - 표준 모드의 경우 모든 브라우저에서 거의 같은 결과를 기대할 수 있음.
  - 호환 모드의 경우 해석시간, 출력시간이 오래 걸리고 브라우저 마다 같은 결과를 기대할 수 없음.
* How do you serve a page with content in multiple languages?
  - i18n 등을 이용해 serving.
* What kind of things must you be wary of when design or developing for multilingual sites?
  - 언어에 따른 layout 변화 (버튼의 width 라던지...).
  - static text에 i18n을 무조건 적용 (나중에 적용하는 경우 실수가 발생할 수도 있음).
* What are `data-` attributes good for?
  - DOM parsing을 위해 HTML에 data를 저장하거나 정보를 추적 가능.
* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
  - cookie: 만료 시간을 설정할 수 있는 key-value storage. 4kb의 용량 제한이 있으며, 서버로 요청을 보낼시 반드시 cookie도 같이 보내게 됨.
  - localStorage: 5mb의 용량 제한이 있으며, 수동으로 데이터를 지우지 않는 이상 storage에 남게 됨. 서버로 요청을 보낼시 전송되지 않아 cookie에 비해서 트래픽 비용을 낮출 수 있음. same-origin 정책에서 작동함.
  - sessionStorage: localStorage와 비슷함. window, tab마다 storage가 제공됨. window 혹은 tab을 닫으면 저장된 정보가 삭제됨.
* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
  - `<script>`: 다운로드 / 실행하는 동안 DOM parsing을 멈춤.
  - `<script async>`: 다운로드하는 동안 DOM parsing을 멈추지 않음. 다운 받자마자 script 실행.
  - `<script defer>`: 다운로드 / 실행하는 동안 DOM parsing을 멈추지 않음. script가 DOM parsing이 모두 끝난 이후 실행됨.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
  - css: FOUC(Flash of Unstyled Content)문제를 막을 수 있음.
  - JS: 다운 및 실행되는 동안 DOM parsing이 멈추는 문제를 막을 수 있음.
* What is progressive rendering?
* Why you would use a `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.
  - viewport의 width에 따라 image resource를 다르게 load할 수 있음.
* Have you used different HTML templating languages before?
