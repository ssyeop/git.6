✔Git 배우기
===

Github
---
### Githuub 가입
[Github 홈페이지](https://github.com/)에서 회원 가입
- 새로운 Repository(원격 저장소) 만들기
    - Owener : 사용자이름
    - Repository name : 중복되지 않는 저장소 이름
    - Description : 저장소를 설명하는 요약 한 줄
    - Public / Private : 공개 / 비공개 설정
    - Add a README : 리드미 파일을 자동으로 추가 (체크 비권장) (이후 추가 가능)
    - Add .gitignore : 깃 저장소에 올리면 안 되는 파일의 목록이 담긴 파일 (해당 파일들은 무시) 추가하기 (프로그래밍 언어별 기본값) (이후 추가 가능)
    - Choose a license : 오픈소스에 대한 지적 재산권을 부여하기 위한 파일을 추가 (이후 추가 가능) 
    - 3가지 파일을 선택하지 않으면, Quick setup (CLI 명령어)를 볼 수 있다.

Git
---

안녕하세요~ 깃 반가워요

1. 깃 저장소 **만들기** 명령어
'git init'

2. 깃 추적되지 않은 파일 모두 현재 폴더 기준으로 **스테이징** : ' git add .'

3. **커밋**하기
 'git commit - m
"커밋 메시지"'

4. **원격저장소** 추가하기 : 
'git remote add [깃힙저장소주소]'

- `git remote add' [원격저장소 이름]
[원격저장소 주소]

5. 메인 브렌치로 변경하기
(2020년도부터 깃허브 기본 브랜치 master -> main으로 변경됨)

    'git branch -M main'

6. 원격 저장소에 업로드하기(push)
    'git push -u origin main'
    
    'git push
    [원격저장소 이름]
    [원격저장소 브랜치]'

- 기본 원격저장소의 이름은 'origin' 기본 브랜치의 이름은 'main  이다'

### 용어 정리
- Git(깃) : VCS (Version Control System) 버전 관리 시스템
- GitHub : Git으로 관리하는 프로젝트를 원격으로 공유하는 사이트
- GUI : Graphic User Interface, 마우스를 화면을 클릭해서 상용하는 방식
- CLI : Command Line Interface, 명령어를 하나씩 입력해서 사용하는 방식
- commit : 버전 관리를 통해 생성된 파일, 또는 행위
- log : 지금까지 만든 커밋을 모두 확인
- 로컬 저장소 : 내 컴퓨터 안의 Git 프로젝트
- 원격 저장소 : GitHub에 업로드 된 Git 프로젝트
- push : 로컬 저장소 -> 원격 저장소로 올리는 것 
- pull : 원격 저장소 -> 로컬 저장소로 내려받는 것

## 토큰 만들기
- GitHub에서 2021년 8월부터 비밀번호 대신 Token을 사용하도록 업데이트(보안문제)
- 깃헙 프로필(우측상단) > Developer > settings > 왼쪽 메뉴 최하단 스크롤 > Personal access token > Genereate new token(classic)
- 기한, 권한(scope) 선택
- 생성된 토큰은 더 이상 보여지지 않으므로 중요한 곳에 저장

### 소스트리에서 토큰 적용하기
- 최상단 메뉴 [도구] => [옵션] => [인증]
- 계정선택 => 편집 => 인증 : Personal Access Token 선택 후 복사한 토큰 붙여넣기

### Git 저장방식 알아보기
- Git의 저장방식 SNAPSHOT
    - 변경된 파일을 통째로 저장
- 차이저만 저장하는 방식 : delta
- 순서
    1. 변경된 파일을 저장한다. (save)
    2. 스테이지로 올라간다. (git add)
    3. 스테이지의 스냅샷을 찍는다. (git commit)
    - 원격저장소 업데이트 (git push)

- 깃으로 관리하는 파일의 4가지 상태
    - 추적안된 상태 (untracked) : add를 하지 않은 경우
    - 추적된 상태 (tracked) : 이미 add가 된 경우
        1. 수정 없음 (unmodified) : 변경사항 없으면
        2. 수정 함 (modified) : 변경사항 있으면
        3. 스테이지 됨 (stage) : 스테이징 하면

    - 예시
     - 새로운 파일을 만들었을 때
        - untracked (추적안된 상태)
    - add를 통해 스테이징
        - untracked -> staged
        - 추적안됨 -> 스테이징(애딩)
    - commit을 통해 snapshot
        - staged -> unmodified
        - 스테이징 -> 수정없음
    - 한번 add가 된 상태에서 파일 내용이 변경 된 경우
        - unmodified -> modified
