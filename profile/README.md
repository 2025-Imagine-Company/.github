# 🎙️ SOUND A.I

> AI 음성 모델을 NFT로 발행하고, API로 활용할 수 있는 Web3 플랫폼

## 👋 About Us

SOUND A.I.는 AI 음성 기술과 블록체인을 결합하여, 개인의 목소리를 디지털 자산으로 만드는 혁신적인 서비스를 개발하고 있습니다. 사용자는 자신의 목소리를 학습시켜 AI 모델로 만들고, 이를 NFT로 발행하여 소유권을 증명하며, TTS API를 통해 수익을 창출할 수 있습니다.

## 🎯 What We Do

- **AI 음성 학습**: 사용자의 목소리를 학습하여 개인화된 AI 음성 모델 생성
- **NFT 발행**: 학습된 음성 모델을 블록체인 기반 NFT로 발행
- **API 제공**: NFT 소유자에게 TTS API 사용권 부여
- **수익 창출**: API 사용량에 따른 토큰 보상 시스템

## 🏗️ System Architecture

```
Client (Flutter)
    ↓
Backend (Spring Boot)
    ↓
AWS S3 (File Storage) + PostgreSQL (Database)
    ↓
AI Server (Flask) ← Voice Model Training
    ↓
Blockchain (Solidity) ← NFT Minting
```

### 핵심 플로우
1. **음성 업로드**: 사용자 → Backend → S3 (Presigned URL 방식)
2. **AI 학습**: S3 음성 파일 → Flask AI 서버 → 학습된 모델
3. **NFT 발행**: 학습 완료 모델 → 블록체인 민팅 → IPFS 메타데이터
4. **API 사용**: NFT 소유 확인 → TTS 변환 → 결과 반환
5. **보상 지급**: 사용량 집계 → $AUDI 토큰 보상

## 🛠️ Tech Stack

### Frontend
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

### Backend
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS_S3-569A31?style=for-the-badge&logo=amazon-s3&logoColor=white)

### AI
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

### Blockchain
![Solidity](https://img.shields.io/badge/Solidity-363636?style=for-the-badge&logo=solidity&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)

## 📊 Database Schema

### Core Tables
- **users**: 지갑 기반 사용자 정보
- **voice_files**: 업로드된 음성 파일 관리
- **voice_models**: AI 학습 모델 및 상태 관리
- **nfts**: 발행된 NFT 정보 및 소유권
- **tts_requests**: API 사용 기록
- **rewards**: 사용량 기반 보상 내역

## 🚀 Key Features

### 1. 음성 학습 및 업로드
- 30초 ~ 1분 길이의 음성 파일 업로드 (`.wav`, `.mp3`)
- 파일 크기 제한: 10MB 이하
- S3 기반 안전한 파일 저장

### 2. NFT 발행
- 학습 완료된 음성 모델을 NFT로 민팅
- IPFS 기반 메타데이터 저장
- 블록체인 상 소유권 증명

### 3. TTS API
- NFT 소유자만 해당 음성으로 TTS 생성 가능
- RESTful API 제공
- 사용량 추적 및 보상 연계

### 4. 보상 시스템
- API 사용량 기반 $AUDI 토큰 보상
- 월별 사용 통계 및 보상 내역 제공

## 📋 API Endpoints

### Authentication
- `POST /auth/login` - 지갑 서명 기반 로그인
- `GET /auth/me` - 사용자 정보 조회

### Voice Management
- `POST /voice/upload` - 음성 파일 업로드
- `GET /voice/status/{model_id}` - 학습 상태 조회
- `GET /voice/result/{model_id}` - 학습 결과 및 미리듣기

### NFT Operations
- `POST /nft/mint` - NFT 발행
- `GET /nft/list/{wallet}` - 보유 NFT 목록
- `GET /nft/{token_id}/metadata` - NFT 메타데이터

### TTS API
- `POST /api/tts` - TTS 변환 요청
- `GET /api/usage/{wallet}` - 사용 기록 조회

### Rewards
- `GET /reward/{wallet}` - 보상 내역 조회

## 📅 Development Timeline

### Phase 1: MVP 개발 (2024.08)
- [x] 시스템 아키텍처 설계
- [x] DB 스키마 설계
- [x] API 엔드포인트 정의
- [x] 기술 스택 확정
- [ ] 개발 환경 구축

### Phase 2: 핵심 기능 구현 (2024.09-10)
- [ ] 음성 업로드 및 S3 연동
- [ ] AI 음성 학습 파이프라인
- [ ] 스마트 컨트랙트 개발
- [ ] NFT 민팅 기능

### Phase 3: 통합 및 테스트 (2024.11)
- [ ] 프론트엔드-백엔드 연동
- [ ] TTS API 구현 및 테스트
- [ ] 보상 시스템 구현
- [ ] 통합 테스트

## 👥 Team

| Role | Responsibilities |
|------|-----------------|
| 🎨 Frontend | Vue.js 기반 UI/UX 구현 |
| ⚙️ Backend | Spring Boot API 서버 개발 |
| 🤖 AI | Flask 기반 음성 학습 모델 |
| ⛓️ Blockchain | Solidity 스마트 컨트랙트 |

## 🔒 Security

- Presigned URL을 통한 안전한 S3 파일 업로드
- 클라이언트의 직접 S3 접근 차단
- 지갑 서명 기반 인증
- NFT 소유권 검증 기반 API 접근 제어

## 📈 Development Progress

**정기 미팅**
- 월 1회 대면 회의
- 필요시 온라인 즉석 회의

**프로젝트 예산**
- 인당 10만원 개인 분배
- 개발 운영비 별도 집행

## 🤝 Contributer
<th></th>
<td></td>

## 📞 Contact

프로젝트에 대한 문의사항이 있으시면 이슈를 등록해주세요.

---

<div align="center">
  <sub>Built with ❤️ by Voice NFT Team</sub>
</div>
