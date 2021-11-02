# git-study repository
git study, training

## git source workflow
<img src="https://user-images.githubusercontent.com/42735302/139765056-86a91b4e-60da-494e-804a-ef2517819812.png">

1. 지역 저장소 생성하기
- git 지역 저장소는 init 명령으로 설정
- 'Initalized empty Git repository in ...' message 확인
- .git 숨김폴더 생성 확인 (git 지역 저장소에서 관리하는 file, branch, 설정 정보등)
```
$ git init
Reinitialized existing Git repository in C:/Users/USER/IdeaProjects/study01/.git/

// git init 취소
$ rm -rf .git
```

2. 사용자등록
- git 지역 저장소의 사용자 정보 등록
- 여러 개발자가 같이 작업할 수 있기 때문에 현재 작업하는 개발자가 누구인지 등록하는 과정
- 사용자 이름, 이메일 주소는 Github 계정의 Username, Email과 동일해야함
```
$ git config user.name "사용자 이름"
$ git config user.email "이메일 주소"

// 모든 프로젝트에 사용될 사용자 정보 등록 --global
// 하나의 로컬PC에서 여러 계정을 사용할 일이 없다면 --global 옵션 사용 용이함
$ git config --global user.name "사용자 이름"
$ git config --global user.email "이메일 주소"
```

3. git 설정 파일 확인
- 설정 정보들은 .git 폴더 안의 config 파일에 등록됨
- core / user 섹션으로 구분되며,  
  - core : git이 파일을 감지, 캐싱, git의 동작을 제어하는 설정
  - user : 사용자 정보 <br>
```
$ cat ./git/config
[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	symlinks = false
	ignorecase = true
[user]
	name = minizm
	email = sktkdals2244@naver.com
[remote "origin"]
	url = https://github.com/minizm/java-pre-course.git
	fetch = +refs/heads/*:refs/remotes/origin/*
```
 
 4. git 원격 저장소 설정
- 생성한 원격 저장소 페이지에서 원격 저장소 주소 Copy
- git remote add origin 명령어로 원격 저장소 주소를 git 지역 저장소에 등록
```
$ git remote add origin {복사한 원격 저장소 주소}
```

