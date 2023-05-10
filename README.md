# Git 사용법 및 활용 방법

*git 형상 관리 롤
		- 버전 관리(히스토리 관리)
	
*형상 관리 롤 :  CVS
				SVN
				GIT
						
	\r\n(CRLF)
	\n(LF)
	
### 1. git 설치
	- git-scm.com 에서 설치

### 2. 로컬 레포지토리(로컬 저장소)
	- git init : 로컬에 저장할 수 있는 공간 생성

### 3. 계정연결
	- git config --global user.email "이메일"
	- git config --global user.name "계정"
	

## 형상관리
### 1. 스테이지 단계
- git add 파일명/파일경로
- git add . (변경된 모든 파일)
	
### 2. 스냅샷 단계
- git commit -m "작업 내용"
	
- 버전을 기록(시점 기록)
	
### 3. 커밋 로그
- git log
- git log --oneline : 한줄로 짧게 볼 수 있다(commit id)
	
### 4. 버전 관리
- git checkout (commit아이디)
- git checkout - : 바로 직전 시점으로 복귀
	
### 5. 브랜치

####	5-1) 브랜치 관리 - 기본 브랜치(master)
- git branch : 현재 브랜치 목록
- git branch 브랜치명 : 브랜치 생성
		현재 브랜치 기준 위치(소스) -> 생성된 브랜치로 복사
	
####	5-2) 브랜치 이동
- git checkout 브랜치명 : 브랜치 이동
	
####	5-3) 브랜치 삭제
- git branch -D 브랜치명
	
####	5-4) 브랜치명 변경
- git branch -M 브랜치명
	

### 6. 소스 합치기
	git merge 브랜치1
		-> 현재 브랜치 기준으로 브랜치1 소스가 병합된다

### 7. 원격 레포지토리 연결
- git remote add origin 원격저장소 주소 : 추가
           set-url origin 원격저장소 주소 : 변경
    
    로컬 레포지토리 -> 원격레포지토리 연결 : 상태 동기화

    로컬 레포지토리 브랜치 -> 원격 레포지토리 브랜치 상태 동기화
    - git push origin 브랜치명

    참고 ) origin/브랜치명 -> 원격 브랜치명
            브랜치명 -> 로컬 브랜치명

원격 레포지토리 브랜치 상태 -> 로컬 레포지토리 브랜치 상태 동기화
- git pull origin 브랜치명

원격 레포지토리 로컬에 복사
- git clone 원격 레포지토리 주소

### 8. 원격저장소 업로드 방법
	1) git init - 최초 명령 , git 폴더 생성
	2) git config --global user.email "user@example.com" : git 로컬에 이메일 설정
	3) git config --global user.name "user" : (github uri의 github.com/"user")
    4) git remote add origin 원격저장소 주소(github.com/"user")
    5) git add . : 작업한 내용 추가
    6) git commit -m "내용" : 로컬 저장소에 추가
    7) git push origin master : 원격 저장소에 업로드

### 9. GitIgnore
- .gitignore 깃 원격 저장소에 반영 배제

*.확장자 : 확장자 배제
파일명/ : 파일명을 포함한 모든 경로 배제
폴더명/ : 폴더명을 포함한 모든 경로 배제
/경로 -> 메인

경로/ -> 경로가 포함된 모든 디렉토리


### 10. Sourcetree 