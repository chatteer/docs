# 채팅 시스템 구축
## 요약
- 1:1 채팅, 멀티 채팅이 가능한 시스템을 구축합니다.
## 백그라운드
- 사이드 프로젝트에 목마른 자들을 위해 채팅서비스를 만들기로 했습니다 🥰
## 목표
### 담당자
|구분|담당자|
|---|---|
|PM|@sieunju|
|Server|@isemang|
|Client API|@isemang, @sieunju|
|Mobile(Android)|@sieunju|

## 규칙
- 담당자가 모든것을 결정한다. eg.) API Response가 별로 맘에 안드는데 변경해주면 안돼요?🙅, API Response 가 JSend 규칙이 아닌데 JSend 규칙으로 변경해줄수 있을까요?🙆‍♂️ 왜냐면 그래야 유지보수할때 쉬울거 같아요!
- 결정된 사항에 대해 토달지 않는다. (의견 제시는 가능 eg.채팅 메시지안에 날짜 정보 넣었으면 좋겠어요🙆‍♂️
- 작업에 대해 언제끝나는지 재촉하지 않는다. eg.)채팅 메시지 보내는 기능 언제 끝나요? 🙅

## 기능
|프로토콜|기능|포지션|
|---|---|---|
|HTTP|회원 가입 (Google SNS)|Server, Mobile|
|HTTP|로그인 (Google SNS)|Server, Mobile|
|HTTP|프로필 변경(이름, 이미지)|Server, Mobile|
|TCP|채팅방 개설|Server, Client|
|TCP|사용자 초대|Server, Client|
|HTTP|사용자 정보 조회|Server, Client|
|TCP|채팅 메시지 보내기|Server, Client|
|TCP|채팅 메시지 받기|Server, Client|
|HTTP|채팅 파일 업로드|Server, Client|
|HTTP|이전 대화 목록 조회(페이징)|Server, Client|
|TCP|채팅방 나가기|Server, Client|

## 채팅 시나리오(방을 개설하는 경우)
1. 방을 개설하고 채팅하고 싶은 사용자를 초대합니다.
2. 초대한 사용자의 프로필 정보를 조회하여 채팅창에 표시할 별칭과 이미지를 가져옵니다.
3. 자유롭게 1:1 채팅을 이용합니다.
4. 채팅방 나가면 대화를 나눴던 내용들은 서버에 저장됩니다.

## 채팅 시나리오(개설된 방에 재입장하는 경우)
1. 초대된 사용자의 프로필 정보를 조회하여 채팅창에 표시할 별칭과 이미지를 가져옵니다.
2. 이전에 채팅한 히스토리를 가져옵니다.
3. 자유롭게 1:1 채팅을 이용합니다.
4. 채팅방 나가면 대화를 나눴던 내용들은 서버에 저장됩니다.

## 모바일 화면 컨셉 (1차)
- 이런 느낌으로 모바일을 구성할 예정입니다. 컨셉샷 정도?

|채팅목록|채팅|
|--|--|
|![Group 18](https://github.com/user-attachments/assets/5b7a86f7-afd8-477c-97a7-244d57f79eb1)|![Group 17](https://github.com/user-attachments/assets/1a6b41bb-4b6f-43fd-abc7-af5dfdd4c02f)|
