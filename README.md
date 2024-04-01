# FeignClient
 - FeignClient는 REST call을 추상화한 Spring Cloud Netflix 라이브러리

FeignClint를 사용하면 HTTP Client를 직접 구현하지 않고도 REST API를 호출할 수 있습니다.
인터페이스를 통해 REST API의 엔드포인트를 정의하고, 해당 인터페이스를 FeignClient로 등록하면 됩니다.

FeignClient는 RestTemplate보다 직관적이고 간단하며 코드가 짧다는 장점이 있습니다.
또한, Spring Cloud의 다른 기능들과 원활하게 통합되어 서비스 디스커버리, 로드 밸런싱 등의 기능을 사용하면서 FeignClient를 활용할 수 있습니다.

# FeignClient의 특징
1. 간결한 API 정의
  - @FeignClient 어노테이션을 사용하여 타겟 서비스 URL과 이름을 명시
  - API 엔드포인트를 나타내는 메소드를 @GetMapping, @PostMapping, @PutMapping 등의 어노테이션으로 정의
  - 인터페이스를 통해 간결하고 직관적인 방식으로 API 호출을 수행
2. 다양한 기능 지원
  - 기본적인 HTTP 메소드 (GET, POST, PUT, DELETE) 지원
  - 템플릿 엔진을 통한 URL 동적 파라미터 설정 가능
  - Timeout, Retry 등의 설정을 통해 네트워크 통신 제어
  - Query Parameterm Header, Body등의 데이터 전송
  - JSON, XML등 다양한 데이터 포멧 지원
  - Spring Cloud Config Server를 통한 설정 자동 로드
3. 쉬운 통합
  - Spring Boot Starter를 통해 간편하게 설정 및 사용
  - Spring Cloud Discovery와 연동하여 서비스 주소 자동 등록 및 해결
  - Ribbon Load Balancer를 통한 자동 로드 밸런싱
  - Hystrix Circuit Breaker를 통한 에러 처리 및 회복성 강화
4. 확장성
  - Feign Decoder/Encoder를 통해 커스터마이징 가능
  - Feign Fallback/Hystrix Command를 통해 에러 처리 및 회복성 강화
  - Feign Interceptor를 통해 추가 기능 및 로깅 구현


