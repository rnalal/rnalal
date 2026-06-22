<h1 align="center">👋 Hi , I'm Jaeyoung Jeon (전재영)</h1>
<p align="center">안녕하세요. 성능 개선을 통해 사용자가 다시 찾고 싶은 서비스를 만드는 개발자, 전재영입니다.</p>

---

## 📁 Portfolio Projects

### 🧷 JBB 베이킹 커뮤니티 프로젝트
🔗 [GitHub Repo 보기](https://github.com/rnalal/JBB_NEW) <br>
🌐 [cafe24 배포 - 사용자 페이지] (https://jaeyoung2.store/jbb/) <br>
🌐 [cafe24 배포 - 관리자 페이지] (https://jaeyoung2.store/jbb/adminlogin) | (임시ID: admin, 임시PWD: 1234)

> 실시간 알림기능과 사용자 중심 개선을 적용한 베이킹 커뮤니티 웹 서비스

- WebSocket+STOMP 기반 양방향 통신 구조 설계해 Polling 방식의 불필요한 HTTP 요청 제거 및 서버 푸시 기반 실시간 알림 서비스 구현
- HttpSession 기반 조회 상태 관리 로직을 구현해 동일 사용자의 반복 조회로 발생하던 조회수 중복 증가 문제 해결 및 사용자 행동 기반 데이터 정합성과 조회수 신뢰성 확보
- PRG 패턴 적용해 새로고침 시 발생하는 조회수 중복 증가 문제를 해결하고, 중복 요청 방지 및 데이터 정합성을 확보하는 요청 흐름 구조를 구현

---

### 🧷 RUNGAME 러닝 게임 프로젝트
🔗 [GitHub Repo 보기](https://github.com/rnalal/run-game) <br>
🌐 [cafe24 배포 - 사용자 페이지] (https://jaeyoung2.store/) <br>
🌐 [cafe24 배포 - 관리자 페이지] (https://jaeyoung2.store/rg-admin/login) | (임시ID: admin@naver.com , 임시PWD: 123456789)

> 실시간 랭킹 시스템과 게임이벤트 처리성능 최적화를 구현한 러닝 게임 웹 서비스

- Redis, Spring Cache 기반 실시간 리더보드 구축 -> 조회 성능 99.0% 개선
- N+1 문제 해결로 사용자 조회 쿼리를 10회 -> 1회 감소
- JdbcTemplate Batch Insert, Session 누적 집계, 단일 조회 기반 상태 복원 구조로 이벤트 처리 병목 개선
  * API 응답 시간 최대 87.6% 개선, 종료 처리 75.3% 단축, 상태 복원 조회 19회 -> 1회 감소
- 단일 집계 쿼리, Spring Cache, 복합 인덱스 적용해 관리자 통계 및 이벤트 검색 성능 개선
  * 세션 차트 33.5%, 이벤트 차트 61.0% 응답 시간 단축, 조회 범위 42,602건 -> 1~80건으로 감소, Full Table Scan을 Index Range Scan 전환

---

### 🧷 GOBONG 반려동물 커뮤니티 프로젝트
🔗 [GitHub Repo 보기](https://github.com/rnalal/gobong)

> 반려동물 기반 SNS 커뮤니티 서비스

- 이미지 데이터를 DB에 직접 저장하던 구조를 파일 서버 저장 및 경로 관리 방식으로 개선해서 DB 부하를 줄이고, 파일과 메타데이터를 분리한 유지보수 가능한 저장 구조 설계

---
## 🧩 Certification
- 정보처리기사
- SQLD
- 컴퓨터활용능력 2급
- 리눅스마스터 2급
---

## 🛠️ Tech Stack
### 💻 Backend
- Java17, Spring Boot, Spring Security, JPA, MyBatis
### 🌐 Frontend
- HTML, CSS, JavaScript
### 🗄️ Database
- MySQL, Redis
### ⚙️ Etc
- Redis Sorted Set, Spring Cache, Query Optimization, Docker, Docker Compose, Git, GitHub

---

## 📫 Contact
- Blog: 🔗[기술 블로그 보러가기](https://velog.io/@youngk8251/posts)
