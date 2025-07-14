# Lagunkoi - AI 라이프스타일 관리 앱

라이프스타일 유형에 맞춘 개인화된 일정 관리와 루틴 추천을 제공하는 AI 기반 React Native 앱입니다.

## 🚀 주요 기능

- **AI 챗봇**: 자연스러운 대화로 일정과 루틴 관리
- **라이프스타일 분석**: 개인 성향에 맞춘 맞춤형 추천
- **스마트 캘린더**: 음성 입력 및 외부 캘린더 연동
- **루틴 관리**: 습관 형성을 위한 체계적인 관리

## 📱 기술 스택

- **Frontend**: React Native + Expo
- **Navigation**: Expo Router (파일 기반 라우팅)
- **State Management**: Zustand
- **Styling**: Custom Design System
- **Backend**: Supabase
- **AI**: OpenAI API

## 🛠️ 설치 및 실행

### 1. 의존성 설치
```bash
npm install --legacy-peer-deps
```

### 2. 환경 변수 설정
```bash
cp env.example .env
# .env 파일을 열어 필요한 키값들을 입력하세요
```

### 3. 개발 서버 실행
```bash
npm start
```

### 4. 플랫폼별 실행
- iOS: `i` 키 입력
- Android: `a` 키 입력
- Web: `w` 키 입력

## 📁 프로젝트 구조

```
lagunkoi/
├── app/                    # Expo Router 페이지
│   ├── (tabs)/            # 탭 네비게이션
│   ├── (auth)/            # 인증 관련 페이지
│   └── onboarding/        # 온보딩 플로우
├── components/            # 재사용 가능한 컴포넌트
├── design-system/         # 디자인 토큰 및 기본 컴포넌트
├── services/              # API 및 외부 서비스
├── stores/                # Zustand 상태 관리
├── hooks/                 # 커스텀 훅
└── utils/                 # 유틸리티 함수
```

## 🎨 디자인 시스템

프로젝트는 일관된 UI/UX를 위한 자체 디자인 시스템을 포함합니다:

- **Typography**: 계층적 텍스트 스타일
- **Colors**: 라이트/다크 테마 지원
- **Spacing**: 일관된 여백 시스템
- **Components**: Button, Card, Typography 등

## 🔒 보안 주의사항

- API 키는 절대 클라이언트 코드에 직접 포함하지 마세요
- 민감한 작업은 서버 사이드에서 처리하세요
- 환경 변수는 `.gitignore`에 포함되어 있는지 확인하세요

## 📝 개발 가이드

### 새로운 페이지 추가
```typescript
// app/새페이지.tsx
export default function NewPage() {
  return <View>...</View>
}
```

### 상태 관리
```typescript
// stores/newStore.ts
export const useNewStore = create((set) => ({
  // 상태와 액션 정의
}))
```

## 🐛 알려진 이슈

- expo-calendar는 현재 사용하지 않음 (권한 이슈)
- 음성 인식은 모의 구현 상태
- 외부 캘린더 연동은 추가 개발 필요

## 📄 라이선스

이 프로젝트는 개인 사용 목적으로 개발되었습니다. 