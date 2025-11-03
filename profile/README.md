# 🎙️ AudiOn

> AI 음성 모델을 NFT로 발행하고, API로 활용할 수 있는 Web3 플랫폼

## 👋 About Us

SOUND A.I.는 AI 음성 기술과 블록체인을 결합하여, 개인의 목소리를 디지털 자산으로 만드는 혁신적인 서비스를 개발하고 있습니다. 사용자는 자신의 목소리를 학습시켜 AI 모델로 만들고, 이를 NFT로 발행하여 소유권을 증명합니다.

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
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)

### Backend & AI
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS_S3-569A31?style=for-the-badge&logo=amazon-s3&logoColor=white)

### Blockchain
![Solidity](https://img.shields.io/badge/Solidity-363636?style=for-the-badge&logo=solidity&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)

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

📱 Application Screenshots
<table>
  <tr>
    <td align="center" width="200px" style="padding: 10px; vertical-align: top;">
      <img src="https://github.com/2025-Imagine-Company/APP/blob/develop/assets/screens/home(updated).png?raw=true" style="width:180px; height:330px; object-fit: contain; border-radius:10px;" alt="홈 화면"/>
      <br /><br />
      <b>홈 화면</b><br />
      <sub>음성 녹음 시작</sub>
    </td>
    <td align="center" width="200px" style="padding: 10px; vertical-align: top;">
      <img src="https://github.com/2025-Imagine-Company/APP/blob/develop/assets/screens/login_walletselect.png?raw=true" style="width:180px; height:330px; object-fit: contain; border-radius:10px;" alt="지갑 연결"/>
      <br /><br />
      <b>지갑 연결</b><br />
      <sub>MetaMask 로그인</sub>
    </td>
    <td align="center" width="200px" style="padding: 10px; vertical-align: top;">
      <img src="https://github.com/2025-Imagine-Company/APP/blob/develop/assets/screens/mypage(updated).png?raw=true" style="width:180px; height:330px; object-fit: contain; border-radius:10px;" alt="마이페이지"/>
      <br /><br />
      <b>마이페이지</b><br />
      <sub>음성 모델 관리</sub>
    </td>
    <td align="center" width="200px" style="padding: 10px; vertical-align: top;">
      <img src="https://github.com/2025-Imagine-Company/APP/blob/develop/assets/screens/record_upload(updated).png?raw=true" style="width:180px; height:330px; object-fit: contain; border-radius:10px;" alt="녹음 페이지"/>
      <br /><br />
      <b>녹음 페이지</b><br />
      <sub>음성 학습 진행</sub>
    </td>
    <td align="center" width="200px" style="padding: 10px; vertical-align: top;">
      <img src="https://github.com/2025-Imagine-Company/APP/blob/develop/assets/screens/minting_transaction.png?raw=true" style="width:180px; height:330px; object-fit: contain; border-radius:10px;" alt="NFT 민팅"/>
      <br /><br />
      <b>NFT 민팅</b><br />
      <sub>블록체인 발행</sub>
    </td>
  </tr>
</table>

## 👥 Team
<table>
  <tr>
    <td align="center" width="200px">
      <a href="https://github.com/MinSang22Kim">
        <img src="https://github.com/MinSang22Kim.png" width="100px;" alt=""/>
      </a>
    </td>
    <td align="center" width="200px">
      <a href="https://github.com/yoonbell">
        <img src="https://github.com/yoonbell.png" width="100px;" alt=""/>
      </a>
    </td>
    <td align="center" width="200px">
      <a href="https://github.com/chaery0ung">
        <img src="https://github.com/chaery0ung.png" width="100px;" alt=""/>
      </a>
    </td>
    <td align="center" width="200px">
      <a href="https://github.com/v2n03">
        <img src="https://github.com/v2n03.png" width="100px;" alt=""/>
      </a>
    </td>
    <td align="center" width="200px">
      <a href="https://github.com/znan2">
        <img src="https://github.com/znan2.png" width="100px;" alt=""/>
      </a>
    </td>
  </tr>
  <tr>
    <td align="center">
      <b>김민상</b>
    </td>
    <td align="center">
      <b>이윤종</b>
    </td>
    <td align="center">
      <b>홍채령</b>
    </td>
    <td align="center">
      <b>노형준</b>
    </td>
    <td align="center">
      <b>박진환</b>
    </td>
  </tr>
  <tr>
    <td align="center">
      ⚡ Solution Architect
    </td>
    <td align="center">
      📱 Frontend
    </td>
    <td align="center">
      📱 Frontend
    </td>
    <td align="center">
      ⚙️ Backend & AI
    </td>
    <td align="center">
      ⛓️ Blockchain
    </td>
  </tr>
</table>


<div align="center">
  <sub>Built with ❤️ by SOUND A.I.</sub>
</div>
