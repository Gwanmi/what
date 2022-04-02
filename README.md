# Mac에 Git 설치 및 연동
## homebrew 설치 후 Git 설치(brew git install)
## git 코드 입력
### git config --global user.name " "
### git config --global user.email " "
## 레파지토리가 있을 경우 로컬로 가져오기
### git clone https://github.com/userid/name.git

# Github에 대해서
## Repository(저장소): 파일이나 디렉토리를 저장하는 장소
### Local Repository(로컬 저장소): 현재 사용하고 있는 디바이스에 저장되는 것
### Remote Repository(원격 저장소): 원격 서버에 저장되고 관리되는 저장소
## commit(커밋): 파일을 변경하거나 변경내용을 저장소에 저장하는 것
## push(푸쉬): 파일을 변경하거나 변경내용을 원격 저장소에 업로드하는 것

# vi 명령어
## 명령모드, 입력모드, 마지막형모드로 구성(첫 진입은 명령모드)
## w: 현재 파일명으로 파일 저장
## q: vi 종료(저장X)
## wq: 저장 후 종료
## *명령어 끝에 !를 붙이면 강제수행

# IntelliJ Run 버튼 비활성화가 돼있을때
## 1. 오른쪽 상단 Add Configuration 클릭
## 2. '+' 클릭 후 Application를 선택하고 OK로 생성
## 3. Main Class에 메인이 될 클래스 입력 후 추가

# IntelliJ 에러
## Class JavaLaunchHelper is implemented in both ... 
### 맥 사용자가 IDE로 App 실행시 일어나는 오래된 자바 버그로 무시해도 안전한 메세지
### Preferences > Edit > General > Console > Fold console lines that contain에 "Class JavaLaunchHelper is implemented in both" 추가
