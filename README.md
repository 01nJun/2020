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
 **박태오 (팀장)** | **@teomichaelpark-glitch**
- 프로젝트 총괄 및 아키텍처 설계: 초기 기술 스택 선정, Custom Hook 기반의 상태 관리 구조 설계 및 팀원 간의 역할 조율을 담당했습니다.
- 공연 목록 다중 필터링: Performances.js 내에서 다중 조건(장르, 지역, 공연 상태)에 따라 실시간으로 API를 재호출하고 목록을 갱신하는 핵심 로직을 구현했습니다.
- 커뮤니티 '인기글' 기능: 일간/주간/월간 탭 UI를 개발하고, 각 탭에 IntersectionObserver를 적용하여 콘텐츠를 무한 스크롤로 불러오는 기능을 구현했습니다.
- 반응형 웹 디자인: 미디어 쿼리를 활용하여 PC, 태블릿, 모바일 등 다양한 디바이스 환경에 대응하는 UI를 구현했습니다.

 **오인준** | **@01nJun**
- 커뮤니티 '투표' 기능 개발: Performances.js 내 커뮤니티 탭 기능 중 '투표' 파트를 전담했습니다.
- '투표' 필터링 로직 구현: dummyPolls.js 데이터와 연동하여 동적 필터링 탭 UI를 구현하고, 선택된 필터(selectedPollsType)를 PollsPage 컴포넌트에 prop으로 전달하여 조건부 렌더링하는 로직을 개발했습니다.

 **전유진** | **@ujyj0414**
- MY PAGE 총괄 및 CRUD 구현: 찜 목록 조회(Favorites.js)부터 상세 페이지(FavoriteDetail.js)까지 이어지는 'MY PAGE'의 전체 사용자 흐름을 담당했습니다.
- 개인화 체크리스트 (CRUD): useChecklist.js 커스텀 훅을 직접 설계하여 체크리스트의 생성(Create), 조회(Read), 수정(Update), 삭제(Delete) 로직을 모두 완성했습니다.
- SPA 라우팅 및 전역 상태 관리: React Router를 사용한 전체 페이지 라우팅 구조를 설계하고, localStorage와 useFavorites 커스텀 훅을 통해 앱 전역의 '찜하기' 상태를 관리하는 로직을 개발했습니다.
- 커뮤니티 '게시판' 기능: selectedCommunityTab 상태에 따라 조건부로 렌더링되는 BoardLibraryPage 컴포넌트의 기본 구조와 UI를 담당했습니다.
전체 CSS 스타일링: 프로젝트의 일관된 디자인 시스템을 적용하고 전체적인 CSS 스타일링을 담당했습니다.

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
<img width="736" height="755" alt="image" src="https://github.com/user-attachments/assets/929ccaf0-2abb-4429-98e4-a4c70d335bd2" />



## 주요 페이지
- 메인 페이지: 사용자가 공연의 예매창으로 갈 수 있고 찜을 할 수 있음

- 잡담 페이지: 사용자들이 글을 올려서 사용자들끼리 대화를 주고 받을 수 있는 공간

- MY PAGE : 내가 찜하기를 누른 공연들의 체크리스트를 적을 수 있다
### 주요 기능
#### 예매하기
- 자신이 원하는 공연의 마우스를 올려 예매하기를 눌러 예매창으로 갈 수 있음
#### 커뮤니티
- 찜하기 / 체크리스트: 찜하기를 누르면 체크리스트로 이동 체크리스트 등록/수정/삭제
- 게시글 : 게시글에 하트를 누를 수 있고 이 게시물을 몇명이 봤는지 알 수 있음
- 투표 : 올라온 투표글에 좋아요와 싫어요 둘 중 하나를 누를 수 있음
