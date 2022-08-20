# git command test

```
git init

git clone https://github.com/honeion/git_test.git
```
## git remote
```
git remote

git remote -v(각 연결 url 포함)
```
- 다른 리포지토리에 대한 연결을 만들고, 보고, 삭제할 수 있음
- ./.git/config 파일

## create remote
```
git remote add <name> <url>
```

## delete remote
```
git remote rm <name>
```

## update remote
```
git remote rename <old-name> <new-name>
```
 - 이름 변경

## git branch
```
git branch = git branch --list
```

## create new branch
```
git branch <branch name>
```

## delete branch
```
git branch -d <branch name>
```
 - 병합되지 않은 변경 사항이 있는 경우 분기를 삭제하지 못함
```
git branch -D <branch name>
```
 - 변합되지 않은 변경 사항 있어도 지정된 분기 강제 삭제

## search branch
```
git branch -m <branch>
```
 - 현재 분기 이름 확인
```
git branch -a
```
 - 모든 원격 분기 나열


## git checkout

```
git checkout -b <new branch>
```
 - 브랜치 생성 및 체크아웃

```
git checkout -b <new branch> <existing branch>

ex) git checkout -bnew-branch HEAD git checkout＜existing-branch＞new-branch existing-branchHEAD
```
 - 현재 브랜치 기반으로 추가 매개변수 줄 수 있음


## git merge

```
# Start a new feature
git checkout -b test2
# Edit some files
git add <file>
git commit -m "Start a feature"
# Edit some files
git add <file>
git commit -m "Finish a feature"
# Merge in the new-feature branch
git checkout main
git merge test2
git branch -d test2
```
