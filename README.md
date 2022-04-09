# Mac에 Git 설치 및 연동
## homebrew 설치 후 Git 설치(brew git install)
## git 코드 입력
git config --global user.name " "
git config --global user.email " "
## 레파지토리가 있을 경우 로컬로 가져오기
git clone https://github.com/userid/name.git

# Github에 대해서
## Repository(저장소): 파일이나 디렉토리를 저장하는 장소
Local Repository(로컬 저장소): 현재 사용하고 있는 디바이스에 저장되는 것
Remote Repository(원격 저장소): 원격 서버에 저장되고 관리되는 저장소
## 저장소에 업로드하는 방법
commit(커밋): 파일을 변경하거나 변경내용을 저장소에 저장하는 것
push(푸쉬): 파일을 변경하거나 변경내용을 원격 저장소에 업로드하는 것
## 원격 저장소에서 로컬 저장소로 가져오는 방법
pull(풀): 원격 저장소에 있는 변경사항을 로컬 저장소로 가져와 자동으로 병합한다. 개인이 쓰는 경우에 적합
fetch(페치): 원격 저장소에 있는 변경사항을 로컬 저장소로 가져오기만 함. 병합은 따로. 다른 사람이 수정한 부분을 확인하고 병합할 수 있다.
clone(클론): 원격 저장소의 내용을 새로운 폴더에 그대로 복사
## 저장소 생성
현재 디렉토리를 기준으로 저장소를 생성: git init
## 로컬 저장소 삭제
숨겨진 파일인 '.git' 삭제로 연동해제: find ./ -name ".git" | xargs rm -Rf
로컬 저장소 삭제: rm -rf "로컬 저장소 명"
## 파일 상태 확인
### git status 명령어로 파일 상태 확인 가능
### git add filename 명령어로 git에게 추적해달라는 명령이 가능
크게 Untracked, Tracked 상태로 나뉘는데 Untracked는 git이 추적하지 않는 상태(기본), Tracked는 git이 추적하는 상태를 말한다.
Tracked는 Staged area에 진입 후 크게 3가지 상태로 나뉜다.
Staged: add 후 staged area에 있는 파일의 상태. git status를 하면 "Changes to be committed"에 들어있는 파일들이다.
Unmodified: Staging area에 있는 파일들을 커밋하면 바뀌는 상태
Modified: Unmodified에 있는 파일을 수정하면 바뀌는 상태
*commit을 하기 위해선 add로 Staged 상태가 돼야한다.
*add는 선택적 커밋이 가능하게 한다.
## 버전업
git commit 명령어 입력 -> vim이 실행 되면 입력모드로 전환해서 버전업에 대한 메세지 입력 후 저장 혹은 git commit -m commit message로 커밋 가능
## 로그 확인
git log 명령어로 누가 언제 커밋을 했는지 조회 가능
git log -p를 사용하면 커밋과 커밋사이 소스의 차이를 알 수 있다.


# vi 명령어
## 명령모드, 입력모드, 마지막형모드로 구성(첫 진입은 명령모드)
i, a를 누르면 입력모드로 진입, ESC를 누르면 명령모드 진입, ':' 입력시 마지막형 모드로 진입
## 명령모드 동작
x: 커서가 위치한 곳의 글자 1개 삭제
dd: 커서가 위치한 곳의 1줄 삭제
p: 커서 아랫줄에 버퍼에 들어간 내용을 붙여넣기
G: 파일의 끝을 이동(대문자로 사용)
*동작이 많으므로 필요한건 찾아보자
## 마지막형 모드 동작
w: 현재 파일명으로 파일 저장
q: vi 종료(저장X)
wq: 저장 후 종료
*명령어 끝에 !를 붙이면 강제수행

# IntelliJ Run 버튼 비활성화가 돼있을때
1. 오른쪽 상단 Add Configuration 클릭
2. '+' 클릭 후 Application를 선택하고 OK로 생성
3. Main Class에 메인이 될 클래스 입력 후 추가

# IntelliJ 에러
Class JavaLaunchHelper is implemented in both ... 
맥 사용자가 IDE로 App 실행시 일어나는 오래된 자바 버그로 무시해도 안전한 메세지
Preferences > Edit > General > Console > Fold console lines that contain에 "Class JavaLaunchHelper is implemented in both" 추가
