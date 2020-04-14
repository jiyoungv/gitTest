# Git
Git은 버전관리시스템 입니다.

## 0. 최초 설정
```
git config --global user.email jiyoungvvvvv@gmail.com

git config --global user.name jiyoung
```

## 1. .git 폴더 생성
```
git init
```

## 2. add와 commit
```
git add index.html // 지정 파일 Tracked
git add . //모든 파일 Tracked
git rm index.html // 지정 파일 Untracked

git commmit -m "Change index.html"

git commit -am "Change index.html" // add + commit 동시에
```
- Tracked File만 commit이 가능하다.

## 기타 명령어
```
git status // 현재 상태 확인
git log // 커밋 내역 확인
```

# GitHub과 연동
GitHub은 파일과 버전이력을 저장해놓는 저장소입니다.

## 1. 원격 저장소 연결
```
git remote add origin https://github.com/jiyoungv/gitTest // origin이라는 이름으로 원격 저장소 주소 등록
git remote remove origin // origint이라는 이름의 원격 저장소 삭제
git remote // 원격 저장소 확인
```

## 2. 원격 저장소 commit 저장
```
git push origin master // master branch의 commit 저장
```
- Github 새로고침하면 push 되어 있다.

## 3. 원격 저장소 코드를 클라이언트로 내려받기
```
git pull origin master // origin의 내용이 master로 복사
git clone https://github.com/jiyoungv/gitTest // 클라이언트에 아무것도 없을때. 저장소 내용 다운로드 & 자동 git init
```

# Git Branch

## 1. branch
```
git branch // 현재 브랜치 확인
git branch feature // feature라는 브랜치 생성
git checkout feature // feature라는 브랜치로 HEAD 이동
```
- 앞에 * 표시와 초록색으로 되어있는 곳이 현재 HEAD가 있는 브랜치.
```
git merge feature // feature라는 브랜치를 합치기
```
- **현재 HEAD가 바탕이 되는 master에 있는지 확인 후, merge를 해야한다.**
```
git branch -d feature // feature라는 브랜치 delete
```

