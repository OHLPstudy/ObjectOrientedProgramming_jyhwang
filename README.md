## 좋은 객체 지향 프로그래밍

[[좋은 객체지향 프로그래밍이란?](https://velog.io/@yyy96/%EA%B0%9D%EC%B2%B4%EC%A7%80%ED%96%A5-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D)](https://velog.io/@yyy96/객체지향-프로그래밍)

[[좋은 객체 지향이란?](https://velog.io/@kcho32/%EC%A2%8B%EC%9D%80-%EA%B0%9D%EC%B2%B4-%EC%A7%80%ED%96%A5%EC%9D%B4%EB%9E%80)](https://velog.io/@kcho32/좋은-객체-지향이란)

[[좋은 객체 지향 설계의 5가지 원칙 (SOLID)](https://kkkdh.tistory.com/entry/%EC%A2%8B%EC%9D%80-%EA%B0%9D%EC%B2%B4-%EC%A7%80%ED%96%A5-%EC%84%A4%EA%B3%84%EC%9D%98-5%EA%B0%80%EC%A7%80-%EC%9B%90%EC%B9%99-SOLID#lsp-%EB%A6%AC%EC%8A%A4%EC%BD%94%ED%94%84-%EC%B9%98%ED%99%98-%EC%9B%90%EC%B9%99---liskov-substitution-principle)](https://kkkdh.tistory.com/entry/좋은-객체-지향-설계의-5가지-원칙-SOLID#lsp-리스코프-치환-원칙---liskov-substitution-principle)

[[좋은 객체지향 프로그래밍이란?](https://ningpop.tistory.com/85)](https://ningpop.tistory.com/85)

### 절차 지향 프로그래밍

- 물이 위에서 아래로 흐르는 것처럼 순차적인 처리가 중요시 되며 프로그램 전체가 유기적으로 연결되도록 만드는 프로그래밍 기법
- 기존 코드를 재사용하는게 비효율적이고 유지보수가 어려움
- 실행 순서가 정해져 있으므로 코드의 순서가 바뀌면 동일한 결과를 보장하기 어려움

### 구조적 프로그래밍

- 절차적 프로그래밍의 하위 개념
- 프로그램을 작은 함수 단위로 나누고 함수끼리 호출을 하는 방식
- 한 문서 내에 메소드의 수가 많아질 경우 추후 유지 보수가 어려움

### 객체 지향 프로그래밍

- 실세계의 사물 또는 개념들을 “객체”로 바라보고, 상태와 행위를 가진 객체를 만들어 그 객체들 간 상호작용을 통해 프로그램을 만들어 나가는 방식
- 유지보수가 어려웠던 절차지향, 구조적 프로그래밍을 해결하기 위해 등장
- 객체를 독립성과 신뢰성이 보장되게 만들어 놓으면 재사용성이 높아지므로 유지보수가 용이
- ~~객체 지향 프로그래밍은 컴퓨터 프로그램을 명령어의 목록으로 보는 시각에서 벗어나 여러 개의 독립된 단위, 즉 “객체”들의 모임으로 파악하고자 하는 것이다. 각각의 객체는 메시지를 주고받고, 데이터를 처리할 수 있다. (협력)~~
- 객체 지향 프로그래밍은 프로그램을 유연하고 변경이 용이하게 만들기 때문에 대규모 소프트웨어 개발에 많이 사용된다.
    
    → 다형성
    

### 객체 지향 특성

1. 다형성
    - 다양한 형태를 가질 수 있게 해줌
    - 인터페이스를 구현한 객체 인스턴스를 실행 시점에 유연하게 변경할 수 있다.
    - 다형성의 본질을 이해하려면 협력이라는 객체 사이의 관계에서 시작해야 함
    - 예시 : 운전자-자동차 / 공연
    - 구현 대상의 내부 구조가 변경되거나, 구현 대상 자체가 변경되어도 클라이언트는 영향을 받지 않음
![Image](https://github.com/OHLPstudy/ObjectOrientedProgramming_jyhwang/assets/78784311/1ab8f8d4-afb0-49be-85cb-5c65a0617fca)

2. 추상화
3. 캡슐화
4. 상속

### 다형성 ⇒ 역할과 구현 분리 가능

- 역할과 구현의 분리가 가능한 것
- 역할과 구현으로 구분하면 세상이 단순해지고, 유연해지며 변경도 편리해진다.
- 장점 
 → 클라이언트는 대상의 역할(인터페이스)만 알면 된다.
 → 클라이언트는 구현 대상의 내부 구조를 몰라도 된다.
 → 클라이언트는 구현 대상의 내부 구조가 변경되어도 영향을 받지 않는다.
 → 클라이언트는 구현 대상 자체를 변경해도 영향을 받지 않는다.
- (자바 언어) 역할과 구현 분리
- 자바 언어의 다형성 활용
 → 역할 = 인터페이스
 → 구현 = 인터페이스를 구현한 클래스, 구현 객체
- 객체를 설계할 때 역할과 구현을 명확히 분리
- 객체 설계 시 역할(인터페이스)을 먼저 부여하고, 그 역할을 수행하는 구현 객체 만들기
- 정리
- 실세계의 역할과 구현이라는 편리한 컨셉을 다형성을 통해 객체 세상으로 가져올 수 있음
- 유연하고, 변경 용이
- 확장 가능한 설계
- 클라이언트에 영향을 주지 않는 변경 가능
- 인터페이스를 안정적으로 잘 설계하는 것이 중요
- 한계
- 역할(인터페이스) 자체가 변하면, 클라이언트, 서버 모두에 큰 변경이 발생한다.
- 자동차를 비행기로 변경해야 한다면?
- 대본 자체가 변경된다면?
- USB 인터페이스가 변경된다면?
- 인터페이스를 안정적으로 잘 설계하는 것이 중요

### 자바 언어의 다형성

- **객체 지향의 핵심**
- 역할 = 인터페이스
- 구현 = 인터페이스 구현 클래스 or 객체
**객체 설계시 역할과 구현의 명확한 분리 필요**
- 인터페이스 먼저 설계 후, 구현

### 스프링과 객체 지향

- 다형성이 가장 중요
- 스프링은 다형성을 극대화해서 이용할 수 있게 도와준다.
- 스프링에서 이야기하는 제어의 역전(IoC), 의존관계 주입(DI)은 다형성을 활용해서 역할과 구현을 편리하게 다룰 수 있도록 지원한다.
- 스프링을 사용하면 마치 레고 블럭 조립하듯이, 공연 무대의 배우를 선택하듯이, 구현을 편리하게 변경할 수 있다.

## 좋은 객체 지향 설계의 5가지 원칙 (SOLID)

[[💠 객체 지향 설계의 5가지 원칙 - S.O.L.I.D](https://inpa.tistory.com/entry/OOP-%F0%9F%92%A0-%EA%B0%9D%EC%B2%B4-%EC%A7%80%ED%96%A5-%EC%84%A4%EA%B3%84%EC%9D%98-5%EA%B0%80%EC%A7%80-%EC%9B%90%EC%B9%99-SOLID#%EB%8B%A8%EC%9D%BC_%EC%B1%85%EC%9E%84_%EC%9B%90%EC%B9%99_-_srp_single_responsibility_principle)](https://inpa.tistory.com/entry/OOP-💠-객체-지향-설계의-5가지-원칙-SOLID#단일_책임_원칙_-_srp_single_responsibility_principle)

### SOLID

- 클린코드로 유명한 로버트 마틴이 좋은 객체 지향 설계의 5가지 원칙 정리
- SRP : 단일 책임 원칙(single responsibility principle)
- OCP : 개방-폐쇄 원칙(Open/closed principle)
- LSP : 리스코프 치환 원칙(Liskov substitution principle)
- ISP : 인터페이스 분리 원칙(Interface segregation principle)
- DIP : 의존관계 역전 원칙(Dependency inversion principle)

### SRP : 단일 책임 원칙(Single Responsibility Principle)

- 한 클래스는 하나의 책임만 가져야 한다.
- ‘책임’의 의미는 하나의 ‘기능 담당’
- 즉, 하나의 클래스는 하나의 기능을 담당하여 하나의 책임을 수행하는데 집중되도록 클래스를 따로따로 설계하라는 원칙
- 하나의 클래스에 기능(책임)이 여러 개 있다면 기능 변경(수정)이 일어났을 때 수정해야 할 코드가 많아짐
- 중요한 기준은 변경. 변경이 있을 때 파급 효과가 적으면 단일 책임 원칙을 잘 따른 것
    
    ⇒ 단일 책임 원칙의 목적은 프로그램의 유지보수 성을 높이기 위한 설계 기법
    
- ex ) UI 변경, 객체의 생성과 사용 분리
    
    ⇒ 청소기는 청소만 잘하면 된다는 책임을 가지면 됨 = 하나의 클래스로 한 가지 책임(기능)만 수행하면 됨
    

### OCP : 개방-폐쇄 원칙(Open/Closed principle)

![Image](https://github.com/OHLPstudy/ObjectOrientedProgramming_jyhwang/assets/78784311/cce500a5-5681-4fa1-986d-850dfa6037ae)
- 클래스는 확장에는 열려 있으나 변경에는 닫혀 있어야 한다.
- 기능 추가 요청 시 → 클래스 확장을 통해 손쉽게 구현하면서, 확장에 따른 클래스 수정은 최소화
- 확장에 열려있다 : 새로운 변경 사항이 발생했을 때 유연하게 코드를 추가함으로서 큰 힘을 들이지 않고, 애플리케이션의 기능을 확장할 수 있음
- 변경에 닫혀있다 : 새로운 변경 사항이 발생했을 때 객체를 직접적으로 수정하는 것을 제한함
- OCP 원칙은 추상화 사용을 통한 관계 구축을 권장
- 다형성과 확장을 가능케 하는 객체지향 장점 극대화

### LSP : 리스코프 치환 원칙(Liskov Substitution Principle)

![Image](https://github.com/OHLPstudy/ObjectOrientedProgramming_jyhwang/assets/78784311/be9dbefe-c2ec-4773-a9f8-d05dfa89a8c8)
- 서브 타입은 언제나 기반(부모) 타입으로 교체할 수 있어야 한다는 원칙
- LSP는 다형성 원리를 이용하기 위한 원칙
- 다형성의 특징을 이용하기 위해 상위 클래스 타입으로 객체를 선언하여 하위 클래스의 인스턴스를 받으면, 업캐스팅된 상태에서 부모의 메서드를 사용해도 동작이 의도대로 흘러가야 하는 것
- ~~프로그램의 객체는 프로그램의 정확성을 깨뜨리지 않으면서 하위 타입의 인스턴스로 바꿀 수 있어야 한다.~~
- ~~다형성에서 하위 클래스는 인터페이스 규약을 다 지켜야 한다는 것, 다형성을 지원하기 위한 원칙, 인터페이스를 구현한 구현체는 믿고 사용하려면, 이 원칙 필요~~
- ~~단순히 컴파일에 성공하는 것을 넘어서는 이야기~~
- ex ) 자동차 인터페이스의 엑셀은 앞으로 가라는 기능, 뒤로 가게 구현하면 LSP 위반, 느리더라도 앞으로 가야함

### ISP : 인터페이스 분리 원칙(Interface Segregation Principle)

![Image](https://github.com/OHLPstudy/ObjectOrientedProgramming_jyhwang/assets/78784311/263be0c0-6d9c-410b-aaa7-ecf0d0f4e940)
- 인터페이스를 각각 사용에 맞게 끔 잘게 분리해야  한다는 설계 원칙
- SRP(단일 책임 원칙)이 클래스의 단일 책임을 강조한다면, ISP는 인터페이스의 단일 책임을 강조하는 것
    
    ⇒ SRP 원칙의 목표는 클래스 분리를 통해 이루어진다면, ISP 원칙은 인터페이스 분리를 통해 설계하는 원칙
    
- ISP 원칙은 인터페이스를 사용하는 클라이언트를 기준으로 분리함으로써, 클라이언트의 목적과 용도에 적합한 인터페이스 만을 제공하는 것이 목표
⇒ but, ISP 원칙의 주의 해야 할 점은 한 번 인터페이스를 분리하여 구성 해놓고 나중에 무언가 수정 사항이 생겨서 또 인터페이스들을 분리하는 행위를 가하지 말아야 함
- ~~특정 클라이언트를 위한 인터페이스 여러 개가 범용 인터페이스 하나보다 낫다~~
- 자동차 인터페이스 → 운전 인터페이스, 정비 인터페이스로 분리
- 사용자 클라이언트 → 운전자 클라이언트, 정비사 클라이언트로 분리
- 분리하면 정비 인터페이스 자체가 변해도 운전자 클라이언트에 영향을 주지않음
- 인터페이스가 명확해지고, 대체 가능성이 높아진다.

### DIP : 의존관계 역전 원칙(Dependency Inversion Principle)

![Image](https://github.com/OHLPstudy/ObjectOrientedProgramming_jyhwang/assets/78784311/8ed1b952-3ff5-4aa5-a503-e238a326eb24)
- 프로그래머는 “추상화에 의존해야지, 구체화에 의존하면 안된다.” 의존성 주입은 이 원칙을 따르는 방법 중 하나
- 쉽게 이야기해서 구현 클래스에 의존하지 말고, 인터페이스(역할)에 의존하라는 뜻
- 의존 관계를 맺을 때 변화하기 쉬운 것 또는 자주 변화하는 것보다는, 변화하기 어려운 것 거의 변화가 없는 것에 의존하라는 것 
⇒ 그래야 유연하게 구현체 변경 가능
- 의존 역전 원칙의 지향점은 각 클래스 간의 결함도(coupling)을 낮추는 것

## ⇒ 정리

- 객체 지향의 핵심은 다형성
- but,
    
    ⇒ 다형성 만으로는 쉽게 부품을 갈아 끼우듯 개발할 수 없음x
    
    ⇒ 다형성 만으로는 구현 객체를 변경할 때 클라이언트 코드도 변경됨
    
    ⇒ 다형성 만으로는 OCP, DIP를 지킬 수 없다.
    
- 추가적으로 무언가 더 필요함
    
    **⇒ 스프링은 다음 기술로 다형성 + OCP, DIP 원칙을 가능하게 지원한다.**
    
    - DI (Dependency Injection): 의존 관계, 의존성 주입
    - DI 컨테이너 제공

## Q&A

1. 개방폐쇄 원칙(OCP)의 코드 예제 (’변경에 닫혀있는’ 방식 예제)
    - 원칙 위반 예제
        
        - Animal 클래스와 Animal 타입을 받아 각 동물의 소리에 맞춰 출력하는 HelloAnimal 클래스
        - 기존 기능 : 고양이, 개
        
        ```java
        class Animal {
        	String type;
        	
        	Animal(String type) {
        		this.type = type;
        	}
        }
        
        // 동물 타입을 받아 각 동물에 맞춰 울음소리를 내게 하는 클래스 모듈
        class HelloAnimal {
            void hello(Animal animal) {
                if(animal.type.equals("Cat")) {
                    System.out.println("냐옹");
                } else if(animal.type.equals("Dog")) {
                    System.out.println("멍멍");
                }
            }
        }
        
        public class Main {
            public static void main(String[] args) {
                HelloAnimal hello = new HelloAnimal();
                
                Animal cat = new Animal("Cat");
                Animal dog = new Animal("Dog");
        
                hello.hello(cat); // 냐옹
                hello.hello(dog); // 멍멍
            }
        }
        ```
        
        - 기능 추가 : 양, 사자
        
        - 추가된 기능을 각 객체의 필드 변수에 맞게 if문을 이용하여 분기처리하여 구성해주어야 한다. 
          → OCP 원칙이 제대로 적용되지 않아 기능이 추가될 때마다 코드를 변경해줘야 한다.
        
        ```java
        class Animal {
        	String type;
            
            Animal(String type) {
            	this.type = type;
            }
        }
        
        class HelloAnimal {
        	// 기능을 확장하기 위해서는 클래스 내부 구성을 일일히 수정해야 하는 번거로움이 생긴다.
            void hello(Animal animal) {
                if (animal.type.equals("Cat")) {
                    System.out.println("냐옹");
                } else if (animal.type.equals("Dog")) {
                    System.out.println("멍멍");
                } else if (animal.type.equals("Sheep")) {
                    System.out.println("메에에");
                } else if (animal.type.equals("Lion")) {
                    System.out.println("어흥");
                }
                // ...
            }
        }
        
        public class Main {
            public static void main(String[] args) {
                HelloAnimal hello = new HelloAnimal();
        
                Animal cat = new Animal("Cat");
                Animal dog = new Animal("Dog");
                Animal sheep = new Animal("Sheep");
                Animal lion = new Animal("Lion");
        
                hello.hello(cat); // 냐옹
                hello.hello(dog); // 멍멍
                hello.hello(sheep); 
                hello.hello(lion);
            }
        }
        ```
        
    
    - 원칙 적용 예제
        
        - 먼저 변경(추가)될 것과 변하지 않을 것을 구분한다.
        
        - 이 두 모듈이 만나는 지점에 추상화(추상클래스 or 인터페이스)를 정의한다.
        
        - 구현체에 의존하기보다 정의한 추상화에 의존하도록 코드를 작성한다.
        
        ```java
        // 추상화에 의존하도록 코드 작성 필요
        abstract class Animal {
            abstract void speak();
        }
        
        class Cat extends Animal { // 상속
            void speak() {
                System.out.println("냐옹");
            }
        }
        
        class Dog extends Animal { // 상속
            void speak() {
                System.out.println("멍멍");
            }
        }
        
        class HelloAnimal {
            void hello(Animal animal) {
                animal.speak();
            }
        }
        
        public class Main {
            public static void main(String[] args) {
                HelloAnimal hello = new HelloAnimal();
        
                Animal cat = new Cat();
                Animal dog = new Dog();
        
                hello.hello(cat); // 냐옹
                hello.hello(dog); // 멍멍
            }
        }
        ```
        
        - 기능 추가 : 양, 사자
        
        - HelloAnimal 클래스의 코드 수정 없이(변경에 닫힘) 정상적으로 기능 확장 된다.
        
        ```java
        // 추상화
        abstract class Animal {
            abstract void speak();
        }
        
        class Cat extends Animal { // 상속
            void speak() {
                System.out.println("냐옹");
            }
        }
        
        class Dog extends Animal { // 상속
            void speak() {
                System.out.println("멍멍");
            }
        }
        
        // 추상클래스를 상속만 하면 메소드 강제 구현 규칙으로 규격화만 하면 확장에 제한 없다 (opened)
        class Sheep extends Animal {
            void speak() {
                System.out.println("매에에");
            }
        }
        
        class Lion extends Animal {
            void speak() {
                System.out.println("어흥");
            }
        }
        
        // 기능 확장으로 인한 클래스가 추가되어도, 더이상 수정할 필요가 없어진다 (closed - 변경에 닫힘)
        class HelloAnimal {
            void hello(Animal animal) {
                animal.speak();
            }
        }
        
        public class Main {
            public static void main(String[] args) {
                HelloAnimal hello = new HelloAnimal();
        
                Animal cat = new Cat();
                Animal dog = new Dog();
                Animal sheep = new Sheep();
                Animal lion = new Lion();
        
                hello.hello(cat); // 냐옹
                hello.hello(dog); // 멍멍
                hello.hello(sheep); // 매에에
                hello.hello(lion); // 어흥
            }
        }
        ```
        
2. 구조적 프로그래밍과 객체지향 프로그래밍의 차이 
    - 구조적 프로그래밍
        
        - 제어 흐름의 직접적인 전환에 대한 규칙 제시
        
        - “기능”을 중심적으로 개발 진행
        
    - 객체지향 프로그래밍
        
        - 제어 흐름의 간접적인 전환에 대한 규칙 제시
        
        - 프로그램 처리 단위가 “객체(속성-변수 / 기능-함수)”인 프로그래밍 방법
        
        - 소프트웨어의 핵심을 “기능”이 아닌 “객체”로 삼으며, “누가 어떠한 일을 할 것인가?”에 초점을 맞춘다. 즉, 객체를 도출하고 각각의 역할을 정의하는 것에 초점을 맞춘다.
        
        ⇒ 객체 지향적 코드는 상태와 행위를 하나의 “클래스”라는 단위로 묶어 관리한다. 클래스 내부를 수정하면 해당 클래스를 이어받는 여러 객체들과 변경사항을 공유할 수 있다.
        
        - “현실 세계를 모델링”하는 대표적인 프로그래밍 패러다임
        
    
    ⇒ 구조적 프로그래밍은 “기능 중심”이기에 주로 전역 변수를 활용하여 상태를 관리하지만, 객체지향 프로그래밍은 “상태”와 “행위”를 하나의 “클래스”라는 단위로 묶어 관리한다. 클래스 내부를 수정하면 해당 클래스를 이어받는 여러 객체들과 변경사항을 공유할 수 있게 된다.
    
3. (다형성) 역할과 구현 분리 예제 
    - 역할 = 인터페이스 / 구현 = 인터페이스 구현 클래스 or 객체
        
        ```java
        //역할
        interface Movable
        {
        	void move(boolean direction);
        }
        
        //구현
        class Unit implements Movable
        {
        	@Override
        	public void move(boolean direction)
        	{
        		// 동작
        	}
        
        	public void work(String act)
        	{
        		// 동작
        	}
        }
        ```
        
        - 실제 사용 예제
        
        ```java
        interface Movable
        {
        	void move(boolean direction);
        }
        
        class UnitA implements Movable
        {
        	@Override
        	public void move(boolean direction)
        	{
        		work("run");
        	}
        
        	private void work(String act)
        	{
        		System.out.println("work: " + act);
        	}
        }
        
        class UnitB implements Movable
        {
        	@Override
        	public void move(boolean direction)
        	{
        		doing(3);
        	}
        
        	private void doing(int num)
        	{
        		System.out.println("doing: " + num);
        	}
        }
        
        class UnitC implements Movable
        {
        	@Override
        	public void move(boolean direction)
        	{
        		active(true);
        	}
        
        	private void active(boolean flag)
        	{
        		System.out.println("active: " + flag);
        	}
        }
        ```
        
        ```java
        public class Main
        {
        	public static void main(String[] args)
        	{
        		Movable movable = switch (new Random().nextInt(3))
        		{
        			case 0 -> new UnitA();
        			case 1 -> new UnitB();
        			case 2 -> new UnitC();
        			default -> null;
        		};
        		
        		movable.move(true);
        	}
        }
        
        // 실행 결과(결과 랜덤) 
        // work: run
        ```
        
    
4. 인터페이스 분리 원칙(ISP) 위반 예제와 수정
    - ISP원칙은 범용적인 인터페이스 보다는 클라이언트(사용자)가 실제로 사용하는 인터페이스를 만들어야 함
    → 클라이언트의 목적과 용도에 적합한 인터페이습만을 제공해야 함
    - 원칙 위반 예제
        
        - interface
        
        ```java
        interface ISmartPhone {
            void call(String number); // 통화 기능
            void message(String number, String text); // 문제 메세지 전송 기능
            void wirelessCharge(); // 무선 충전 기능
            void AR(); // 증강 현실(AR) 기능
            void biometrics(); // 생체 인식 기능
        }
        ```
        
        - class
        
        ```java
        //신형 기종 -> 모든 기능이 필요하므로 ISP원칙 만족
        class S20 implements ISmartPhone {
            public void call(String number) {
            }
        
            public void message(String number, String text) {
            }
        
            public void wirelessCharge() {
            }
        
            public void AR() {
            }
        
            public void biometrics() {
            }
        }
        
        //신형 기종 -> 모든 기능이 필요하므로 ISP원칙 만족
        class S21 implements ISmartPhone {
            public void call(String number) {
            }
        
            public void message(String number, String text) {
            }
        
            public void wirelessCharge() {
            }
        
            public void AR() {
            }
        
            public void biometrics() {
            }
        }
        
        //구형 기종 -> 무선 충전/생체인식 기능 포함X
        //추상 메소드 구현 규칙상 오버라이딩은 하되, 메서드 내부는 빈 공간으로 두거나 혹은 예외가 발생하도록 구현해야함
        //필요하지도 않은 기능을 어쩔 수 없이 구현하게 되어 낭비 발생
        // -> ISP원칙을 어김 
        class S3 implements ISmartPhone {
            public void call(String number) {
            }
        
            public void message(String number, String text) {
            }
        
            public void wirelessCharge() {
                System.out.println("지원 하지 않는 기능 입니다.");
            }
        
            public void AR() {
                System.out.println("지원 하지 않는 기능 입니다.");
            }
        
            public void biometrics() {
                System.out.println("지원 하지 않는 기능 입니다.");
            }
        }
        ```
        
    - 원칙 적용 예제
        
        - 각각의 기능에 맞게 인터페이스를 잘게 분리하도록 구성
        
        - 잘게 분리된 인터페이스를 클래스가 지원되는 기능만을 선별하여 implements 하면 원칙이 지켜짐
        
        - interface
        
        ```java
        interface IPhone {
            void call(String number); // 통화 기능
            void message(String number, String text); // 문제 메세지 전송 기능
        }
        
        interface WirelessChargable {
            void wirelessCharge(); // 무선 충전 기능
        }
        
        interface ARable {
            void AR(); // 증강 현실(AR) 기능
        }
        
        interface Biometricsable {
            void biometrics(); // 생체 인식 기능
        }
        ```
        
        - class
        
        ```java
        class S21 implements IPhone, WirelessChargable, ARable, Biometricsable {
            public void call(String number) {
            }
        
            public void message(String number, String text) {
            }
        
            public void wirelessCharge() {
            }
        
            public void AR() {
            }
        
            public void biometrics() {
            }
        }
        
        class S3 implements IPhone {
            public void call(String number) {
            }
        
            public void message(String number, String text) {
            }
        }
        ```
