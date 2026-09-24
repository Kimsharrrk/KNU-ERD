# 🏫 SW중심대학사업 관리 시스템 — ERD & 순서도

> **경북대학교 데이터베이스프로그래밍** 팀 프로젝트 — DB 설계 문서

---

## 📦 파일 목록

| 파일 | 설명 |
|------|------|
| `SW사업관리_ERD_순서도.html` | ⭐ **메인 문서** — 브라우저에서 바로 열어서 확인 |
| `SW사업관리_전체_ERD_Chen_Clean.pdf` | Chen 표기법 전체 ERD (무한 확대 가능) |
| `SW사업관리_전체_ERD_Chen_Clean.png` | Chen 표기법 전체 ERD 이미지 |
| `dbdiagram_ERD.dbml` | [dbdiagram.io](https://dbdiagram.io) 용 DBML 코드 |

---

## 🗂️ 시스템 개요

| 항목 | 수치 |
|------|------|
| 엔터티 (테이블) | **28개** |
| 속성 (컬럼) | **212개** |
| 외래키 (FK) | **46개** |
| 업무 도메인 | **6개** |
| 순서도 | **5개** |

---

## 🎨 도메인 구성

| 색상 | 도메인 | 엔터티 |
|------|--------|--------|
| 🟪 | **공통/계정** | USER, ROLE, USER_ROLE, COMMON_CODE_GROUP, COMMON_CODE, CHANGE_LOG |
| 🟨 | **학생 관리** | DEPARTMENT, STUDENT, ENROLLMENT_HISTORY, STUDENT_INFO_REQUEST |
| 🟦 | **TOPCIT** | TOPCIT_ROUND, TOPCIT_SCORE |
| 🟥 | **마일리지** | PROGRAM, MILEAGE_POLICY, MILEAGE_APPLY, ATTACH_FILE, MILEAGE_LEDGER |
| 🟩 | **예산·지출** | BUDGET_PROJECT, BUDGET_ITEM, PROJECT_BUDGET, PROFESSOR, EXPENSE, STUDENT_STIPEND, BUDGET_CHANGE_HIST |
| 🟧 | **만족도** | SURVEY, SURVEY_QUESTION, SURVEY_RESPONSE, SURVEY_ANSWER |

---

## 🚀 보는 방법

### 1. HTML 메인 문서 (추천)
```
SW사업관리_ERD_순서도.html 파일을 Chrome/Safari로 열기
```
- 상단 네비게이션으로 원하는 섹션 바로 이동
- 전체 ERD, 도메인별 ERD, 순서도 5개, 스키마 목록 포함

### 2. Chen 표기법 ERD (PDF)
```
SW사업관리_전체_ERD_Chen_Clean.pdf 를 열고 확대해서 보기
```
- 파란 네모 = 엔터티, 초록 타원 = 속성, 검은 마름모 = 관계

### 3. dbdiagram.io
```
dbdiagram_ERD.dbml 내용을 복사 → https://dbdiagram.io 에 붙여넣기
```

---

## 📋 순서도 목록

1. 🔑 **로그인 & 인증** — 비밀번호 해시 검증 → 역할 조회 → 세션 발급
2. 📝 **학생 인적사항 수정 요청** — 학생 요청 등록 → 관리자 승인/반려
3. ⭐ **마일리지 적립 신청** — 신청 → 증빙 첨부 → 승인 → 원장 적립
4. 💰 **예산 지출 승인** — 지출 등록 → 승인 → 예산 차감
5. 📋 **만족도 조사 응답** — 조사 생성 → 학생 응답 → 완료

---

*경북대학교 소프트웨어학부 · 2026-09-24*
