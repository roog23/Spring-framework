# Spring-framework
자바 플랫폼을 위한 오픈소스 애플리케이션 프레임워크로 개발하기 위한 모든 기능을 종합적으로 제공하는 경량화된 솔루션   
경량 컨테이너로 자바 객체를 담고 직접 관리   

spring-framework는 IOC(inversion of Control)기반
-
일반적으로 각 객체들이 프로그램의 흐름을 결정하고 각 객체를 구성하는 작업에 직접적으로 참여하는 사용자가 제어하는 구조에서,   
자신이 언제 만들어지고 사용되는지 모르는 상태로 권한을 다른 대상에게 위임함으로써 제어 권한을 위임받은 객체에서 결정을하는 구조가 됨   
제어의 흐름을 사용자가 컨트롤하지 않고 위임한 특별한 객체에 모든 것을 맡기는 것   

IOC는 DI와 DL에 의해 구현   
-
DL(Dependency Lookup)- 의존성 검색   
컨테이너에서는 객체들을 관리하기 위해 별도의 저장소에 빈을 저장   
개발자들이 컨테이너에서 제공하는 API를 이용하여 사용하고자 하는 빈을 검색하는 방법   

DI(Dependency Injection) - 의존성 주입   
객체가 서로 의존하는 관계가 되게 의존성을 주입하는 것   
객체지향 프로그램에서는 하나의 객체가 어떠한 다른 객체를 사용하고 있음을 의미   
IOC에서는 각 클래스 사이에 필요로 하는 의존 관계를 빈 설정 정보를 바탕으로 컨테이너가 자동으로 연결해주는 것   

Spring framework는 POJO 기반  
- 
EJB는 확장 가능한 재사용이 가능한 로직을 개발하기 위해 사용    
한가지 기능을 위해 불필요하게 복잡한 로직이 들어가는 단점이 있었음   
POJO는 getter/setter를 가진 단순 자바 오브젝트로 정의   
단순 오브젝트는 의존성이 없고 추후 테스트 및 유지 보수가 편리한 유연성의 장점을 가짐   

Spring framework는 AOP   
-
AOP는 관점 지향 프로그래밍   
OOP는 객체지향 원칙에 따라 관심사가 같은 데이터를 한 곳에 모아 분리하고 낮은 결합도를 가지고 있어 독립적이고 유연한 모듈로 캡슐화 하는것   
이 과정중 중복된 코드가 많아지고, 가독성, 확장성, 유지보수성을 떨어 뜨려 이를 보완하는 AOP를 사용   
AOP는 핵심 기능과 공통기능을 분리시켜 핵심 로직에 영향을 끼치지 않게 공통기능을 끼워 넣는 형태   
중복되는 코드를 제거가능해지고, 공통기능을 한 곳에 보관하여 유지보수가 효율적으로 가능해지고 재활용성이 높아짐   

Spring framework는 MVC
-
Model에서는 데이터 처리를 담당   
Service영역과 DAO영역으로 구분   
Service 부분은 불필요한 HTTP통신을 하지 않아야 하고, request나 response와 같은 객체를 매개 변수로 받으면 안됨   
view에 종속적인 코드가 존재하면 안되고 view가 변경되도 그대로 사용가능해야 함
Model에서는 View와 Controller 어떠한 정보도 가지고 있으면 안됨   

View는 사용자 인터페이스를 담당   
Controller를 통해 모델에 데이터에 대한 시각화를 담당하여 자신이 요청을 보낼 Controller의 정보만을 가지고 있어야함   
Model이 가지고 있는 정보를 저장하면 안되고 Model, Controller에 구성 요소를 알면 안됨   

Controller는 View에 받은 요청을 가공하여 Model에 전달 or Model로 부터 받은 결과를 View로 넘겨주는 역할을 담당   
Controller에서는 모든 요청 에러와 모델 에러를 처리하며 Model과 View의 정보를 알고 있어야함   

Model, View, Controller를 나눠 소스를 불리하여 목적이 명확하게 할 수 있고, 유지보수 하는데 용이함   

Spring Framework의 구조
=
Spring Core
-

Spring Context
-

Spring AOP
-

Spring Dao
-

Spring ORM
-

Spring Web
-

Spring MVC
-
