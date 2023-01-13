# git 배운것
## git clone 
- git clone 'url' 하면 하위 폴더를 repository의 이름을 가져오면서 복사.
- git clone 'url' . 하면 작업하는 폴더를 복사.
- git pull origin master 로 다운로드, git push origin master 로 업로드
  - git pull -u origin master, git pull -u
- 한 번에 하나씩 pull, push 해야지 충돌 안나고 잘 동기화됨. 동시에 작업하면 충돌로 인한 오류 발생

## git commit --amend
- `git commit --amend`로 commit 된거 push 전에 고칠수 있음.
  - vim 에디터 나옴. `insert` 눌러서 모드 바꾸고 commit 메시지 수정가능.
  - esc 누른다음 :wq 타이핑 하면 완료됨.
  - git log 할떄는 q 누르면 나가짐

## 특정 파일 무시하는법 (screte)
- `touch .gitignore` 명령어로 `git ignore` 파일 생성
  - `git ignore` 편집해서 무시할 파일명 입력 (ex: 메모장 열고 secret.txt)
  - 입력된 파일은 status에 안뜨고 `add`, `commit`안됨
  - `.gitignore.io` 에서 무시할만한 파일들 참조 가능함.
    - #은 주석, /은 디렉토리(하위 파일들 전부 무시)
- git init 하자마자 만드는게 권장됨.
   - 한번 관리된 파일은 무시하지 못하기 떄문임. add 한 순간 안됨