# 🧀 치이이즈 : 딱 7일만 열리는 특별한 공유 앨범 서비스
> 🔗 서비스 링크: [https://say-cheese.me](https://say-cheese.me)

![웹 썸네일](https://github.com/user-attachments/assets/f5a6c97a-21b9-4dff-a7b7-8c12fe6e27db)

## 👨‍👩‍👧‍👦 Members 

| **김규태** | **김건우** | **우다현** | **주정빈** |
| :--------: | :-----------: | :--------: |:-----------:|
|<a href="https://github.com/dasosann"><img src="https://avatars.githubusercontent.com/u/183822817?v=4" width="150"> | <a href="https://github.com/caseBread"><img src="https://avatars.githubusercontent.com/u/92029332?v=4" width="150"> | <a href="https://github.com/dahyun24"><img src="https://avatars.githubusercontent.com/u/123882512?v=4" width="150"> | <a href="https://github.com/zyovn"><img src="https://avatars.githubusercontent.com/u/166782961?v=4" width="150"> |
| `frontend` | `frontend` | `backend` | `backend` |

## 📜 API 명세서
[[Swagger] 🧀 치이이즈 API 명세서](https://dev.say-cheese.me/swagger-ui/index.html#/)

## 🗃️ ERD
<img width="1680" height="862" alt="Cheeeese (2)" src="https://github.com/user-attachments/assets/a523f9d5-a40e-44bf-8d5a-64b072469454" />

## 🏛️ System Architecture
<img width="3812" height="2232" alt="image" src="https://github.com/user-attachments/assets/2f90fde1-3a95-4ed9-8720-009bd289c829" />

## 🚀 Frontend Tech Stack
| 기술 스택                            | 설명                                                                           |
| -------------------------------- | ---------------------------------------------------------------------------- |
| **Next.js 15 (App Router)**      | - SSR·SSG 지원으로 초기 로딩 및 SEO 최적화<br/>- 이미지·폰트 최적화 등 내장 기능으로 고성능 웹 구축           |
| **TypeScript**                   | - 정적 타입 시스템으로 컴파일 단계에서 오류 사전 방지                                              |
| **Tailwind CSS**                 | - Token Studio 기반 디자인 토큰 → Tailwind 변환<br/>- 유틸리티 클래스 기반 빠른 UI 개발, 최소 CSS 번들 |
| **ShadCn UI**                    | - WA 접근성 표준 준수<br/>- 코드 직접 소유 → 완전한 커스터마이징 가능<br/>- 검증된 UI 패턴으로 개발 시간 절약     |
| **Zustand**                      | - 간결한 전역 상태 관리<br/>- 업로드 대기열·다중 선택 등 복잡 상태도 직관적으로 관리                         |
| **Tanstack Query (React Query)** | - 서버 데이터 캐싱·동기화 최적화<br/>- 무한 스크롤 등 사용자 경험 강화 기능 제공                           |
| **Github Actions**               | - PR 테스트/린팅 자동화로 품질 관리<br/>- 빌드→배포까지 자동화된 CI/CD 구축                           |
| **Lucide React**                 | - SVG 기반의 가볍고 일관된 아이콘 제공                                                     |
| **Framer Motion**                | - 부드러운 앱 수준의 인터랙션 구현<br/>- 선언적 애니메이션으로 직관적인 UI 동작 개발                         |
| **Vitest**                       | - Vite 기반 초고속 테스트 러너<br/>- 리팩토링 시 안정성을 보장하는 테스트 환경 제공                        |

## 🛠 Backend Tech Stack
| 기술 스택                                            | 설명                                                                                                        |
| ------------------------------------------------ | --------------------------------------------------------------------------------------------------------- |
| **Spring Boot 3.5.6 + Java 21**                  | - 최신 LTS로 안정성과 성능 강화<br/>- GC 성능 개선 및 높은 생산성으로 유지보수성 극대화                                                  |
| **Redis**                                        | - 인메모리 기반 초고속 조회 성능<br/>- Cache-Aside로 앨범/사진 데이터 조회 최적화<br/>- ZSET 기반 만료 스케줄러로 일관성 보장                     |
| **MySQL**                                        | - 안정성과 복구력이 검증된 RDBMS<br/>- 트랜잭션 기반 일관성 확보<br/>- 구조화된 스키마 설계에 적합                                          |
| **JPA**                                          | - ORM 기반으로 SQL 반복 작성 부담 제거<br/>- 도메인 모델 중심 설계와 자연스럽게 결합<br/>- 생산성과 유지보수성 향상                               |
| **Python + Pillow (PIL) - Cloud Functions**      | - 이미지 회전/리사이징/WebP 변환 등 최적화<br/>- Node 대비 빌드 의존성 문제 감소<br/>- 썸네일/4cut 생성 등 **서버 부하 완전 분리**                |
| **Naver Cloud Platform (NCP)**                   | - Object Storage · Cloud Functions · CDN · VPC 자연스러운 통합<br/>- 국내 트래픽에 최적화된 낮은 레이턴시<br/>- 비용·운영 효율 모두 우수   |
| **Object Storage + CDN**                         | - Presigned URL 기반으로 업로드·다운로드 처리<br/>→ 서버를 거치지 않아 트래픽 부담 0<br/>- CDN이 이미지 서빙 대부분 담당<br/>→ 글로벌 지역에서도 빠른 조회 |
| **Github Actions + Docker (CI/CD)**              | - 빌드 → 테스트 → 이미지 생성 → 배포 자동화<br/>- Docker로 환경 일관성 확보<br/>- Blue-Green 방식으로 무중단 배포 실현                      |
| **PLG (Promtail / Loki / Grafana) + Prometheus** | - 로그(Loki) + 메트릭(Prometheus) + 시각화(Grafana)로 완전한 Observability 구축<br/>- 장애 원인 추적 및 운영 효율 극대화              |
