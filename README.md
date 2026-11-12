<div align="center">

<img width="300" alt="HASHI 로고" src="https://github.com/user-attachments/assets/5298892e-9135-49bb-b2ac-5ea650c8ea88" />

# HASHI Server

**발견부터 예약까지, 포기 없이**

**취향에 맞는 일식당을 발견하고, 예약과 방문 리뷰까지 연결하는 HASHI의 백엔드 서버입니다.**

[서비스](https://hashi.kr) · [클라이언트 저장소](https://github.com/hwistlezz/HASHI-CLIENT) · [개발 API](https://dev-api.hashi.kr) · [Swagger](https://dev-api.hashi.kr/swagger-ui/index.html) · [개발 컨벤션](docs/conventions/00-index.md)

</div>

## HASHI

HASHI는 한국인 여행자가 일본에서 취향에 맞는 식당을 찾고 예약할 수 있도록 돕는 서비스입니다. 큐레이션으로 식당을 추천하고, 일본어로 진행되는 예약 절차를 대신 처리해 실제 방문까지 연결합니다.

서버는 도메인 경계를 유지하면서도 빠르게 개발하고 배포할 수 있도록 Spring Modulith 기반 모듈러 모놀리스로 구성했습니다. 외부에는 하나의 애플리케이션으로 배포하되, 내부에서는 식당·예약·리뷰·포인트 등 각 도메인의 책임과 의존 방향을 분리합니다.

<img width="960" alt="HASHI 맛집 큐레이션과 예약 화면" src="https://github.com/user-attachments/assets/cdb8f00b-8e43-41a9-9e03-c152bc3c5a9e" />

<img width="960" alt="일본 맛집 큐레이션과 예약 대행 서비스 소개" src="https://github.com/user-attachments/assets/66913dff-dc2f-4c9f-894d-075095479c49" />

## Key Features

| 영역 | 제공 기능 |
| --- | --- |
| 식당 탐색 | 식당 목록과 정렬, 키워드 자동완성, 검색어 추천, 랜덤 추천, 식당·매장·메뉴 상세 조회 |
| 예약 | 등록 식당 예약, 어디든지 예약, 내 예약 목록·상세 조회, 진행 중 예약 취소와 사용 포인트 복구 |
| 리뷰 | 예약 단위 작성 가능 여부 확인, 리뷰 작성 화면 정보 조회, 식당 리뷰·내 리뷰 조회 및 삭제 |
| 인증·회원 | 카카오 OAuth 로그인, JWT 발급·재발급, 온보딩, 내 정보와 프로필 요약 조회 |
| 포인트 | 보유 포인트 조회, 예약 시 차감, 진행 중 예약 취소 시 복구 |
| 콘텐츠·관리 | 매거진 배너·목록, 식당·매거진·예약·사용자 관리자 기능 |
| 이미지 | S3 Presigned URL 일괄 발급, 클라이언트 직접 업로드, CloudFront 기반 이미지 제공 |

<details>
<summary>주요 화면 보기</summary>

<img width="960" alt="맛집 탐색" src="https://github.com/user-attachments/assets/22453cb0-5cab-4d8e-95c2-743e6e80fb0c" />

<img width="960" alt="식당 예약 신청" src="https://github.com/user-attachments/assets/d02a100f-44d0-4ec7-8d3f-7c2cc4b8c9aa" />

<img width="960" alt="어디든지 예약" src="https://github.com/user-attachments/assets/093c808c-ab57-4439-a1be-265e8b964929" />

<img width="960" alt="예약 상태 확인" src="https://github.com/user-attachments/assets/b49287ac-b8e8-4c83-81a1-951926a4e488" />

<img width="960" alt="방문 후 리뷰" src="https://github.com/user-attachments/assets/caa6b47f-1b82-43d1-a5f6-bf7f470d2e5c" />

</details>

## Tech Stack

### Core

![Java 21](https://img.shields.io/badge/Java-21-E76F00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot 3.5.15](https://img.shields.io/badge/Spring_Boot-3.5.15-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Modulith 1.4.3](https://img.shields.io/badge/Spring_Modulith-1.4.3-6DB33F?style=for-the-badge&logo=spring&logoColor=white)

### Data & Storage

![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![MySQL 8](https://img.shields.io/badge/MySQL-8-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=for-the-badge&logo=flyway&logoColor=white)
![Amazon S3](https://img.shields.io/badge/Amazon_S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white)
![CloudFront](https://img.shields.io/badge/Amazon_CloudFront-8C4FFF?style=for-the-badge)

### Security & API

![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-272727?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![Kakao OAuth](https://img.shields.io/badge/Kakao_OAuth-FFCD00?style=for-the-badge&logo=kakao&logoColor=black)
![OpenAPI](https://img.shields.io/badge/OpenAPI-6BA539?style=for-the-badge&logo=openapiinitiative&logoColor=white)

### Infrastructure & Observability

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Loki](https://img.shields.io/badge/Loki-2C3642?style=for-the-badge&logo=grafana&logoColor=white)

### Testing

![JUnit 5](https://img.shields.io/badge/JUnit-5-25A162?style=for-the-badge&logo=junit5&logoColor=white)
![Mockito](https://img.shields.io/badge/Mockito-4A7A3C?style=for-the-badge)
![H2](https://img.shields.io/badge/H2-09476B?style=for-the-badge)

### 주요 기술 선택

- **모듈러 모놀리스**: 하나의 배포 단위를 유지하면서 모듈 경계와 참조 방향을 코드 수준에서 검증합니다.
- **Flyway**: 환경마다 동일한 순서로 스키마를 적용하고 변경 이력을 저장소에서 관리합니다.
- **Redis**: 만료 시간이 중요한 Refresh Token과 온보딩 토큰을 애플리케이션 메모리와 분리해 관리합니다.
- **Presigned URL**: 이미지 파일이 API 서버를 거치지 않고 S3로 직접 업로드되도록 해 서버의 네트워크 부하를 줄입니다.
- **Prometheus·Loki·Grafana**: 요청 지연과 자원 상태를 메트릭으로, 요청별 실행 흐름을 로그로 함께 추적합니다.

## Modular Monolith

모듈 간 호출은 공개 Port를 통해 수행하고, 다른 모듈의 내부 구현이나 Repository를 직접 참조하지 않습니다. Spring Modulith 검증 테스트로 모듈 경계와 순환 의존을 확인합니다.

| 모듈 | 책임 |
| --- | --- |
| `auth` | 카카오 로그인, JWT 발급·재발급, 인증 사용자 조회 |
| `user` | 온보딩, 사용자 정보와 프로필 관리 |
| `restaurant` | 식당·매장·메뉴 조회, 검색과 추천 |
| `reservation` | 등록 식당·어디든지 예약, 상태 관리와 취소 |
| `review` | 예약 기반 리뷰 작성, 식당·사용자 리뷰 조회 |
| `point` | 포인트 잔액과 예약 연계 증감 처리 |
| `magazine` | 매거진 배너·목록과 관리자 편집 |
| `upload` | S3 Presigned URL 발급과 파일 조건 검증 |
| `admin` | 관리자 인증과 운영 API |
| `shared` | 특정 도메인에 속하지 않는 공통 응답·예외·유틸리티 |
| `dev` | 개발 환경 전용 지원 API |

모듈 구조와 참조 규칙은 [`architecture.md`](docs/conventions/architecture.md)에 정리되어 있으며, `ApplicationModules.verify()`로 위반 여부를 검증합니다.

## Project Structure

```text
HASHI-SERVER
├── .github
│   ├── ISSUE_TEMPLATE
│   ├── pull_request_template.md
│   └── workflows
│       ├── ci.yml
│       ├── cd-dev.yml
│       └── cd-prod.yml
├── docker
│   ├── grafana
│   ├── loki
│   ├── prometheus
│   ├── promtail
│   ├── docker-compose.dev.yml
│   ├── docker-compose.monitoring.local.yml
│   └── docker-compose.prod.yml
├── docs
│   ├── conventions
│   ├── dev
│   └── infra
└── src
    ├── main
    │   ├── java/org/sopt/hashi
    │   │   ├── admin
    │   │   ├── auth
    │   │   ├── config
    │   │   ├── dev
    │   │   ├── magazine
    │   │   ├── point
    │   │   ├── reservation
    │   │   ├── restaurant
    │   │   ├── review
    │   │   ├── shared
    │   │   ├── upload
    │   │   └── user
    │   └── resources
    │       ├── db/migration
    │       ├── application.yml
    │       └── logback-spring.xml
    └── test
```

각 도메인 모듈은 책임에 따라 다음 패키지를 사용하며, 필요하지 않은 패키지는 생략합니다.

```text
code     도메인별 성공·오류 코드
domain   Entity, Repository와 도메인 모델
service  비즈니스 로직과 외부 공개 Port
dto      요청·응답 및 내부 전달 객체
web      Controller와 API 문서화 인터페이스
```

## Observability

### Logging

- Actuator 경로를 제외한 애플리케이션 요청마다 `requestId`를 생성하고 인증된 요청에는 `userId`를 MDC에 기록합니다.
- 응답의 `X-Request-Id` 헤더로 클라이언트 요청과 서버 로그를 연결합니다.
- 개발·운영 로그는 JSON으로 출력하고 Promtail이 컨테이너 로그를 Loki로 전송합니다.
- 예약·리뷰·포인트·관리 작업에는 식별자와 상태, 금액, 평점 등 처리 결과를 기록합니다.
- Docker 로그는 크기와 파일 수를 제한해 디스크 사용량을 관리합니다.

### Monitoring

- Actuator와 Micrometer가 HTTP, JVM, GC, CPU, HikariCP 메트릭을 생성합니다.
- Prometheus가 애플리케이션 메트릭을 수집하고 Grafana가 메트릭과 Loki 로그를 함께 시각화합니다.
- 공통 Grafana 대시보드와 datasource 설정은 `docker/grafana`에서 코드로 관리합니다.
- 개발·운영 환경의 Prometheus 메트릭 엔드포인트는 외부에 직접 공개하지 않습니다.

## Documents

| 문서 | 설명 |
| --- | --- |
| [컨벤션 인덱스](docs/conventions/00-index.md) | 개발 문서 전체 목록 |
| [아키텍처](docs/conventions/architecture.md) | 모듈 경계와 의존 방향 |
| [코딩 스타일](docs/conventions/coding-style.md) | 패키지·계층·네이밍 규칙 |
| [Git Convention](docs/conventions/git-convention.md) | 이슈·브랜치·커밋·PR 규칙 |
| [인증](docs/conventions/auth.md) | JWT와 인증 처리 규칙 |
| [에러 처리](docs/conventions/error-handling.md) | 공통 응답과 에러 코드 규칙 |
| [데이터베이스](docs/conventions/database.md) | JPA와 Flyway 규칙 |
| [테스트](docs/conventions/testing.md) | 테스트 범위와 작성 기준 |
| [개발 서버 배포](docs/infra/dev-deploy.md) | 개발 인프라와 CD 운영 절차 |
