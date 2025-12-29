# [프로젝트 이름]
 Project "STANCE" (스탠스)
 쇼핑몰이름 PACEY
> [쇼핑몰의 컨셉 한 줄 소개]
트렌드 리더를 위한 운동화 전문 쇼핑몰
## 1. 프로젝트 소개
* **설명:** 기획부터 디자인, 개발까지 직접 참여하였으며, **Mock Data(JSON)**를 활용해 실제 커머스 로직을 구현한 운동화 쇼핑몰 프로젝트입니다.
* **진행 기간:** 2025.12.21 ~ 2025.12.29 (6일)
* **개발 인원:** FrontEnd 5인 (Team Project)
* **배포 링크:** [\](https://github.com/elijahthinking/stance-woong)]

## 2. 사용 기술 스택 (Tech Stack)
* **Language:** JavaScript (ES6+)
* **Framework:** React.js
* **Styling:** SCSS
* **Data Handling:** Custom Mock Data (JSON)
* **Design & Tool:** **Figma**, Git, GitHub ,Illustrator, Photoshop

## 3. 기획 및 디자인 (Planning & Design)
* **Tool:** Figma
* **Concept:** 사용자 직관성을 고려한 UI/UX 설계 및 와이어프레임 제작

## 4. 디렉토리 구조
```text
src
├── assets                                 # 이미지, 폰트 및 JSON 데이터
│
├── data                                   # 화면에 쓰이는 고정 데이터 관리
│
├── images                                 # 이미지 파일 보관
│
├── components                             # 공통으로 쓰이는 컴포넌트, 스타일, 데이터 관리 폴더
│    │
│    ├── common                            # 주요 컴포넌트
│    │      ├── Gnb.js                     # 사이트 상단 글로벌 내비게이션 메뉴로, 주요 카테고리 페이지로 이동하는 링크 제공
│    │      ├── Gnb.scss                   # Gnb 스타일 파일
│    ├── detail                            # 상품 상세 페이지 전용 컴포넌트 폴더
│    │      ├── DetailContent.js           # 상품 id 기반으로 상세 이미지를 렌더링하는 상품 정보 영역
│    │      ├── DetailContent.scss         # DetailContent 스타일 파일
│    │      │
│    │      ├── DetailKeyword.js           # 트렌드 키워드를 이미지 그리드로 제공하는 상세 페이지
│    │      ├── DetailKeyword.scss         # DetailKeyword 스타일 파일
│    │      │
│    │      ├── DetailPick.js              # 상세 페이지에서 MD 추천 상품 4개를 보여주는 섹션
│    │      ├── DetailPick.scss            # DetailPick 스타일 파일
│    │      │
│    │      ├── DetailTop.js               # 상품 상세 페이지 상단, 이미지 선택과 옵션 선택 후 장바구니 담기 기능을 제공하는 영역
│    │      ├── DetailPick.scss            # DetailTop 스타일 파일
│    │
│    ├── main                              # 메인 페이지(홈) 전용 컴포넌트 폴더
│    │      ├── BannerSection.js      ┐
│    │      ├── BannerSection.scss    │    # 메인 페이지 상단 및 이벤트 배너 영역으로, 자동 및 수동 슬라이드, 진행바, 화살표, 텍스트 오버레이 기능 제공
│    │      ├── BannerSection2.js     │    # BannerSection 스타일 파일
│    │      ├── BannerSection2.scss   ┘
│    │      │
│    │      ├── BottomBlog.js              # 무한 스크롤 방식의 트렌드 키워드 해시태그 섹션
│    │      ├── BottomBlog.scss            # BottomBlog 스타일 파일
│    │      │
│    │      ├── CategorySection.js         # 스크롤 애니메이션이 적용된 러닝 뉴스 카드 섹션
│    │      ├── CategorySection.scss       # CategorySection 스타일 파일
│    │      │
│    │      ├── Footer.js                  # 푸터 영역
│    │      ├── Footer.scss                # Footer 스타일 파일
│    │      │
│    │      ├── Header.js                  # 헤더 및 네비게이션 영역
│    │      ├── Header.scss                # Header 스타일 파일
│    │      │
│    │      ├── Midblog.js                 # 이벤트 및 프로모션 배너를 노출하는 메인 중단 영역
│    │      ├── Midblog.scss               # Midblog 스타일 파일
│    │      │
│    │      ├── ProductSection.js      ┐
│    │      ├── ProductSection.scss    │   # 슬라이드 기능·스크롤 애니메이션이 적용된 상품 섹션
│    │      ├── ProductSection2.js     │   # ProductSection 스타일 파일
│    │      ├── ProductSection2.scss   ┘
│    │      │
│    │      ├── TopBlog.js                 # 메인 페이지 상단 브랜드 인트로 및 안내 영역
│    │      ├── TopBlog.scss               # TopBlog 스타일 파일
│    │
├── pages         # 라우팅 페이지 (Cart, Detail, Main...)
│   ├── CartPage.js                        # 장바구니 페이지로, 로컬스토리지에서 담긴 상품 데이터를 불러와서 선택/삭제, 수량 조절, 합계 계산, 결제금액 확인, 이미지 미리보기 기능을 제공하는 컴포넌트
│   ├── CartPage.scss                      # CartPage 스타일 파일
│   │
│   ├── DetailPage.js                      # 상품 상세 페이지로, 상단 이미지/옵션, 상품 정보, MD 추천, 키워드 섹션을 순차적으로 렌더링하는 컴포넌트
│   │
│   ├── MainPage.js                        # 메인 페이지로, 배너, 카테고리, 뉴스, 베스트셀러, 이벤트, 키워드 등 주요 섹션을 순서대로 렌더링하는 컴포넌트
│   │
└── layout                                 # 공통 레이아웃 구조 (Header, Footer )
    ├── Layout.js                          # 공통 레이아웃 구조

## 5. 담당 역할

[기획, 문서]
* 실제 판매되는 벤치 및 마케팅 요소 고려 기획 수립
* 문서 수집 및 스케줄 관리

[개발:  기능]
* 푸터, 상세페이지



## 6. 주요 기능
메인 기능 메인페이지 이미지 캐러셀
개별 제품 사진 hover시 이미지 변경
페이지 최상단으로 이동하는 스크롤 버튼
제품 CART 버튼 클릭 시 장바구니 담기 기능

## 7. 트러블 슈팅
문제 1. 반응형 변환 오류
상황: 푸터 모바일형으로 변환시 UI 오류
해결: 팀원들의 코딩 능력 협조로 인해 문제 해결
과정: 데스크탑 화면에서 보여지는 UI 구조는 작성하였으나 모바일 화면에서 새롭게 나타나는 선을 어떻게 할지 몰라 팀원에게 도움을 구했고 해당 문제를 사사 받고 해결 

## 8. 실행 화면
https://elijahthinking.github.io/stance-woong/#/detail/12