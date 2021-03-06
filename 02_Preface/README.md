# You Don't Know JS
# 들어가며

이미 눈치챘겠지만, 본 시리즈 제목 일부인 "`JS`"는 자바스크립트를 깎아내릴 의도로 쓴 약어가 아니다. 물론 자바스크립트 언어에 숨겨진 기벽 <sub>`quirk`</sub> 이 만인이 비난하는 대상임은 부인할 수 없겠지만!

웹 초장기 시절부터 자바스크립트는 사람들이 대화하듯 웹 콘텐츠를 소비할 수 있게 해준 기반 기술이었다. 마우스 트레일을 깜빡이거나 팝업 알림창을 띄워야 할 수요에서 비롯되어 20년 가까이 흐른 지금, 자바스크립트는 엄청난 규모로 기술적 역량이 성장하였고, 세계에서 가장 널리 사용되는 소프트웨어 플랫폼이라 불리는, 웹의 심장부를 형성하는 핵심 기술이 되었다.

그러나 프로그래밍 언어로서의 자바스크립트는 끊임없는 비난과 논란의 대상이기도 했는데, 부분적으론 과거로부터 전해 내려온 폐해 탓이기도 하지만, 그보다 설계 철학 자체가 문제시 되기도 했다. 브렌단 아이크<sub>`Brendan Eich`</sub> <sub>[01](#01)</sub>의 표현을 빌자면 '자바스크립트'란 이름 자체가 좀 더 성숙하고 나이 많은 형인 '자바' 아래의 "바보 같은 꼬마 동생 <sub>`dumb kid brother`</sub>" 같은 느낌을 준다. 하지만 이름은 정치와 마케팅 사정상 우연히 그렇게 붙여진 것일 뿐, 두 언어는 여러 중요한 부분에서 이질적이다. "자바스크립트"와 "자바"는 "카메라"와 "카<sub>`car`</sub>"만큼이나 무관하다.

`C` 스타일의 절차형 언어에서 미묘하며 불확실한 스킴<sub>`Scheme`</sub>/리스프<sub>`Lisp`</sub> 스타일의 함수형 언어에 이르기까지 자바스크립트는 서너 개 언어로부터 근본 개념과 구문 체계를 빌려 왔기 때문에 꽤 폭넓은 개발자층을 확보하는 데 대단히 유리했고, 심지어 프로그래밍 경력이 별로 없는 사람들도 쉽게 배울 수 있었다. "`Hello World`"를 자바스크립트로 출력하는 코드는 너무 단순해서 출시 당시엔 나름의 매력이 있었고 금방 익숙해졌다.
  
자바스크립트는 처음 시작하고 실행하기는 가장 쉬운 언어지만 독특한 기벽 탓에 다 른언어들에 비해 언어 자체를 완전히 익히고 섭렵한 달인은 찾아보기 매우 어려운 편 이다. `C/C++` 등으로 전체 규모<sub>`full-scale`</sub>의 프로그램을 작성하려면 언어 자체를 깊이 있게 알고 있어야 하지만, 자바스크립트는 언어 전체의 능력 중 일부를 대략 수박 겉 핥기 정도만 알고 사용해도 웬만큼 서비스를 운영할 수 있다.

언어 깊숙이 뿌리를 내려 자리잡은 정교하고 복잡한 개념이 외려 (콜백함수를 다른함수에 인자로 넘기는 것처럼) 겉보기에 단순한 방식으로 사용해도 괜찮게끔 유도하고, 그러다보니 자바스크립트 개발자는 내부에서 무슨 일들이 벌어지든, 있는 그대로의 언어 자체를 사용하여 개발할 수 있다.

그러나 간단하고 쓰기 쉬운 언어일수록 여러 가지 의미와 복잡하고 세밀한, 다양한 기법들이 결집되어 있기 때문에 꼼꼼하게 학습하지 않으면 제 아무리 노련한 개발자라 할지라도 올바르게 이해하지 못한다.

이것이 바로 자바스크립트의 역설이자 아킬레스건이며, 이 책을 읽고 여러분이 넘어야 할 산이다. 다 알지 못해도 사용하는 데 문제가 없다 보니 끝내 자바스크립트를 제대로 이해하지 못하고 넘어가는 경우가 비일비재하다.

## 목표

자바스크립트의 놀랍거나 불만스런 점들을 마주할 때마다 자신의 블랙리스트에 추가하여 금기시한다면(이런 일에 익숙한 사람들이 더러 있다), 자바스크립트란 풍성함의 빈 껍데기에 머무르게 될 것이다.

누군가 "`The Good Parts`"란 유명한 별칭을 달아놓았는데 <sub>[02](#02)</sub>, 부디 독자 여러분들! "좋은 부분"이라기보단 차라리 "쉬운 부분", "안전한 부분", 또는 "불완전한 부분"이라고 하는 편이 더 정확할 것이다.

"`You Don’t Know JS`" 시리즈는 정반대의 방향으로 접근한다. 자바스크립트의 모든 것, 그 중 특히 "어려운 부분<sub>`The Tough Part`</sub>"을 심층적으로 이해하고 학습할 것이다!

나는 자바스크립트 개발자들이 정확히 언어가 어떻게, 왜 그렇게 작동하는지 알려 하지 않고, "그냥 이 정도면 됐지" 식으로 대충 이해하고 때우려는 자세를 직접 거론할 것이다. 험한 길을 마주한 상황에서 쉬운 길로 돌아가라는 식의 조언은 절대하지 않을 것이다.

코드가 일단 잘 돌아가니 이유는 모른채 그냥 지나치는건 내 성격상 용납할수없다. 여러분도 그래야 한다. 여러분이 나와 함께 험난한 "가시밭길"을 탐험하면서 자바스크립트가 무엇인지, 자바스크립트로 뭘 할 수 있을지 포괄적으로 배우기 바란다. 이런 지식을 확실히 보유하고 있으면 테크닉, 프레임워크, 금주의 인기 있는 머리글자 따위는 여러분 손바닥 위에서 벗어나지 않을 것이다.

본 시리즈는 자바스크립트에 대해 가장 흔히 오해하고 있거나 잘못 이해하고 있는, 특정한 핵심 언어 요소를 선정하여 아주 깊고 철저하게 파헤친다. 여러분은 이론적으로만 알고 넘어갈 것이 아니라, 실전적으로 "내가 알고 있어야 할" 내용을 분명히 다 알 고 간다는 확신을 갖고 책장을 넘기기 바란다.

아마도 지금 여러분이 알고 있는 자바스크립트는 다른 사람들이 불완전한 이해로 구워낸 단편적인 지식들을 물려받은 정도일 것이다. 이런 자바스크립트는 진정한 자바스크립트의 그림자에 불과하다. 여러분은 지금 자바스크립트를 제대로 알고 있지 못 하지만, 본 시리즈를 열독하면 완벽히 알게 될 것이다. 동료, 선후배 여러분들, 포기하 지 말고 계속 읽기 바란다. 자바스크립트가 여러분의 두뇌를 기다리고 있다.

## 정리하기

자바스크립트는 굉장한 언어다. 다만 적당히 아는 건 쉬워도 완전히(충분히) 다 알기는 어렵다. 헷갈리는 부분이 나오면 개발자들은 대부분 자신의 무지를 탓하기 전에 언어 자체를 비난하곤 한다. 본 시리즈는 이런 나쁜 습관을 바로잡고 이제라도 여러분이 자 바스크립트를 제대로, 깊이 있게 이해할 수 있도록 도와주는 것을 목표로 한다.

Note: 이 책의 예제 코드를 실행하려면 현대적인 자바스크립트 엔진(예: `ES6`)이 필요하다. 구 엔진(`ES6` 이전)에서는 코드가 작동하지 않을 수 있다.

----

##### 01
<sub>자바스크립트의 창시자.1995년 넷스케이프 근무 당시 열흘만에 자바스크립트 언어를 고안했습니다.</sub>

##### 02 
<sub>『더글라스 크락포드의 자바스크립트 핵심 가이드』(한빛미디어, 2008.)의 원서명 『JavaScript: The Good Parts』(O’Reilly, 2008.)를 의미합니다.</sub>