<h1 align="center">👋 Hi , I'm Jaeyoung Jeon (전재영)</h1>
<p align="center">안녕하세요. 성능 개선을 통해 사용자가 다시 찾고 싶은 서비스를 만드는 개발자, 전재영입니다.</p>

---

## 📁 Portfolio Projects

### 🧷 JBB 베이킹 커뮤니티 프로젝트
🔗 [GitHub Repo 보기](https://github.com/rnalal/JBB_NEW) <br>
🌐 [cafe24 배포 - 사용자 페이지] (https://jaeyoung2.store/jbb/) <br>
🌐 [cafe24 배포 - 관리자 페이지] (https://jaeyoung2.store/jbb/adminlogin) | (임시ID: admin, 임시PWD: 1234)

> 게시글, 회원 관리와 Redis/Caffeine 기반 성능 최적화를 적용한 베이킹 커뮤니티 웹 서비스

- Redis INCR + Scheduler 기반 조회수 Write-Behind 구조 구현
  - 조회수 10회 증가 기준 DB UPDATE 10회 -> 1회, UPDATE 횟수 약 90% 감소
  - Soft Delete와 실제 장애를 구분하고, 장애 시 Key 유지/재시도 및 Key별 예외 처리로 재처리/부분 실패 격리 구조 확보
- Caffeine Cache 적용 및 데이터 의존성 기반 선택적 캐시 무효화 구조 개선
  - 게시글 약 10,000건 기준 /board/list 39.46ms -> 1.73ms, 약 95.6% 응답시간 감소
  - 동일 요청 3회 기준 주요 SQL 실행 횟수 9회 -> 3회, 약 66.7% 감소
  - afterCommit() 기반 캐시 무효화로 DB-Cache 정합성 강화
- 게시글 삭제 구조를 Hard Delete에서 Soft Delete 기반 LifeCycle로 확장
  - Soft Delete -> 관리자 복구 -> 30일 경과 미복구 데이터 Hard Delete Batch 구조 구현
  - 삭제 이력 관리 및 DB/이미지/Redis 조회수 Key/인기글 Member 정리
  - 건별 REQUIRES_NEW Transaction으로 Batch 부분 실패 격리

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
