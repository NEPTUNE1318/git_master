# git 사용 방법

## 초기 git setting
1. $ git init
2. $ git config --global user.email "e-mail"
3. $ git config --global user.name "user name"
4. $ git add .
5. $ git commit -m "수정된 내용"
6. $ git branch -M master
7. $ git remote add origin 링크
(만약 7번이 안될 경우 $ git remote remove origin)
8. $ git push -u origin master

## 수정
1. $ git add . (or 원하는 파일 이름, 확장자 포함)
2. $ git commit -m "수정된 내용"
3. $ git push -u origin master (한번 실행한 경우 git push만 해도 적용됨)

## git file 다운 방법
* $ git clone [git link]                      -> 로컬 저장소와 일치 시킴
* $ git pull [원격 저장소 이름] [브랜치 이름] -> 이미 수정한 파일이 있을 경우 내용을 가져와 merge
안되는 경우 git pull [원격 저장소 이름] [브랜치 이름] --allow-unrelated-histories
* $ git fetch [원격 저장소 이름]              -> pull과 동일하지만 merge x

## 되돌리기
* $ git checkout 해시코드 6자리      // 해당 해시코드의 버전 불러오기
* $ git checkout 브런치 이름         // 최신에 커밋된 버전을 불어오기
* $ git revert 해시코드 6자리        // 해당 해시코드의 버전 불러오고 커밋까지 자동 실행
* $ git revert --hard 해시코드 6자리 // 해당 해시코드의 이후 모두 버전 삭제

## 유용한 명령어
* $ git status                       // 지금 git의 상태
* $ git log                          // 변경괸 것을 로그로 나타내냄
* $ git diff                         // 두 버전 사이의 차이점 확인


## 브랜치 관련 명령어
* git checkout [브랜치 이름] ->      브랜치 전환
* git merge [브랜치 이름]    ->      브랜치 병합