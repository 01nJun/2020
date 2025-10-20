# 공연웹사이트(커뮤니티)
- 이 플랫폼은 React를 기반으로하여 공연의 예매와 순위를 볼 수 있고 다른 유저들과의 소통이 가능한 잡담공간까지 지원하는 공연 웹사이트입니다.


## 프로젝트 개요
- 이 프로젝트는 공연의 정보를 효율적으로 검색하고 다른 유저들과의 소통을 활발히 할 수 있는 웹 애플리케이션입니다. 사용자들이 게시물을 올려 서로 잡담을 하거나 공연에 대해 궁금한 점을 물어보고 답해주고 요즘 어떤 공연이 HOT한지도 알 수 있도록 지원합니다.



## 구현한 핵심 기능

- CRUD:생성/조회/수정/삭제 전부 구현
- SPA(router)
- 무한 스크롤: 데이터의 효율화 처리
- 코드스플리팅: lazy+ Suspense 처리하기
- 외부데이터 연동: 외부데이터 이름
- 반응형웹(PC, 태블릿 or 모바일)
  
 ## 개발기간
- 25.10.14(화) ~ 25.10.20(수)

### 팀원 소개 및 역할 분담
- **박태오 (팀장)** | **@teomichaelpark-glitch**
- **오인준** | **@01nJun**
- **전유진** | **@ujyj0414**




### 개발 환경
- 언어

<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/> <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white"/> <img src="https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white"/>

- 개발 도구 

<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black"/> <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white"/>

- IDE

<img src="https://img.shields.io/badge/Visual_Studio_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white"/>

- OS

<img src="https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white"/>

- Sever : AWS

## 실행하기
### 환경 버전
- #### JavaScript
- #### Node.js 18+ (React 19.1.1)



## 프로젝트 구조
```
kopis-crud-system/
└── src/
    ├── api/
    ├── components/         <-- 🆕 새로운 폴더!
    │   ├── common/         <-- 🆕 공통으로 사용하는 컴포넌트
    │   │   ├── Card.js
    │   │   └── TabMenu.js
    │   ├── community/      <-- 🆕 '잡담' 관련 컴포넌트
    │   │   ├── CommunityFilter.js
    │   │   └── PopularPostList.js
    │   └── performance/    <-- 🆕 '공연' 관련 컴포넌트
    │       ├── PerformanceFilter.js
    │       └── PerformanceList.js
    ├── data/
    ├── hooks/              <-- 여기는 그대로!
    └── pages/
        ...
```

### ERD


## 주요 페이지
- 메인 페이지: 사용자가 공연의 예매창으로 갈 수 있고 찜을 할 수 있음

- 잡담 페이지: 사용자들이 글을 올려서 사용자들끼리 대화를 주고 받을 수 있는 공간

- MY PAGE : 내가 찜하기를 누른 공연들의 체크리스트를 적을 수 있다
### 주요 기능
#### 커뮤니티
- 찜하기 / 체크리스트: 찜하기를 누르면 체크리스트로 이동 체크리스트 등록/수정/삭제
- 투표 : 올라온 투표글에 좋아요와 싫어요 둘 중 하나를 누를 수 있음
