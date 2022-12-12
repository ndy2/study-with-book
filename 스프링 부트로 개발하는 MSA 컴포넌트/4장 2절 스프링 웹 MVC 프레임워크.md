### Grosary

**자바 플랫폼 엔터프라이즈 에디션**
- a.k.a. Java platform. Enterprise Edition, Java EE, J2EE
- 자바 언어를 사용하여 엔터프라이즈 애플리케이션을 만들 수 있는 플랫폼
- 동시에 표준 스펙의 집합
- 웹 애플리케이션(JSP, Servlet 등), 데이터베이스 접근(JDBC), 자바 메시징 처리 (JMS) ...

**Servlet**
- HTTP 프로토콜을 사용하여 데이터를 주고받는 서버용 프로그래밍 스펙
- javax.servlet.Servlet 인터페이스 형태로 Java API 에서 제공
	- c.f. tomcat 10 이상 -> jakarta.servlet.Servlet (Java EE -> Jakarta EE 로 migrate)
	
> A servlet is a small Java program that runs within a Web server. Servlets receive and respond to requests from Web clients, usually across HTTP, the HyperText Transfer Protocol

Servlet Container
- a.k.a. Web Application Server (자바 진영)
- 서블릿을 보관, 관리하고 적절한 서블릿을 찾아 실행함
- e.g. Tomcat, Undertow, Jetty, ...


```java
package jakarta.servlet

import java.io.IOException;

public interface Servlet{

	public void init(ServletConfig config) throws ServletException;
	public ServletConfig getServletConfig();
	public void service(ServletRequest req, ServletResponse res)  
	        throws ServletException, IOException;
	public String getServletInfo();
	public void destroy();
}

```

Life-cycle 메서드 세개 (`init`, `service`, `destroy`) 와 메타 정보를 조회하기 위한 메서드 두개 (`getServletConfig`, `getServletInfo`) 를 정의한다.

