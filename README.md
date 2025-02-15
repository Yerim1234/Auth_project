<h1>Auth project</h1>

## **1. 무엇을 개발할 것인가? - Auth 관련 기능 구현**

- **목표 정의**
  - 사용자가 로그인, 회원가입, 로그아웃을 할 수 있는 시스템.
  - 비밀번호 보안 및 인증 절차를 강화 (e.g., 비밀번호 암호화, 토큰 기반 인증 등).
  - 에러 처리 (e.g., 잘못된 입력, 중복 계정 생성 등).
- **추가 고려 사항**
  - 소셜 로그인 연동 (미래 확장을 위해).
  - 사용자 세션 관리 (로컬 스토리지, 쿠키, 서버 세션 등).

---

## **2. 사용 스택 고안**

- **프론트엔드**
  - HTML, CSS, JavaScript (Vanilla로 진행).
- **백엔드**
  - Open API로 구현 예정
- **기타**
  - Postman 또는 Thunder Client로 API 테스트.
  - ESLint와 Prettier를 사용하여 코드 품질 관리.

---

## **3. 프로젝트 구현**

### 1. **초기 설정**

- 프로젝트 디렉토리 생성 및 초기화 (`npm init`, `.gitignore` 설정).
- ESLint 및 Prettier 설정 파일 추가.
- CSS 기본 스타일 파일 작성.

### 2. **UI 설계**

- 회원가입, 로그인, 로그아웃 UI 초안 설계.
- 반응형 레이아웃 고려.
- **할 일**
  - [ ] 회원가입 폼: 이메일, 비밀번호 입력 및 제출 버튼, 이메일 인증
  - [ ] 로그인 폼: 이메일, 비밀번호 입력 및 제출 버튼.
  - [ ] 로그아웃 버튼.

### 3. **API 설계**

- **회원가입 API**
  - HTTP Method: POST `/auth/signup`
  - 요청: `{ email, password }`
  - 응답: 성공 메시지 또는 에러 메시지.
- **로그인 API**
  - HTTP Method: POST `/auth/login`
  - 요청: `{ email, password }`
  - 응답: JWT 토큰 또는 에러 메시지.
- **로그아웃 API**
  - HTTP Method: POST `/auth/logout`
  - 요청: 토큰.
  - 응답: 성공 메시지.

### 4. **기능 구현**

- **회원가입**
  - 비밀번호 암호화 및 데이터베이스 저장.
  - 이메일 중복 체크.
- **로그인**
  - 입력값 검증 및 비밀번호 비교.
  - JWT 생성 후 클라이언트 전달.
- **로그아웃**
  - 서버에서 JWT 무효화 (선택 사항).

### 5. **테스트 작성**

- Jest를 사용하여 유닛 테스트 및 통합 테스트 작성.
- 테스트 범위:
  - 이메일 중복 확인 기능.
  - 비밀번호 암호화 및 비교.
  - JWT 발급 및 검증.

---

## **4. 프로젝트 배포**

### 1. **로컬 배포**

- Node.js 서버 실행 및 Postman으로 API 테스트.
- 브라우저에서 프론트엔드 확인.

### 2. **클라우드 배포**

- 플랫폼 선택 (Heroku, Vercel, Render 등).
- CI/CD 도구 활용 (GitHub Actions, Netlify).
- 배포 후 테스트:
  - 회원가입 및 로그인 정상 동작 확인.
  - 비정상 입력 처리 확인.
# Auth_project
