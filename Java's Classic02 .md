2021/02/27 Java의 정석 

p 27 ~ 35

2. 변수의 타입
문자와 숫자, 정수와 실수로 나뉜다.
논리형 boolean 문자형 char 정수형 byte, short, int, long 실수형 float, double 가 있다.
기본형과 참조형
기본형은 실제 값을 저장하고
참조형은 값이 저장되어 있는 주소를 값으로 갖는다.
참조형 8개의 기본형을 제외한 나머지 타입들..

참조변수를 선언하는 방법
클래스이름 변수이름;
ex) Date today = new Date(); // Date 객체를 생성해서, 그 주소를 today에 저장한다.

2.1 기본형 
기본형은 8개 타입이 있고 
논리형 문자형 정수형 실수형으로 구분된다.
boolean = true, false
char = 문자 하나 저장
byte = 이진 데이터 다룰 때 주로 사용
short = C언어랑 호환하려고 추가함
int, long = .주로 사용되는 정수값 저장 타입

2.2 상수와 리터럴
상수도 값을 저장할 수 있는 공간이지만 변수랑을 달리
한번 저장하면 못바꾼다.

final 키워드를 붙이면 된다.
ex) final int MAX_SPEED = 10;
상수는 선언과 동시에 초기화를 해줘야 한다.

리터럴 = 원래 12, 123, 3.14, 'A' 같은 값들이 상수인데 
프로그래밍에선 상수라는 또 다른 의미를 정했기 때문에 요런 값들의 이름을 상수대신 리터럴이란 이름으로 재 정의 했다.
ex) int year = 2014;
         변수 = 리터럴;
    final int MAX_VALUE = 100;
                변       수 = 리터럴;

상수가 필요한 이유 = 상수는 리터럴에 의미있는 이름을 붙여서 코드의 이해와 수정을 쉽게 해주기 위해 만든다.

리터럴 타입과 접미사 : 
논리형 리터럴 = true, false, 접미사 = 없음
정수형 리터럴 = 123, 0b0101, 077, 0xFF, 100L, 접미사  = L
실수형 리터럴 = 3.14, 3.0e8, 1.4f, 접미사 = f, d
문자형 리터럴 = 'A', 'a', 'B', 접미사 = 없음
문자열 리터럴 = "ABC", "123", 접미사 = 없음

실수형에선 floast 타입 리터럴 뒤에 f 나 F 를 붙이고 
double 타입 리터럴 뒤에는 d 나 D 를 붙인다.
float pi = 3.14f;
double rate = 1.618d;

또 정수형 기본 자료형이 int 인 것 처럼
실수형 기본 자료형이 double 이라 접미사 d 생략이 가능하다
근데 float 는 생략이 안된다.

리터럴에 소수점이나 10의 제곱을 나타내는 기호 E 또는 e 그리고 접미사 f F d D 를 포함하고 있으면 실수형 리터럴로 간주된다.
또 잘 안쓰지만 p 를 이용해서 실수 리터럴을 16진 지수형태로 표현 할 수 있다. p 는 2의 제곱을 의미하며 , p의 왼쪽엔 16진수를 적고 오른쪽엔 지수를 10진 정수로 적는다.
p 는 대소문자 둘다 가능하고 p가 포함된 리터럴은 실수형이다.
[참고] flaoat 는 점미사나 정밀도 등 신경 쓸게 많다 귀찮으면 근냥 int 처럼 double 을 사용하자.

문자 리터럴과 문자열 리터럴 
'A' 처럼 작은 따음표 하나로 감싼걸 '문자 리터럴' 이라고 한다.
"A" 처럼 큰 따음표 로 감싼걸 '문자열 리터럴' 이라고 한다.

char 타입 변수는 단 하나 문자만 저장 할 수 있다.
여러 문자를 저장하려면 String 을 써라
String str = ""; <- 내용이 없는 빈 문자열
char ch = ''; <- 에러 안에 하나의 문자가 반드시 필요

String 은 클래스이다.
String name = new String("Java"); // String 객체를 생성

덧셈 연산자를 사용하면 문자열을 결합할 수 있어서 다음처럼 가능하다.
String name = "Ja" + "Va";
System.out.println(name); // JaVa
