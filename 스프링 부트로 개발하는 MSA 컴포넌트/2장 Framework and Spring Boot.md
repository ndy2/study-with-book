
프레임워크란 용도에 맞는 일반적인 기능들을 보편적인 방식으로 제공한다.
> ❗ 면접 단골 질문 중 하나인 Framework/ Library/ API 의 차이도 이해하자!


스프링은 참 다양한 의미를 가진다.
- Spring (Framework) - 스프링 프레임워크
- Spring (Core Framework) - 스프링 핵심 프레임 워크
- Spring (Application Context, BeanFactory) - IOC 컨테이너

[스프링 프로젝트 공식문서](https://spring.io/projects/spring-framework) 의 소개글 첫머리와 그 특징이다.

[Spring Framework](https://spring.io/projects/spring-framework)
> The Spring Framework provides a comprehensive programming and configuration model for modern Java-based enterprise applications - on any kind of deployment platform.

- POJO 기반의 경량 컨테이너 제공
- 복잡한 비즈니스 영역의 문제를 쉽게 개발하고 운영하기 위한 철학 (the Spring Triangle)
- Module 식 프레임워크


[Spring Boot](https://spring.io/projects/spring-boot)
> Spring Boot makes it easy to create stand-alone, production-grade Spring based Applications that you can "just run".

-   Create stand-alone Spring applications
-   Embed Tomcat, Jetty or Undertow directly (no need to deploy WAR files)
-   Provide opinionated 'starter' dependencies to simplify your build configuration
-   Automatically configure Spring and 3rd party libraries whenever possible
-   Provide production-ready features such as metrics, health checks, and externalized configuration
-   Absolutely no code generation and no requirement for XML configuration


두 프로젝트에서 개발시 경험하는 스프링의 대부분의 마법같은 일이 일어난다.
IOC, AOP, AutoConfigure, Embedded WAS ...

스프링 애플리케이션은 자바 애플리케이션이므로 `main` 메서드에 의해 시작된다.
Spring Initializer로 프로젝트를 생성하게 되면 `SpringApplication.run` 메서드를 호출하는 코드가 달랑 한줄 있다. `run` 메서드가 의미하는 바를 간단히 정리해보자.