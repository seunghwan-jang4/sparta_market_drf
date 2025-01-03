# spartamarket_DRF

## 1. 프로젝트 개요
`spartamarket_DRF`는 중고 거래를 위한 웹 애플리케이션으로, Django와 Django REST Framework(DRF)를 활용하여 사용자에게 중고 물품을 등록하고 조회할 수 있는 기능을 제공합니다. 본 프로젝트는 최소한의 기능(MVP)을 구현하여, 사용자가 물품을 등록하고 자신의 프로필을 관리할 수 있는 시스템을 구축하는 것을 목표로 합니다. 

<details>
<summary>주요 기능</summary>

## 2. 주요 기능
- **회원가입**: 사용자가 기본 정보(이메일, 비밀번호, 사용자명 등)를 입력하여 계정을 생성합니다.
- **로그인**: 사용자가 등록된 계정으로 로그인하고 인증 토큰을 발급받습니다.
- **프로필 조회**: 로그인한 사용자가 자신의 프로필 정보를 조회할 수 있습니다.
- **상품 등록**: 사용자가 중고 물품을 등록하고 이미지 및 설명을 첨부할 수 있습니다.
- **상품 목록 조회**: 모든 사용자에게 등록된 중고 물품 목록을 페이지네이션 방식으로 제공합니다.
- **상품 수정**: 등록한 사용자만 자신의 상품을 수정할 수 있습니다.
- **상품 삭제**: 등록한 사용자만 자신의 상품을 삭제할 수 있습니다.
</details>


<details>
<summary>사용된 기술</summary>

## 3. 사용된 기술
- **Django**: 웹 애플리케이션의 기본 프레임워크로 사용됩니다.
- **Django REST Framework (DRF)**: RESTful API를 쉽게 구축할 수 있도록 도와주는 Django의 확장 프레임워크입니다.
- **SQLite**: 데이터베이스로 사용됩니다. 기본적으로 SQLite를 사용하지만, 필요에 따라 다른 데이터베이스로 변경 가능합니다.
- **JWT (JSON Web Token)**: 로그인 시 사용자 인증을 위한 토큰 기반 인증 방식을 사용합니다.
</details>

<details>
<summary>트러블 슈팅</summary>

## 4. 트러블 슈팅

`product_detail.html 수정사항 미적용.`

 	수정 및 삭제 버튼 기능을 추가했지만, 페이지에서 보이지 않는 이슈 발생.

**해결 과정**

a. ulrs.py의 문제가 없음을 확인한 후, products 폴더의 view.py 내용을 명시적으로 수정.

b. product_detail.html 또한 명시적으로 수정. 

c. F12 개발자 도구를 통해, 수정 및 삭제 버튼이 존재하는지 확인 실패.

d. 작성한 글에 대한 권한 확인을 위해, 로그인 확인 및 업로드한 계정으로 수정 및 삭제 시도.

e. 작성중인 같은 파일이 두 개가 있었고, 수정된 파일은 다른 경로에 있었음.

	경로를 일치시켜서 해결 완료.
</details>

<details>
<summary>프로젝트 구조</summary>
  
## 5. 프로젝트 구조
- **accounts**: 사용자 계정 관련 기능을 담당합니다. 회원가입, 로그인, 프로필 조회 등을 포함합니다.
- **products**: 중고 물품 관련 기능을 담당합니다. 상품 등록, 수정, 삭제, 목록 조회 기능을 제공합니다.
</details>

<details>
<summary>설치 및 실행 방법</summary>

## 6. 설치 및 실행 방법
프로젝트는 가상 환경에서 실행되며, 필요한 의존성은 `requirements.txt`에 정의되어 있습니다. 로컬 서버에서 실행할 수 있습니다.
</details>

<details>
<summary>향후 확장 가능성</summary>

## 7. 향후 확장 가능성
- **검색 기능**: 사용자가 중고 물품을 검색할 수 있는 기능 추가.
- **카테고리 분류**: 물품을 카테고리별로 분류하여 필터링 기능 추가.
- **리뷰 시스템**: 거래가 이루어진 후 사용자 간의 리뷰를 남길 수 있는 기능 추가.
- **채팅 시스템**: 사용자 간의 실시간 채팅 기능 추가.
</details>


<details>
<summary>ERD</summary>

## 8. ERD

![image](https://github.com/user-attachments/assets/dd0a534b-4373-4c8e-95f3-2844807b6cf3)
</details>
