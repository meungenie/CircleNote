# CircleNote

동아리 활동 기록 및 관리를 위한 웹 플랫폼

## 프로젝트 소개

동아리 운영에 필요한 공지사항, 일정, 사진, 스터디 자료, 멤버 관리 기능을 하나의 웹사이트에서 통합적으로 제공합니다.

- **개발 기간:** 2024.11 ~ 2024.12
- **개발 인원:** 1인 (기획, 설계, 개발, 배포 전 과정)

## 주요 기능

- 홈화면: 동아리 소개 및 공지사항 관리 (관리자/일반 사용자 권한 분리)
- 캘린더: 동아리 일정 등록 및 조회
- 사진첩: 폴더별 활동 사진 업로드 및 공유
- 스터디: 스터디룸 생성 및 자료 기록
- 멤버: 동아리 구성원 정보 관리

## 기술 스택

| 구분 | 기술 |
| --- | --- |
| Frontend | React.js, Axios, CSS |
| Backend | Node.js, Express.js, MongoDB, Mongoose |
| 인증 | JWT, bcrypt |
| 배포 | AWS EC2 (백엔드), S3 + CloudFront (프론트엔드), Route 53 (도메인), HTTPS |

## 아키텍처

```
[사용자] → Route 53 → CloudFront → S3 (React 정적 파일)
                                  ↓
                          EC2 (Express API 서버) → MongoDB Atlas
```

## 실행 방법

```bash
# 클론
git clone https://github.com/meungenie/CircleNote.git
cd CircleNote

# 백엔드
cd server
npm install
npm start

# 프론트엔드
cd ../client
npm install
npm start
```
