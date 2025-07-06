# Kolektt 정적 웹페이지

Kolektt 앱을 위한 정적 웹페이지 모음입니다. GitHub Pages를 통해 배포되어 이메일 인증, 회원가입 완료 등의 프로세스에서 사용됩니다.

## 📋 페이지 목록

### 1. 개인정보처리방침 (`index.html`)
- **URL**: `https://objktt.github.io/kolektt-privacy-policy/`
- **용도**: 앱 내 개인정보처리방침 링크
- **특징**: 반응형 디자인, 깔끔한 레이아웃

### 2. 이메일 인증 완료 (`verified.html`)
- **URL**: `https://objktt.github.io/kolektt-privacy-policy/verified.html`
- **용도**: 이메일 인증 성공 시 리디렉션 페이지
- **특징**: 
  - 성공 아이콘과 애니메이션
  - 앱으로 돌아가기 버튼 (딥링크 지원)
  - 다음 단계 안내

### 3. 인증 오류 (`error.html`)
- **URL**: `https://objktt.github.io/kolektt-privacy-policy/error.html`
- **용도**: 이메일 인증 실패 시 표시
- **특징**:
  - URL 파라미터로 오류 정보 표시
  - 문제 해결 방법 안내
  - 고객지원 연결
  - 기술적 세부사항 토글 기능

### 4. 회원가입 완료 (`welcome.html`)
- **URL**: `https://objktt.github.io/kolektt-privacy-policy/welcome.html`
- **용도**: 회원가입 완료 축하 페이지
- **특징**:
  - 환영 메시지와 축하 애니메이션
  - 앱 기능 소개
  - 커뮤니티 통계
  - 그라디언트 배경과 현대적 디자인

## 🚀 사용 방법

### Supabase 인증 설정

1. **이메일 인증 리디렉션 URL 설정**
```
성공: https://objktt.github.io/kolektt-privacy-policy/verified.html
실패: https://objktt.github.io/kolektt-privacy-policy/error.html
```

2. **회원가입 완료 리디렉션**
```
환영: https://objktt.github.io/kolektt-privacy-policy/welcome.html
```

### URL 파라미터

#### `error.html`
- `error` 또는 `error_code`: 오류 코드
- `error_description` 또는 `message`: 오류 메시지

예시:
```
https://objktt.github.io/kolektt-privacy-policy/error.html?error=token_expired&error_description=인증%20링크가%20만료되었습니다
```

#### `welcome.html`
- `name` 또는 `user_name`: 사용자 이름

예시:
```
https://objktt.github.io/kolektt-privacy-policy/welcome.html?name=홍길동
```

## 📱 딥링크 지원

모든 페이지는 "앱으로 돌아가기" 버튼을 통해 딥링크를 지원합니다:

- **인증 완료**: `kolektt://verified`
- **오류 페이지**: `kolektt://error`
- **환영 페이지**: `kolektt://welcome`

앱이 설치되지 않은 경우 각각의 앱스토어로 리디렉션됩니다:
- Android: Google Play Store
- iOS: App Store

## 🎨 디자인 특징

- **일관된 브랜딩**: 모든 페이지에서 Kolektt 브랜드 컬러 사용
- **반응형 디자인**: 모바일과 데스크톱 모두 지원
- **접근성**: WCAG 가이드라인 준수
- **현대적 UI**: 그라디언트, 섀도우, 애니메이션 활용

## 🔧 개발 및 배포

### 로컬 개발
```bash
# 로컬 서버 실행 (Python 3)
python -m http.server 8000

# 또는 Node.js
npx serve .
```

### GitHub Pages 배포
1. 파일을 main 브랜치에 커밋
2. GitHub에서 자동으로 배포
3. `https://objktt.github.io/kolektt-privacy-policy/`에서 확인

## 📞 연락처

- **개발 문의**: privacy@kolektt.com
- **고객 지원**: support@kolektt.com

## 📄 라이선스

Copyright (c) 2025 Kolektt. All rights reserved.
