# General Questions:

* What did you learn yesterday/this week?
  - Cryptozombie 문제풀기.
  - rxjs / express.
* What excites or interests you about coding?
* What is a recent technical challenge you experienced and how did you solve it?
  - TypeScript를 이용한 React app boilerplate 작성.
* When building a new web site or maintaining one, can you explain some techniques you have used to increase performance?
* Can you describe some SEO best practices or techniques you have used lately?
* Can you explain any common techniques or recent issues solved in regards to front-end security?
* What actions have you personally taken on recent projects to increase maintainability of your code?
* Talk about your preferred development environment.
* Which version control systems are you familiar with?
* Can you describe your workflow when you create a web page?
* If you have 5 different stylesheets, how would you best integrate them into the site?
* Can you describe the difference between progressive enhancement and graceful degradation?
  - 우아한 성능저하(graceful degradation)
    - 최신 브라우저에 맞춘 app 작성 -> 이전 브라우저에 맞게 성능 및 js함수, css property 수정.
    - 최신 브라우저에서 동작하는 layer 제거.
    - 접근성 향상 / 새 표준 준수가 필요할 때 사용.
  - 점진적 향상(progressive enhancement)
    - 모든 브라우저에서 작동하도록 개발 -> 최신 브라우저에 맞는 고급 기능 layer 추가.
    - 대부분의 일반적인 경우 사용.
    - 기본버전 개발 후 테스트, layer추가시 각각의 layer테스트.
* How would you optimize a website's assets/resources(질문을 정확히 이해 못함)?
  - icon의 경우 image sprite 사용.
  - cdn을 통해 asset serving.
  - css, js file minified.
* How many resources will a browser download from a given domain at a time?
  * What are the exceptions?
  - Http/1.x spec에서 도메인 당 동시 요청 갯수가 제한되어있음. ([Http/1.x의 connection management](https://developer.mozilla.org/ko/docs/Web/HTTP/Connection_management_in_HTTP_1.x))
  - 대략 6~8개, IE하위 버전은 2개.
  - Domain Sharding
    - Domain Sharding은 static file(이미지, css, js)의 로딩 속도를 개선하는 방법으로, 여러개의 서브도메인을 생성하여 파일을 병렬로 가져옴.
  - Domain Sharding대신 Http/2로 전환하는 것이 좋음(동시에 여러 리소스를 받는것이 가능함) [참고](http://americanopeople.tistory.com/115).
* Name 3 ways to decrease page load (perceived or actual load time).
  - lazy load 이용.
  - 다운 받는 resouce 용량의 최소화(minified).
  - cdn 및 cache를 이용.
* If you jumped on a project and they used tabs and you used spaces, what would you do?
* Describe how you would create a simple slideshow page.
* If you could master one technology this year, what would it be?
* Explain the importance of standards and standards bodies.
* What is Flash of Unstyled Content? How do you avoid FOUC?
  - CSS가 적용되기 전, 잠시동안 CSS가 적용되지 않은 화면이 보이는것.
  - `<head />`태그 사이에 style link를 넣어 css 파일이 먼저 load 되도록 관리.
  - document가 onload되면 css class 등을 바꾸어 `<body />`태그의 visivilty를 관리.
* Explain what ARIA and screenreaders are, and how to make a website accessible.
  - 장애인들을 위한 접근성 향상 방법.
  - ARIA를 통해 nav landmark, JS widjet, form 힌트, 에러 메시지, 실시간 콘텐츠 업데이트 등에 접근성을 부여.
  - `role` attr을 통해 html tag에 적절한 타입을 정의. role=article 등...
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
  - UI 요소가 적고, simple하면서 반복적인 변화만 존재 할 경우 css 사용.
  - 복잡하거나 사용자와의 interaction이 필요한 경우 js 사용.
  - 반드시 css가 gpu의 도움을 받는것도 아니고 생각보다 js animation의 부하가 적음.
  - GSAP 같은 선택지도 있음.
* What does CORS stand for and what issue does it address?
  - Cross Origin Resouce Sharing.
  - Cross Origin request를 제어함 (다른 도메인으로의 ajax요청 등).
  - XMLHttpRequest는 same-origin 정책을 따름.
* How did you handle a disagreement with your boss or your collaborator?
* What resources do you use to learn about the latest in front end development and design?
