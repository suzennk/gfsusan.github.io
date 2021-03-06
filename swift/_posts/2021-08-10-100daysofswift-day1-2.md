---
layout: post
title: Swift 기초 | 정수와 문자열 타입
description: >
   정수와 문자열에 대해서 알아보자.
tags: [swift]
comments: true
related_posts:
  - swift/_posts/2021-08-10-100daysofswift-day1-1.md
  - swift/_posts/2021-08-10-100daysofswift-day1-3.md
---

Swift는 type-safe 언어이다. 즉, 모든 변수가 하나의 명시된 타입이 지정되어야 한다는 의미이다. Xcode가 생성해준 `str` 변수는 "Hello, playround"라는 철자의 문자열을 저장하기 때문에 Swift는 이 변수에 `String`이라는 타입을 지정한다.

만약 누군가의 나이를 저장하고 싶다면 다음과 같이 변수를 생성할 수 있다.

~~~swift
var age = 25
~~~

이는 정수를 저장하기 때문에, Swift는 'integer'의 줄인 버전인 `Int` 타입을 지정한다.

큰 수를 저장하고 싶다면, Swift에서는 천 단위를 나타내는 언더바(_)를 사용할 수 있다. 이 언더바는 숫자를 변경하지 않고 더 쉽게 읽을 수 있도록 해준다.

~~~swift
var population = 8_000_000
~~~

문자열과 정수는 서로 다른 타입이며, 혼용될 수 없다. 따라서 `str`의 값을 "Goodbye"로 변경하는 것은 허용되지만, 38로는 변경할 수 없다. 왜냐 하면 38은 `String`이 아닌 `Int` 타입이기 때문이다.

## Swift는 왜 type-safe 언어일까?

Swift에서는 문자열과 정수 뿐만아니라 여러가지 다른 타입의 데이터 타입으로 변수를 생성할 수 있다. 여러분이 변수를 생성하면 Swift는 대입된 데이터가 어떤 타입인지를 바탕으로 데이터 타입을 지정하고, 그 순간부터 해당 변수는 지정된 특정 데이터 타입만을 가진다.

예를 들어, 다음 코드는 값이 42인 `meaningOfLife`라는 변수를 생성한다.

~~~swift
var meaningOfLife = 42
~~~

우리는 `meaningOfLife`라는 변수에 42라는 초기값을 지정했기 때문에 Swift는 해당 변수는 정수 타입으로 지정할 것이다. 변수이기 때문에 언제든지 필요할 때 값을 변경할 수 있지만 그것의 데이터 타입은 변경할 수 없다. 언제나 정수여아만 한다.

이는 앱을 빌드할 때 굉장히 도움이 된다. Swift는 우리가 데이터를 가지고 실수를 하지 않게끔 보장해준다. 예를 들어 다음과 같은 코드는 작성할 수 없다.

~~~swift
meaningOfLife = "Forty two"
~~~

이는 정수형 변수에 문자열 타입을 대입하려고 시도한다. 그러나 이는 Swift 컴파일러에 의해서 허용되지 않는다. 물론 이와 같이 명백한 실수는 거의 하지 않겠지만 이런 type-safe한 Swift의 특징은 Swift 코드를 작성할 때 개발자가 실수하지 않도록 도와 준다.

다음을 생각해보자. 막 변수를 생성하고, 그 변수의 타입을 바꾸는 시도를 했다. 이는 당연히 실패할 것이다. 하지만 여러분의 프로그램의 규모와 복잡성이 커질 수록, 모든 변수의 타입을 머릿속에 떠올리는 것은 불가능할 것이다. 따라서 이 부분을 Swift에게 맡기는 것이다.
