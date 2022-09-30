
# 애플리케이션 전체 구조

# 사용 스킬
- react
- firebase

# 학습 내용
## 기본
1. react app 생성
    - node 설치 확인 : ```node -v```
    - react app 생성 : ```npx create-react-app ./```
    - 개발 단계 : ```npm run start```
    - 테스트 단계 : ```npm run test```
    - 배포 단계 : ```npm run build```
        - 
2. Create React App 구조
```
	src
	|-- assets
		|-- images
	|-- commons
		|-- components : 여러 페이지에서 쓰일 수 있는 것들(Modals, Tooptips...)
		|-- types : typescript를 위해 type 지정
	|-- components : Page 집합
	|-- redux : Redux를 위한 폴더들
		|-- actions 
		|-- reducers
	|-- App.js : routing 관련 일 처리(react-router-dom)
```

폴더 구조에 정답은 없음			

3. React Router Dom



4. Redux 기본구조
5. REST vs WebSockets
6. Firebase 개념 및 사용법
    - 이메일로 유저 생성 시 문제점
    - Firebase에서 생성한 유저 데이터베이스에 저장
7. React Bootstrap
8. v9

## 요구사항
1. 인증 처리
	- 회원 가입 UI
	- 회원 가입 유효성 체크 (react-hook-form)
	- 현재 password 값 갖기 (useRef)
	- 로그인 UI
	- 인증 후 페이지 이동 (useHistory)
	- (목적) 로그인 유저 정보 저장 (Redux store)
---
2. 공개방 채팅
	- 채팅 페이지 UI
	- 채팅룸 리스트 UI
	- 채팅룸 생성
	- 로그 아웃(Redux Store)
	- 프로필 이미지 수정(Firebase storage 이미지 업로드, Redux Store)
	- Firebase에서 데이터 실시간으로 받기
	- 현재 채팅룸 설정
	- event listener 제거
	- 메시지 헤더 UI
	- 메시지 바디, 메시지 폼 UI
	- 메시지 저장
	- 메시지 보여주기
	- 메시지 컴포넌트 만들기
	- 이미지 파일 업로드
	- 파일 업로드 Progress Bar 만들기
	- 업로드한 파일 메시지를 상대방이 볼 수 있게 해주기
	- 검색으로 메시지 찾기(reduce, regex)
	- 방 생성자, 방 설명
	- 각 사람당 글 쓴 데이터 가져오기
	- UserPosts 데이터를 count가 높은 순서부터 보여주기
---
3. DM 채팅
	- Side Panel DM UI
	- User 목록 가져오기
	- DM방 ID 생성
	- DM 방 클릭 시 해줘야할 것들
	- Private, Public 채팅방 구분해주기
---
4. 알림 & 즐겨찾기 방
	- 알림 UI
	- 알림 정보 만들기
	- 알림 count 클릭해서 없애주기 (messageRef)
	- Favorite 버튼 UI
	- Favorite 정보 데이터베이스에 넣기
	- 페이지 새로고침 시에도 좋아요 표시 남아있게 해주기
	- Favorite 채팅방 클릭 시 해당 방으로 이동
	- Favorite 을 위한 listener 제거
---
5. Typing...
	- Typing UI
	- 타이핑 시작 시 타이핑 정보 데이터베이스에 저장
	- listener 이용하여서 타이핑 정보를 가져오기
	- Typing listener 제거
---
6. Auto Scroll & Skeleton
	- 메시지 보낼 때 자동으로 스크롤 내려가게 하기
	- 메시지 로딩 중 스켈레톤 처리
	- 엔터키로 메시지 보내기
---
7. 데이터베이스, 스토리지 규칙 & 배포
	- Firebase 스토리지 규칙
	- Firebase 데이터베이스 규칙
	- 애플리케이션 배포
---
8. Firebase v9으로 소스코드 수정
	- firebase initialize 소스코드 변경
	- 로그인 회원가입 변경
	- database ref, storage ref
	- listener 등록 (onChildAdded, onValue ...)
	- 채팅방 생성, 채팅 보내기
	- 이미지 업로드
	- 채팅방 즐겨찾기
	- DM