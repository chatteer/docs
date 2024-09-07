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

