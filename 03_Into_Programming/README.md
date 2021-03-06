# You Don't Know JS: Up & Going
# Chapter 1: Into Programming

*You Don't Know JS* (*YDKJS*) 시리즈에 온 것을 환영한다.

*Up & Going*은 프로그래밍의 몇 가지 기본 개념 -- 물론 JavaScript ( 줄여서 JS )를 배우는 것을 위주로 -- 을 소개하고 이 시리즈의 나머지 타이틀에 접근하고 이해하는 방법에 대해서도 설명한다. 특히 프로그래밍, 또는 JavaScript의 입문자라면 이 책이 *Up & Going* 하고 싶어하는 것을 간략하게 살펴본다.

이 책은 매우 높은 수준에서의 프로그래밍 기본 원칙을 설명한다. 이전에 프로그래밍 경험이 거의 없이 *YDKJS*를 시작하거나, 이 책들을 JavaScript의 관점을 통해서 프로그래밍을 이해하려고 시작하는 이에게 주로 도움이 된다.

1장은 *into programming*을 배우고 익히기 위한 간략한 개요로써 접근해야 한다. 또한 앞으로 다른 많은 환상적인 프로그래밍 소개 자료를 깊게 이해하는데 도움이 된다. 이 장을 통해 배울 것을 권장한다.

일반적인 프로그래밍 기본 사항에 익숙해지면 2장은 JavaScript 프로그래밍에 익숙해 지도록 가이드 해준다. 2장에서는 JavaScript가 무엇인지 소개하지만, 포괄적인 가이드는 아니다. 나머지는 *YDKJS* 에서 볼 수 있다.

이미 JavaScript에 익숙하다면 3장을 먼저 살펴보고 바로 넘어가자!

## 코드

처음부터 시작해 보자.

흔히 소스 코드 또는 코드라고 하는 프로그램은 수행할 작업을 컴퓨터에게 전달하는  특별한 지침의 집합이다. 일반적으로 코드는 텍스트 파일에 저장되며 JavaScript를 사용하면 앞으로 살펴볼 내용들을 브라우저의 개발자 콘솔에 직접 코드를 입력할 수도 있다.  

유효한 형식 및 명령어이 조합에 대한 규칙을 *컴퓨터 언어*라고 하며 *구문*이라고도 하며, 영어와 거의 같은 방식으로 철자를 쓰는 방법과 단어 구두점을 사용하여 유효한 문장을 만드는 방법을 알려주겠다.

### 문

컴퓨터 언어에서 특정 작업을 수행하는 단어, 숫자, 연산자의 집합을 *문*이라고 한다. JavaScript에서의 문은 다음과 같다.

```js
a = b * 2;
```

문자 `a`와 `b`는 무엇이든 저장할 수 있는 상자와 같은 *변수*( "변수" 참고 )라고 부른다. 프로그램에서 변수는 프로그램에서 사용할 값을 가진다. ( 숫자 `42`같은 ) 값 자체를 가리키는 자리 표시라고 생각하자.

그에 반해, 리터럴 값이라고 불리우는 `2`는 변수에 저장되지 않고 혼자 있기 때문에 그 자체로 값이다. 

`=`와 `*` 문자열은 *연산자*( "연산자: 참고 )이다. 값과 변수를 가지고 할당 및 수학적 연산을 수행한다.

JavaScript의 문 대부분은 끝에 세미콜론( ; )을 붙인다.

`a = b * 2;` 문은 컴퓨터에게 변수 `b`에 현재 저장된 값을 가져와서 값 `2`와 곱한 결과를 또 다른 변수인 `a`에 저장하도록 전달한다.

프로그램은 프로그램의 목적을 수행하는 데 필요한 모든 단계를 기술한 많은 문의 모음일 뿐이다.

### 식

문은 하나 이상의 *식*으로 구성된다. 식은 변수 또는 값에 대한 참조이거나 연산자와 결합 된 변수 및 값의 집합이다.

예를들어

----

```js
a = b * 2;
```

이 문에는 4 개의 식이 있다.

* `2`는 리터럴 값 표현식이다.
* `b`는 현재 값에 접근하는 변수 표현식이다.
* `b * 2`는 연산을 의미하는 산술 표현식이다.
* `a = b * 2`는 `b * 2` 표현식의 결과를 변수 `a`에 할당하는 할당 표현식이다. ( 할당에 대해서는 나중에 자세히 설명 함 )

일반적으로 다음과 같이 단독으로 사용되는 식은 식 문이라고도 한다.

```js
b * 2;
```

보통 이런 식 문은 프로그램 실행에 아무런 영향을 미치지 않기 때문에  유용하지 않다. `b`의 값에 접근하여 `2`를 곱한 다음 결과값을 가지고 아무 것도하지 않는다.

보다 일반적인 식 문은 함수 스스로를 호출하는 *함수 호출 표현식* 문( "Function" 참고 ) 이다.

```js
alert( a );
```

### 프로그램 실행

이러한 프로그래밍 문의 집합은 컴퓨터에게 무엇을 요청할까? 프로그램은 실행되어야 한다.

`a = b * 2`와 같은 문은 개발자가 읽고 쓰는 데 도움이되지만 실제로 컴퓨터가 직접 이해할 수있는 형식은 아니다. 따라서 컴퓨터의 특별한 유틸리티 (인터프리터 또는 컴파일러)는 작성한 코드를 컴퓨터가 이해할 수있는 명령으로 변환하는 데 사용된다.

인터프리터를 사용하는 언어의 경우, 이 명령들의 변환이 프로그램이 실행될 때마다 한 줄씩 위에서부터 차례대로 수행되며 보통 코드 인터프리팅이라고 부른다.

컴파일러를 사용하는 언어의 경우 변환은 코드 컴파일 시점에 미리 수행되기 때문에 프로그램이 나중에 실행될 때 실제로 실행되는 것은 이미 컴파일 된 컴퓨터 명령어이다.

일반적으로 자바 스크립트 소스 코드는 실행될 때마다 처리되므로  JavaScript는 인터프리터 언어라고 합니다. 그러나 완전히 정확하지는 않다. JavaScript 엔진은 실제로 프로그램을 즉시 컴파일 한 다음 컴파일 된 코드를 즉시 실행한다.

참고 : JavaScript 컴파일에 대한 자세한 내용은이 시리즈의 Scope & Closures 제목의 처음 두 장을 참조하라.

## 도전하기

이 장에서는 모든 프로그래밍 개념을 간단한 코드 스니펫으로 소개 할 것이며, 모두 JavaScript로 작성할 것이다.

강조하자면 이 장을 읽는 동안 시간을 ​​들여 여러 번 반복해야 할 수도 있다. 코드를 직접 입력하며 이러한 각 개념을 연습해야 한다. 가장 쉬운 방법은 가장 가까운 브라우저 (Firefox, Chrome, IE 등)에서 개발자 도구 콘솔을 여는 것이다.

팁 : 일반적으로 키보드 단축키 또는 메뉴 항목을 사용하여 개발자 콘솔을 시작할 수 있다. 자주 사용하는 브라우저에서 콘솔을 시작하고 사용하는 방법에 대한 자세한 내용은 "Developer Tools Console 마스터 링"(http://blog.teamtreehouse.com/mastering-developer-tools-console)을 참조하라. 한 번에 여러 줄을 콘솔에 입력하려면 `<shift> + <enter>`를 사용하여 다음 줄로 이동하라. `<enter>`를 누르면 콘솔이 방금 입력 한 모든 것을 실행한다.

콘솔에서 코드를 실행하는 프로세스에 익숙해 지자. 먼저, 브라우저에서 빈 탭을 열어보자. 주소 표시 줄에 about : blank를 입력하면 된다. 앞에서 설명한 것과 같이 개발자 콘솔이 열려 있는지 확인하라.

이제 이 코드를 입력하고 실행되는 것을 확인하라.

```js
a = 21;

b = a * 2;

console.log( b );
```

Chrome의 콘솔에 위의 코드를 입력하면 다음과 같은 결과가 나타난다.

<img src="fig1.png" width="500">

어서 해보자. 프로그래밍을 배우는 가장 좋은 방법은 코딩을 시작하는 것이다!

### 출력

위의 코드에서 `console.log (..)`를 사용했다. 그 코드 라인이 무엇을 의미하는지 간단히 살펴 보겠다.

짐작할 수 있겠지만 개발자 콘솔에서 텍스트 (사용자에게 출력)를 인쇄하는 방법이다. 그 문에는 우리가 이해해야 할 두 가지 특징이 있다.

먼저 `log (b)` 부분을 함수 호출이라고 한다. ( "Function"참고 ). `b` 변수를 함수에 건네주고, `b`의 값을 받아서 콘솔에 출력 할 것을 요청한다.

그 다음, `console` 부분은 `log (..)` 메소드가 있는 객체에 대한 참조이다. 객체와 속성은 2 장에서 자세히 다룬다.

출력을 생성하는 또 다른 방법은 `alert (..)` 문을 실행하는 것이다.

```js
alert( b );
```

위의 코드를 실행하면 출력을 콘솔에 인쇄하는 대신 `b` 변수의 내용이있는 "OK" 경고창이 나타난다. `console.log (..)`를 사용하면 브라우저 인터페이스를 방해하지 않고 즉시 많은 값을 출력 할 수 있기 때문에 일반적으로 `alert (..)`을 사용하는 것보다 콘솔에서 프로그램 코딩 및 실행에 대해 배우게 된다.

이 책에서는 `console.log (..)`를 사용하여 출력하겠다.

### 입력

출력에 대해 살펴보는 동안 입력 ( 예 : 사용자로부터 정보 수신 )에 대해 궁금 할 수 있다.

가장 일반적인 방법은 HTML 페이지에서 사용자가 입력 할 수있는 양식 요소 ( 예 : 텍스트 상자 )를 표시 한 다음 JS를 사용하여 해당 값을 프로그램 변수로 읽는 것이다.

그러나 이 책 전체에서 수행 할 작업과 같은 간단한 학습 및 데모 용 입력을 얻는 더 쉬운 방법이 있다. `prompt (..)` 함수를 사용하자.

----

```js
age = prompt( "Please tell me your age:" );

console.log( age );
```

예상대로 `prompt (..)`에 메시지를 전달하면 -이 경우에는 `"Please tell me your age:"`가 팝업으로 출력된다.

이것은 다음과 같다.

<img src="fig2.png" width="500">

"OK"를 클릭하여 텍스트를 입력하면 입력한 값이 age 변수에 저장되고 console.log (..)와 함께 출력된다는 것을 알 수 있다.

<img src="fig3.png" width="500">

기본 프로그래밍 개념을 배우는 동안은 간단하게 하기 위해 이 책의 예제에서는 입력을 사용하지 않을 것이다. 하지만 이제 `prompt(..)`를 사용하는 법을 알았으므로 학습을 위해 예제를 학습할 때 입력을 사용해 볼 수 있다.

## 연산자

연산자는 변수와 값에 대한 작업을 수행하는 방법이다. 이미 두 개의 JavaScript 연산자인 `=`와 `*`를 보았다.

`*` 연산자는 곱셈 연산을 수행한다. 충분히 심플하지 않은가?

`=` 연산자는 할당에 사용된다. 먼저 `=`의 우변에 있는 값을 계산 한 다음 좌변에 지정한 변수 (대상 변수)에 할당한다.

경고 : 이것은 지정을 지정하는 이상한 역순처럼 보일 수 있다. `a = 42` 대신에 순서를 뒤집어서 소스 값이 왼쪽에 있고 목표 변수가 오른쪽에있는 `42 -> a` (JavaScript에서는 유효하지 않다!)와 같은 것을 선호 할 수 있다. 불행히도, `a = 42` 문과 비슷한 유형들은 현대 프로그래밍 언어에서 널리 보급되어 있다. 부자연스럽다고 느낄 경우, 순서를 연습하면서 시간을 들여 익숙해져야 한다.

예를 들어

```js
a = 2;
b = a + 1;
```

여기서는 `a` 변수에 `2` 값을 할당한다. 그런 다음 변수 `a`(여전히 2)의 값을 가져 와서 값 1을 더해 3으로 만든 다음 해당 값을 변수 `b`에 저장한다.

기술적으로 연산자는 아니지만 모든 프로그램에서 키워드 `var`가 필요하다. 변수를 선언 (일명 생성)하는 주요 방법이다. ( "변수"참고 ).

----

변수를 사용하기 전에 변수를 항상 변수명으로 선언해야 한다. 그러나 각각의 스코프 내에서는 한 번만 변수를 선언하면 된다. ( "스코프" 참고 ). 선언한 이후에는 필요할 때마다 여러 번 사용할 수 있다. 

예를들어.

```js
var a = 20;

a = a + 1;
a = a * 2;

console.log( a );	// 42
```

JavaScript에서 가장 자주 사용되는 연산자들 중 일부이다.

* 할당 연산자: `a = 2`에서 `=`.
* 수학 연산자: `a * 3` 과 같이, `+` ( 더하기 ), `-` ( 빼기 ), `*` ( 곱하기 ), `/` ( 나누기 ).
* 복합 할당 연산자: `a += 2`( `a = a + 2`와 같다 )와 같이 `+=`, `-=`, `*=`, `/=`은 수학 연산자와 할당 연산자를 합친 것과 같은 복합 연산자이다.
* 증감 연산자: `a++`( `a = a + 1`과 유사하다 )과 같은 `++`( 증가 ), `--`( 감소 ) 연산자.
* 객체 프로퍼티 접근 연산자: `console.log()`에서의 `.`.
  객체는 프로퍼티라는 특정 위치에 다른 값을 가지는 값이다. `obj.a`는 `a`라는 프로퍼티를 가진 `obj` 객체 값을 의미한다. 프로퍼티는 `obj["a"]`로 접근할 수도 있다. 2장을 참고하자.
* 같음 연산자: `a == b`와 같은 `==`( 느슨한 같음 ), `===`( 엄격한 같음 ), `!=`( 느슨한 다름 ), `!==`( 엄격한 다름 ).
  2장의 "값과 타입"을 참고하자.
* 비교 연산자: `a <= b`처럼 `<`( 작은 ), `>`( 큰 ), `<=`( 작거나 같은 ), `>=`( 크거나 같은 ).
  2장의 "값과 타입"을 참고하자.
* 논리 연산자: `a`*또는* `b`가 참인 경우를 선택하는 `a || b`와 같은 `&&`( and ), `||`( or ).

  이 연산자는 `a` 또는 `b`가 참인 경우와 같이 복합 조건부( "조건" 참고 )를 표현할 때 사용한다.

**참고** 여기서 다루지 않은 연산자에 대한 자세한 내용과 적용 범위는 Mozilla Developer Network ( MDN )의 "Expressions and Operators"(https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)를 참고하자.

----

## 값과 타입

전화기 상점 직원에게 전화기가 얼마인지 물어보면 "구십 구, 구십 구"라고 답한다. 전화기를 구입하기 위해 필요한 (세금을 포함한.) 실제 달러 숫자 값이다. 이 전화기 두 대를 산다면 기본 숫자의 두 배인 199.98 달러를 암산으로 쉽게 알 수 있다.

직원이 다른 유사한 폰을 들고 "무료"라고 할 때는 숫자를 말하지 않지만 $0.00 달러라는 것을 알 수 있다. -- 단어는 "무료"이지만.

충전기가 포함된 가격인지 물어보면 대답은 "네" 또는 "아니오"일 것이다.

이처럼 프로그램에서 값을 표현할 때도 용도에 따라 다른 표기를 선택할 수 있다.

이러한 다양한 값 표현을 프로그래밍 분야에서는 *타입*이라고 한다. JavaScript에는 *프리미티브* 값이라고 하는 내장 타입들이 있다. 

* 수학 연산을 할 때는 `number` 타입을 사용한다.
* 화면에 값( 하나 이상의 문자, 단어, 문장 등)을 출력할 때는 `string` 타입을 사용한다.
* 프로그램에서 판단을 위해 `boolean` 타입(`true` 또는 `false`)을 사용한다.

소스 코드에 직접 포함된 값을 *리터럴*이라고 한다. `string` 리터럴은 쌍따옴표(`"..."`) 또는 홑따옴표(`'...'`)로 감싸서 표기한다. - 선호일 뿐 차이는 없다. `number`, `boolean` 리터럴은 그대로 표기한다. ( 예를 들어 `42`, `true`, 등등 ) 

예를 들어:

```js
"I am a string";
'I am also a string';

42;

true;
false;
```

`string` / `number` / `boolean` 타입 이외에도, 프로그래밍 언어에서는 보통 `array`, `object`, `function` 등을 사용한다. 이 장에서 값과 타입에 대해 더욱 깊이 살펴보겠다.

### 타입 변환

`number` 타입을 화면에 출력해야 하는 경우라면 값을 `string` 타입으로 변환해야 하며, JavaScript에서는 이러한 변환을 "강제 변환"이라고 한다. 마찬가지로 일련의 숫자를 상거래 페이지의 폼<sub>form</sub>에 입력한다면, 입력된 값은 `string` 타입이지만 값을 가지고 수학적인 연산을 수행해야 한다면 `number` 타입으로 변환해야 한다.

JavaScript는 타입 간에 강제 변환을 위한 몇 가지 다양한 기능을 제공한다.

예를 들어.

```js
var a = "42";
var b = Number( a );

console.log( a );  // "42"
console.log( b );  // 42
```

보다시피 내장 함수인 `Number(..)`를 사용하면 어떤 타입이던지 명시적으로 `number` 타입으로 강제 변환을 할 수 있다. 이런 변환은 아주 간단한 값에 유용하다.

하지만 암시적 강제 변환이 필요한 같은 타입이 아닌 두 값을 비교하려 할 때에 논쟁의 여지가 있다.

문자열 `99.99`와 숫자 `99.99`를 비교할 때 대부분은 같다라고 생각할 것이다. 하지만 정확히 같지는 않지 않은가. 이것은 두 가지 다른 표현, 즉 두 가지 *타입*으로서 동일한 값이다. 단순히 느슨하게<sub>loosely</sub> 비슷하다 정도로 말할 수 있지 않을까.

이런 일반적인 상황에서 편의를 돕기 위해 JavaScript는 때때로 두 값을 일치하는 타입으로 암묵적인 강제 변환을 한다.

따라서 `"99.99" == 99.99`처럼 `==`를 사용하여 느슨한 비교를 하는 경우, JavaScript는 좌변의 `"99.99"` 문자열을 `99.99`로 변환한다. 비교는 `99.99 == 99.99`가 되어 참이된다.

암시적 강제 변환은 편의 기능으로 고안되었지만, 강제 변환이 이루어지는 규칙을 충분히 숙지하지 않은 경우 혼란에 빠질 수가 있다. 대부분의 JS 개발자는 강제 변환을 충분히 숙지하지 못해서 혼란을 느끼고 예기치 않은 버그를 만들어내 프로그램을 망가뜨린다. 그렇기 때문에 암묵적 강제 변환은 가급적 피해야 한다. 심지어 언어 디자인의 결함이라고도 한다.

하지만 암묵적인 강제 변환은 충분히 숙지할 수 있는 매커니즘이며 JavaScript 전문가라면 필히 숙지해야 한다. 암묵적인 강제 변환의 규칙을 숙지하면 혼란을 피할 수 있을 뿐 아니라 실제로 더 좋은 프로그램을 만들 수 있다! 충분히 가치가 있는 학습 대상이다.

참고: 강제 변환에 대한 더 자세한 내용은 이 책의 2장과 이 시리즈의 *타입과 문법* 4장을 참고하자.

## 코드 주석

전화기 매장 직원은 새로 출시된 전화기의 기능이나 회사에서 내려주는 계획을 메모해 둘 수 있다 이 메모는 직원만 읽을 수 있고 고객은 읽을 수 없다. 그렇지만 이 메모는 직원이 고객에게 말해야 하는 것을 문서화함으로써 자신의 업무를 더 잘 수행할 수 있게 해준다.

코드 작성에서 배울 수있는 가장 중요한 교훈 중 하나는 코드 작성이 컴퓨터만을 대상으로 하지 않는다는 것이다. 모든 코드는 컴파일러 뿐 아니라 개발자를 위한 것이기도 하다.

컴퓨터는 컴파일에게 전달되는 기계 코드, 일련의 이진 0과 1만을 신경쓴다. 개발자는 0과 1만으로도 모든 프로그램을 작성할 수 있다. 프로그램을 작성하는 방법에 대한 선택은 개발자 본인 뿐 아니라 다른 팀원에게도 중요하다.

올바르게 작동하는 프로그램을 작성하는 것뿐만 아니라 검토할 때 의미가있는 프로그램을 작성해야한다. 변수("변수 참고)와 함수("함수" 참고)에 좋은 이름을 할당하는 것에 더 많은 시간을 쏟을 수도 있다.

그러나 또 다른 중요한 부분은 코드 주석이다. 이것들은 순수하게 사람에게 설명하기 위해 삽입되는 텍스트이다. 인터프리터 / 컴파일러는 항상 이러한 주석을 무시한다.

주석 처리된 코드를 작성하는 것에 대해 많은 의견이 있다. 절대적으로 옳은 규칙은 실제로 정의 할 수 없다. 그러나 일부 의견과 가이드 라인은 매우 유용하다.

* 주석이 없는 코드는 차선책이다.
* (코드 할 줄에 한 줄씩 같은)너무 많은 주석은 코드가 잘못 작성되었음을 나타낸다.
* 주석은 *무엇*이 아니라 *왜*를 기술해야 한다. 또는 혼란스러운 코드의 *어떻게*를 기술할 수도 있다.

JavaScript에는 한 줄 주석과 여러 줄 주석이라는 두 가지 유형의 주석이 있다.

예:

```js
// This is a single-line comment

/* But this is
       a multiline
             comment.
                      */
```

`//` 한 줄 주석은 단일 문장 바로 위에 주석을 달거나 줄 끝 부분에 주석을 넣을 때 적절하다. `//` 뒤에 오는 줄의 모든 내용은 줄 끝까지의 주석으로 처리된다. (컴파일러에게 무시됩니다). 한 줄 주석에 작성할 수있는 것에는 제한이 없습니다.

예:

```js
var a = 42;		// 42 is the meaning of life
```

`/ * .. * /` 여러 줄 주석은 주석에 여러 줄의 설명을 추가할 때 적절하다.

다음은 여러 줄 주석의 일반적인 사용법이다.

```js
/* The following value is used because
   it has been shown that it answers
   every question in the universe. */
var a = 42;
```

`*/` 부분에서 종료되기 때문에 줄의 중간 또는 아무 곳에나 작성할 수 있다.

```js
var a = /* arbitrary value */ 42;

console.log( a );	// 42
```

여러 줄 주석에 추가할 수 없는 유일한 문자는 주석을 끝내기 위해 사용되는 `*/` 뿐이다.

주석을 작성하는 습관과 함께 프로그래밍을 배우는 것을 권장한다. 이 장의 나머지 부분들에 추가되어 있는 주석들을 똑같이 베끼는 것도 좋다. 나를 믿어라. 당신의 코드를 읽는 사람들이 고마워 할 것이다.

## 변수

대부분의 유용한 프로그램은 프로그램 진행 과정에서 변경 될 때마다 가치를 추적해야하며 프로그램의 의도 된 작업이 요구하는 다양한 작업을 수행해야합니다.

프로그램에서이 변수를 사용하는 가장 쉬운 방법은 변수라는 심볼 컨테이너에 값을 할당하는 것입니다.이 컨테이너의 값은 필요에 따라 시간에 따라 달라질 수 있습니다.

일부 프로그래밍 언어에서는 숫자 또는 문자열과 같은 특정 유형의 값을 보유 할 변수 (컨테이너)를 선언합니다. 정적 유형 지정 (유형 적용이라고도 함)은 일반적으로 의도하지 않은 값 변환을 방지하여 프로그램 정확성에 대한 이점으로 인용됩니다.

다른 언어는 변수 대신 값의 유형을 강조합니다. 동적 유형 지정이라고도하는 약한 유형 지정을 사용하면 변수가 언제든지 모든 유형의 값을 보유 할 수 있습니다. 일반적으로 프로그램의 논리 흐름에서 특정 순간에 값이 취할 수있는 형식 형식에 상관없이 단일 변수가 값을 나타낼 수 있으므로 프로그램 유연성을위한 이점으로 인용됩니다.

JavaScript는 후자의 방식 인 동적 타이핑을 사용합니다. 즉, 변수는 유형 적용없이 모든 유형의 값을 보유 할 수 있습니다.

앞서 언급했듯이 우리는 var 문을 사용하여 변수를 선언합니다. 선언에 다른 유형 정보가 없다는 것을 알 수 있습니다. 이 간단한 프로그램을 생각해보십시오 :

```js
var amount = 99.99;

amount = amount * 2;

console.log( amount );		// 199.98

// convert `amount` to a string, and
// add "$" on the beginning
amount = "$" + String( amount );

console.log( amount );		// "$199.98"
```

금액 변수는 99.99를 보유하기 시작한 다음 금액 * 2 (199.98)의 수 결과를 보유합니다.

첫 번째 console.log (..) 명령은 숫자 값을 암시 적으로 강제로 인쇄하여 문자열을 출력해야합니다.

그런 다음 명령문 amount = "$"+ String (amount)은 명시 적으로 199.98 값을 문자열로 강제 변환하고 처음에 "$"문자를 추가합니다. 이 시점에서 amount는 이제 문자열 값 "$ 199.98"을 보유하므로 두 번째 console.log (..) 문은이를 인쇄하기 위해 강제 변환 할 필요가 없습니다.

JavaScript 개발자는 99.99, 199.98 및 "$ 199.98"값 각각에 대해 금액 변수를 사용할 수있는 유연성에 주목합니다. 정적 유형의 애호가는 금액 유형이 다르므로 amountStr과 같은 별도의 변수를 사용하여 값의 최종 "$ 199.98"표현을 유지하는 것을 선호합니다.

어느 쪽이든, 당신은 금액이 프로그램의 과정에서 바뀌는 실행 가치를 지니고 있음을 알 수 있습니다. 변수의 주요 목적 : 프로그램 상태 관리.

즉, 상태는 프로그램이 실행될 때 값의 변경을 추적합니다.

변수의 또 다른 일반적인 용도는 값 설정을 중앙 집중화하는 것입니다. 변수를 값으로 선언하고 해당 값이 프로그램 전체에서 변경되지 않도록하려는 경우 더 일반적으로 상수라고합니다.

이러한 상수는 종종 프로그램 상단에 선언되므로 필요한 경우 한 자리에서 값을 변경하는 것이 편리합니다. 일반적으로 상수로 사용되는 JavaScript 변수는 대문자로 표시되며 여러 단어 사이에 _이 붙습니다.

다음은 바보 같은 예입니다.

```js
var TAX_RATE = 0.08;	// 8% sales tax

var amount = 99.99;

amount = amount * 2;

amount = amount + (amount * TAX_RATE);

console.log( amount );				// 215.9784
console.log( amount.toFixed( 2 ) );	// "215.98"
```

참고 : console.log (..)가 콘솔 값에서 객체 속성으로 액세스되는 함수 로그 (..)와 어떻게 비슷한지 toFixed (..)는 숫자 값에서 액세스 할 수있는 함수입니다. 자바 스크립트 숫자는 자동으로 달러 형식으로 지정되지 않습니다. 엔진은 의도가 무엇인지 알지 못하며 통화 유형이 없습니다. toFixed (..)는 소수점 이하 자리수를 지정하고, 필요에 따라 문자열을 생성합니다.

TAX_RATE 변수는 규칙에 의해서만 일정합니다 -이 프로그램에서 변경되지 않도록 특별한 것은 없습니다. 그러나 도시에서 판매 세율을 9 %로 인상하면 프로그램 전체에 0.08의 값이 발생하는 것을 많이 발견하지 않고 TAX_RATE 할당 값을 0.09로 설정하여 프로그램을 쉽게 업데이트 할 수 있습니다. .

이 글을 쓸 당시의 최신 버전의 JavaScript (일반적으로 "ES6")에는 var 대신 const를 사용하여 상수를 선언하는 새로운 방법이 포함되어 있습니다.

```js
// as of ES6:
const TAX_RATE = 0.08;

var amount = 99.99;

// ..
```

상수는 변경되지 않은 값을 갖는 변수와 마찬가지로 유용합니다. 단, 상수는 초기 설정 이후 실수로 다른 값을 변경하는 것을 방지합니다. 첫 번째 선언 다음에 TAX_RATE에 다른 값을 지정하려고하면 프로그램이 변경을 거부합니다 (엄격 모드에서는 오류와 함께 실패합니다 - 2 장의 "엄격 모드"참조).

그건 그렇고, 실수에 대한 그런 종류의 "보호"는 정적 타이핑 유형 강제와 비슷하므로 다른 언어의 정적 유형이 왜 매력적인지 알 수 있습니다!

참고 : 변수에서 다른 값을 프로그램에서 사용하는 방법에 대한 자세한 내용은이 연재의 유형 및 문법 제목을 참조하십시오.

## Blocks

전화 상점 직원은 새 전화를 구입할 때 일련의 단계를 수행하여 결제를 완료해야합니다.

마찬가지로, 코드에서 일련의 문장을 그룹화해야 할 때가 많습니다. JavaScript에서 블록은 중괄호 쌍 ({}} 안에 하나 이상의 명령문을 래핑하여 정의됩니다. 중히 여기다:

```js
var amount = 99.99;

// a general block
{
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```

이러한 종류의 독립 실행 형 {..} 일반 블록은 유효하지만 JS 프로그램에서 일반적으로 볼 수있는 것은 아닙니다. 일반적으로 블록은 if 문 ( "조건부"참조) 또는 루프 ( "루프"참조)와 같은 다른 제어 문에 첨부됩니다. 예 :

```js
var amount = 99.99;

// is amount big enough?
if (amount > 10) {			// <-- block attached to `if`
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```

다음 절의 if 문에 대해 설명하겠습니다. 그러나 볼 수 있듯이 두 개의 명령문이있는 {..} 블록은 if (amount> 10)에 첨부됩니다. 조건부가 통과하는 경우에만 블록 내부의 명령문이 처리됩니다.

주 : console.log (amount)와 같은 대부분의 다른 명령문과는 달리, 블록 명령문은 결론을 내리기 위해 세미콜론 (;)이 필요하지 않습니다.

## Conditionals

"9.99 달러에 구입하신 화면 보호 장치를 추가하고 싶습니까?" 도움이되는 전화 상점 직원이 귀하에게 결정을 요청했습니다. 그리고 그 질문에 대답하기 위해 지갑이나 은행 계좌의 현재 상태를 먼저 확인해야 할 수도 있습니다. 그러나 분명히 이것은 단순한 "예 또는 아니오"질문 일뿐입니다.

프로그램에서 조건부 (aka decision)를 표현할 수있는 방법은 아주 많이 있습니다.

가장 일반적인 것은 if 문입니다. 근본적으로 말하면, "이 조건이 사실이라면, 다음을 수행하십시오 ...". 예 :

```js
var bank_balance = 302.13;
var amount = 99.99;

if (amount < bank_balance) {
	console.log( "I want to buy this phone!" );
}
```

if 문은 true 또는 false로 처리 할 수있는 괄호 () 사이에있는 표현식을 필요로합니다. 이 프로그램에서 표현 금액 <bank_balance를 제공했습니다. 실제로 bank_balance 변수의 양에 따라 true 또는 false로 평가됩니다.

else 절로 불리는 조건이 참이 아니면 대안을 제공 할 수도 있습니다. 중히 여기다:

```js
const ACCESSORY_PRICE = 9.99;

var bank_balance = 302.13;
var amount = 99.99;

amount = amount * 2;

// can we afford the extra purchase?
if ( amount < bank_balance ) {
	console.log( "I'll take the accessory!" );
	amount = amount + ACCESSORY_PRICE;
}
// otherwise:
else {
	console.log( "No, thanks." );
}
```

여기에 금액 <bank_balance가 true이면 "액세서리를 가져 가겠습니다!"라는 메시지가 인쇄됩니다. 우리 금액 변수에 9.99를 추가하십시오. 그렇지 않으면 else 절은 우리가 정중하게 "아니, 감사합니다."라고 대답 할 것이라고 말합니다. 금액을 변경하지 마십시오.

앞서 "Values ​​& Types"에서 논의했듯이, 이미 예상 된 유형이 아닌 값은 종종 해당 유형으로 강제 변환됩니다. if 문은 부울을 기대하지만, 이미 부울이 아닌 무언가를 전달하면 강제 변환이 발생합니다.

JavaScript는 부울로 강요 될 때 false가 될 때 "0"및 ""와 같은 값을 포함하기 때문에 "거짓"으로 간주되는 특정 값의 목록을 정의합니다. "거짓"목록에없는 다른 값은 자동으로 "진실"입니다. 진리가 진리가 될 때 진리가됩니다. 진리 값에는 99.99와 "무료"같은 것이 포함됩니다. 자세한 내용은 2 장의 "Truthy & Falsy"를 참조하십시오.

조건문은 if 이외의 다른 형식으로 존재합니다. 예를 들어, switch 문은 일련의 if..else 문에 대한 줄임말로 사용할 수 있습니다 (2 장 참조). 루프 ( "루프"참조)는 조건을 사용하여 루프를 계속 진행할지 또는 중지할지 결정합니다.

참고 : 조건문의 테스트 표현식에서 암시 적으로 발생할 수있는 강제 변환에 대한 자세한 내용은이 시리즈의 유형 및 문법 제목 4 장을 참조하십시오.

## Loops

바쁜 시간에는 전화 상점 직원과 통화해야하는 고객을위한 대기자 명단이 있습니다. 그 목록에 여전히 사람들이 있지만, 그녀는 단지 다음 고객에게 계속해서 봉사해야합니다.

특정 조건이 실패 할 때까지 일련의 작업을 반복합니다. 즉, 조건이 유지되는 동안 만 반복하는 것은 프로그래밍 루프의 작업입니다. 루프는 다른 형식을 취할 수 있지만이 기본 동작을 모두 만족시킵니다.

루프는 테스트 조건과 블록 (일반적으로 {..}와 같이)을 포함합니다. 루프 블록이 실행될 때마다이를 반복이라고합니다.

예를 들어 while 루프 및 do..while 루프 양식은 조건이 더 이상 true가 아닌 것으로 평가 될 때까지 문 블록을 반복하는 개념을 보여줍니다.

```js
while (numOfCustomers > 0) {
	console.log( "How may I help you?" );

	// help the customer...

	numOfCustomers = numOfCustomers - 1;
}

// versus:

do {
	console.log( "How may I help you?" );

	// help the customer...

	numOfCustomers = numOfCustomers - 1;
} while (numOfCustomers > 0);
```

이러한 루프 간의 유일한 차이점은 조건부가 첫 번째 반복 전에 (while) 또는 첫 번째 반복 후에 (do..while) 테스트되는지 여부입니다.

두 가지 형태 중 하나라도 조건부 테스트가 거짓이면 다음 반복이 실행되지 않습니다. 즉, 조건이 처음 false이면 while 루프는 실행되지 않지만 do..while 루프는 처음 실행됩니다.

때로는 0에서 9 (10 개의 숫자)와 같은 특정 숫자 세트를 계산하는 의도 된 목적을 위해 루핑합니다. 당신은 값 0에서 i와 같은 루프 반복 변수를 설정하고 반복 할 때마다 1 씩 증가시킴으로써 그렇게 할 수 있습니다.

경고 : 다양한 역사적 이유로 프로그래밍 언어는 거의 항상 0부터 시작하여 0부터 시작한다는 것을 의미하는 0부터 시작하는 방식으로 계산합니다. 그 사고 방식에 익숙하지 않은 경우 처음에는 상당히 혼란 스러울 수 있습니다. 0으로 시작하는 계산을 연습 할 시간을 가지십시오.

루프 내에서 묵시적인 if 문이있는 것처럼 조건은 각 반복에서 테스트됩니다.

우리는 JavaScript의 break 문을 사용하여 루프를 멈출 수 있습니다. 또한 깨지기 쉬운 메커니즘없이 영원히 돌아갈 수있는 루프를 만드는 것은 너무나 쉽습니다.

설명해 보겠습니다.

```js
var i = 0;

// a `while..true` loop would run forever, right?
while (true) {
	// stop the loop?
	if ((i <= 9) === false) {
		break;
	}

	console.log( i );
	i = i + 1;
}
// 0 1 2 3 4 5 6 7 8 9
```

경고 : 이것은 반드시 루프에 사용하려는 실제적인 형식은 아닙니다. 여기서는 설명을 목적으로 제시된 것입니다.

잠시 동안 (또는 do..while) 수동으로 작업을 수행 할 수 있지만 그 목적을 위해 for 루프라는 또 다른 구문 형식이 있습니다.

```js
for (var i = 0; i <= 9; i = i + 1) {
	console.log( i );
}
// 0 1 2 3 4 5 6 7 8 9
```

보시다시피, 두 경우 모두 조건식 i <= 9는 두 루프 양식의 처음 10 번의 반복 (i는 값 0에서 9까지)에 적용되지만 값 10이면 거짓이됩니다.

for 루프에는 초기화 절 (var i = 0), 조건부 테스트 절 (i <= 9) 및 업데이트 절 (i = i + 1)의 세 가지 절이 있습니다. 따라서 루프 반복을 통해 셀 수 있다면 더 이해하기 쉽고 더 쉽게 작성할 수 있습니다.

묵시적 조건 테스트는 모든 속성이 처리되었는지 여부와 같은 객체의 속성 (2 장 참조)과 같이 특정 값을 반복하는 다른 특수한 루프 양식이 있습니다. "조건이 실패 할 때까지 루프"개념은 루프의 형식에 관계없이 유지됩니다.

## Functions

전화 상점 직원은 아마도 세금 및 최종 구매 금액을 계산하기 위해 계산기를 들고 다니지 않습니다. 그것은 한 번 정의하고 반복해서 사용해야하는 작업입니다. 확률은 회사에 "기능"이 내장 된 계산대 (컴퓨터, 태블릿 등)가 있습니다.

비슷하게, 당신의 프로그램은 코드의 작업을 반복적으로 반복적으로 반복하는 대신 재사용 가능한 부분으로 분해하려고합니다. 이를 수행하는 방법은 함수를 정의하는 것입니다.

함수는 일반적으로 이름으로 "호출"할 수있는 코드의 명명 된 섹션이며 그 안에있는 코드는 매번 실행됩니다. 중히 여기다:

```js
function printAmount() {
	console.log( amount.toFixed( 2 ) );
}

var amount = 99.99;

printAmount(); // "99.99"

amount = amount * 2;

printAmount(); // "199.98"
```

함수는 선택적으로 인수 (일명 매개 변수) - 전달한 값을 취할 수 있습니다. 또한 선택적으로 값을 반환 할 수도 있습니다.

```js
function printAmount(amt) {
	console.log( amt.toFixed( 2 ) );
}

function formatAmount() {
	return "$" + amount.toFixed( 2 );
}

var amount = 99.99;

printAmount( amount * 2 );		// "199.98"

amount = formatAmount();
console.log( amount );			// "$99.99"
```

printAmount (..) 함수는 amt라고 부르는 매개 변수를 취한다. formatAmount () 함수는 값을 반환합니다. 물론 동일한 기능에서 두 기술을 결합 할 수도 있습니다.

함수는 여러 번 호출 할 계획 인 코드에 자주 사용되지만 한 번만 호출 할 계획이라 할지라도 관련 코드 비트를 명명 된 컬렉션으로 구성하는 데 유용 할 수 있습니다.

중히 여기다:

```js
const TAX_RATE = 0.08;

function calculateFinalPurchaseAmount(amt) {
	// calculate the new amount with the tax
	amt = amt + (amt * TAX_RATE);

	// return the new amount
	return amt;
}

var amount = 99.99;

amount = calculateFinalPurchaseAmount( amount );

console.log( amount.toFixed( 2 ) );		// "107.99"
```

calculateFinalPurchaseAmount (..)는 한 번만 호출되지만 동작을 별도의 명명 된 함수로 구성하면 로직을 사용하는 코드 (amount = calculateFinal ... 문)가보다 명확 해집니다. 기능에 더 많은 진술이 포함되어 있다면 이점이 훨씬 더 분명해질 것입니다.

### Scope

전화 상점 직원에게 매장에서 판매하지 않는 전화 모델을 요청하면 원하는 전화를 판매 할 수 없습니다. 그녀는 매장의 인벤토리에있는 전화에만 액세스 할 수 있습니다. 찾고있는 전화를 찾을 수 있는지 확인하려면 다른 상점을 방문해야합니다.

프로그래밍에는이 개념을위한 용어 (범위 : 기술적으로 어휘 범위)가 있습니다. JavaScript에서 각 함수는 자체 범위를 가져옵니다. 범위는 기본적으로 변수의 모음 일뿐 아니라 변수가 이름을 통해 액세스되는 방법에 대한 규칙입니다. 해당 함수 내부의 코드 만 해당 함수의 범위 변수에 액세스 할 수 있습니다.

변수 이름은 동일한 범위 내에서 고유해야합니다. 서로 다른 변수가 두 개씩 나란히있을 수 없습니다. 그러나 동일한 변수 이름이 다른 범위에 나타날 수 있습니다.

```js
function one() {
	// this `a` only belongs to the `one()` function
	var a = 1;
	console.log( a );
}

function two() {
	// this `a` only belongs to the `two()` function
	var a = 2;
	console.log( a );
}

one();		// 1
two();		// 2
```

또한, 생일 파티의 광대가 다른 풍선 안에 하나의 풍선을 날려 보내는 것처럼 범위를 다른 범위 안에 중첩시킬 수 있습니다. 하나의 범위가 다른 범위 안에 중첩되어 있으면 가장 안쪽의 범위 안에있는 코드는 두 범위 중 하나의 변수에 액세스 할 수 있습니다.

중히 여기다:

```js
function outer() {
	var a = 1;

	function inner() {
		var b = 2;

		// we can access both `a` and `b` here
		console.log( a + b );	// 3
	}

	inner();

	// we can only access `a` here
	console.log( a );			// 1
}

outer();
```

어휘 범위 규칙은 하나의 범위에있는 코드가 그 범위 또는 그 범위 밖에있는 변수에 액세스 할 수 있다고 말합니다.

따라서 inner () 함수 내부의 코드는 변수 a와 b 모두에 액세스 할 수 있지만 outer ()의 코드는 a에만 액세스 할 수 있습니다. 변수는 inner () 내부에만 있으므로 b에 액세스 할 수 없습니다.

이전의 코드 스 니펫을 상기 해보십시오.

```js
const TAX_RATE = 0.08;

function calculateFinalPurchaseAmount(amt) {
	// calculate the new amount with the tax
	amt = amt + (amt * TAX_RATE);

	// return the new amount
	return amt;
}
```

TAX_RATE 상수 (변수)는 calculateFinalPurchaseAmount (..) 함수 내부에서 액세스 할 수 있습니다. 어휘 범위가 있기 때문에 전달하지 않았습니다.

참고 : 어휘 범위에 대한 자세한 내용은이 시리즈의 범위 및 종결 제목의 처음 세 장을 참조하십시오.

## Practice

학습 프로그래밍 연습에는 절대적으로 대안이 없습니다. 내 부분에 명확한 글을 쓰지 않아도 당신을 프로그래머로 만들 수 있습니다.

이를 염두에두고이 장에서 배웠던 몇 가지 개념을 연습 해 봅시다. 나는 "요구 사항"을 줄 것이고 당신은 그것을 먼저 시도 할 것이다. 그런 다음 아래 코드 목록을 참조하여 내가 어떻게 접근했는지 확인하십시오.

전화 구매 총액을 계산하는 프로그램을 작성하십시오. 당신은 당신의 은행 계좌에서 돈이 떨어질 때까지 전화 (힌트 : 루프!)를 계속 구매할 것입니다. 구매 금액이 정신력 지출 기준 액 이하인 경우 각 전화에 대한 액세서리도 구매하게됩니다.
구매 금액을 계산 한 후 세금을 더한 다음 계산 된 구매 금액을 인쇄하여 올바르게 형식화하십시오.
마지막으로 금액을 은행 계좌 잔액과 비교하여 지불 할 여유가 있는지 여부를 확인하십시오.
'세율', '전화 가격', '액세서리 가격'및 '지출 한도'에 대한 상수 및 '은행 계좌 잔고'에 대한 변수를 설정해야합니다.
세금을 계산하고 "$"로 소수점 이하 두 자리로 반올림하여 가격을 형식화하는 함수를 정의해야합니다.
보너스 챌린지 :이 프로그램에 입력을 통합하십시오. 아마도 앞에서 "입력"에서 설명한 프롬프트 (..)를 사용하십시오. 예를 들어 사용자에게 은행 계좌 잔액을 묻는 메시지를 표시 할 수 있습니다. 재미 있고 독창적이십시오!
알았어. 시도 해봐. 직접 코드 목록을 볼 때까지 내 코드 목록을 엿보지 마십시오!

참고 :이 책은 JavaScript 책이므로 JavaScript로 연습 문제를 해결할 것입니다. 그러나 좀 더 편하게 느끼면 다른 언어로도 할 수 있습니다.

다음은이 연습을위한 JavaScript 솔루션입니다.

```js
const SPENDING_THRESHOLD = 200;
const TAX_RATE = 0.08;
const PHONE_PRICE = 99.99;
const ACCESSORY_PRICE = 9.99;

var bank_balance = 303.91;
var amount = 0;

function calculateTax(amount) {
	return amount * TAX_RATE;
}

function formatAmount(amount) {
	return "$" + amount.toFixed( 2 );
}

// keep buying phones while you still have money
while (amount < bank_balance) {
	// buy a new phone!
	amount = amount + PHONE_PRICE;

	// can we afford the accessory?
	if (amount < SPENDING_THRESHOLD) {
		amount = amount + ACCESSORY_PRICE;
	}
}

// don't forget to pay the government, too
amount = amount + calculateTax( amount );

console.log(
	"Your purchase: " + formatAmount( amount )
);
// Your purchase: $334.76

// can you actually afford this purchase?
if (amount > bank_balance) {
	console.log(
		"You can't afford this purchase. :("
	);
}
// You can't afford this purchase. :(
```

참고 :이 JavaScript 프로그램을 실행하는 가장 간단한 방법은 가장 가까운 브라우저의 개발자 콘솔에 JavaScript 프로그램을 입력하는 것입니다.

어떻게 지냈니? 내 코드를 본 적이 있으므로 이제 다시 시도해도 좋을 것입니다. 그리고 프로그램이 다른 값으로 실행되는 방법을보기 위해 상수의 일부를 변경하면서 놀아보십시오.

## Review

학습 프로그래밍은 복잡하고 압도적 인 과정 일 필요는 없습니다. 머리를 감싸는 데 필요한 몇 가지 기본 개념이 있습니다.

이들은 빌딩 블록과 같은 역할을합니다. 키가 큰 타워를 만들려면 먼저 블록 맨 위에 블록을 올려 놓습니다. 프로그래밍에도 동일하게 적용됩니다. 다음은 필수 프로그래밍 빌딩 블록 중 일부입니다.

값에 대한 작업을 수행하려면 연산자가 필요합니다.
숫자에 대한 수학이나 문자열을 사용한 출력과 같은 여러 종류의 작업을 수행하려면 값과 유형이 필요합니다.
프로그램을 실행하는 동안 데이터 (일명 상태)를 저장하기위한 변수가 필요합니다.
의사 결정을하기 위해서는 if 문과 같은 조건문이 필요합니다.
조건이 참이 될 때까지 작업을 반복하려면 루프가 필요합니다.
논리적이고 재사용 가능한 청크로 코드를 구성하는 기능이 필요합니다.
코드 주석은보다 이해하기 쉬운 코드를 작성하는 효과적인 방법 중 하나이며, 문제가있는 경우 나중에 프로그램을 이해하고 유지 관리하고 수정하는 것이 더 쉽습니다.

마지막으로, 연습의 힘을 무시하지 마십시오. 코드 작성 방법을 배우는 가장 좋은 방법은 코드를 작성하는 것입니다.

코드 작성 방법을 익히기에 매우 흥분됩니다. 그것을 지키십시오. 다른 초보자 프로그래밍 리소스 (책, 블로그, 온라인 교육 등)를 확인하는 것을 잊지 마십시오. 이 장과이 책은 훌륭한 시작이지만 간단한 소개 일뿐입니다.

다음 장에서는이 장의 많은 개념을 검토 할 것이지만, 나머지 JavaScript 시리즈에서는 자세히 다루는 주요 주제를 대부분 강조 표시하는 JavaScript에 대한 구체적인 관점에서 검토 할 것입니다.