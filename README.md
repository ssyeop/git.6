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
