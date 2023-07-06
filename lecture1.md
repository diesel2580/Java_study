<h1>Java</h1>

<h5>intelliJ IDEA 단축키 모음</h5>

_편집기_

a. ctrl + alt + enter : 윗 줄로 엔터

b. ctrl + alt + L : 코드 정렬

c. ctrl + y: 전체 라인 삭제

d. ctrl + /: 주석 처리

_컴파일_

a. shift + F10 : 프로젝트 실행

<br>
<br>

<h4>입출력</h4>

1. Scanner 클래스를 이용한 입력

- java.util에서 import 하는 클래스
- 입력되는 키 값을 공백으로 구분되는 토큰 단위로 읽는다.

  a. 클래스 import

  ```java
    import java.util.Scanner;
    import java.util.*; //java.util에 있는 모든 클래스를 import
  ```

  b. Scanner 객체 생성

  ```java
   Scanner sc = new Scanner(System.in);
   //new : 새로운 객체를 heap 메모리에 할당
   //System.in : 콘솔에서 입력을 받는 표준 라이브러리
  ```

  c. Scanner 객체를 이용한 입력

  - 자료형에 따라 Scanner 클래스의 메서드를 달리해야 함
    |메소드|설명|
    |-----|---|
    |next()|String을 읽음, 토큰 기준|
    |nextLine()|String을 읽음, Enter 기준|
    |nextInt()|int를 읽음|
    |nextBoolean()|boolean을 읽음 |
    |nextLong()|long을 읽음|
    |nextDouble()|double을 읽음|
    |nextFloat()|float을 읽음|
    <br>
    <br>

2.  표준 출력(System.out) 을 이용한 출력

- 따로 import 하지 않아도 된다.
  |메소드|설명|
  |----|---|
  |System.out.println()|출력 후 개행|
  |System.out.print()|개행 없이 출력|
  |System.out.printf()|c와 유사, 형식에 맞추어 출력|
- println, print 예제 코드

  ```java
    int a = 10;
    int b = 20;
    char c = 'A';
    String d = "str";

    /*리터럴*/
    System.out.println("내용"); // 출력 + 개행
    System.out.println(123); // 출력 + 개행
    System.out.print("내용\n"); // 출력 + 개행 (개행문자 \n사용)
    System.out.print("내용"); // 출력 + 개행 X

    /*변수*/
    System.out.println(a); //int 출력
    System.out.println(c); //char 출력
    System.out.println(d); //String 출력

    System.out.println(a + b); // 변수와 변수의 연산
    System.out.println(a + c); // C변수의 (A)라는 문자를 아스키코드값 65로 인식
    System.out.println("문자열" + d);  // "문자열"+변수 => 문자열
    System.out.println(c + d); // 문자 + 문자열 = > 문자열
  ```

- printf 예제 코드

  - %d(정수), %f(실수), %c(문자), &s(문자열), %n \n(줄바꿈)

  ```java
      System.out.printf("%d %n",100);
      System.out.printf("%s %n","hello");

      System.out.printf("탭(tab): \t");
      System.out.printf("줄바꿈: \n");
      System.out.printf("%연산자: %%");
  ```

    <br>

3. 입출력을 활용한 예제

```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a;
        int b;
        int c;
        a = sc.nextInt();
        b = sc.nextInt();
        c = sc.nextInt();
        System.out.println((a + b) % c);
        System.out.println(((a % c) + ((b % c))) % c);
        System.out.println(((a * b) % c));
        System.out.println((((a % c) * (b % c)) % c));
    }
}
```
