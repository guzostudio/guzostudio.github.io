# webpage
This is a private repository for webpages of GuzoStudio: www.guzostudio.com

## 깃 관리 방법 안내

### 새 SSH 등록하기

SSH를 등록해야 로컬에서 원격저장소에 푸시가 가능합니다.

1. [Github ssh key 등록하는 법](https://brunch.co.kr/@anonymdevoo) 에 나온 글을 참고하여 SSH를 생성합니다.
```bash
$ ssh-keygen
```
> **참고**
> 어디에 저장할 지 물어볼 때 그냥 엔터를 쳤을때 현재 디렉토리에 생성됩니다.

> **중요**
> 암호를 두번 치는데 반드시 암호를 기억하도록 합니다. (커밋 내용을 푸시할때마다 암호입력을 요구할 수 있음.)

2. `Your public key has been saved in /Users/kkoko/.ssh/id_rsa.pub.` 이런 문구가 나오면 아래 명령어 실행
```bash
$ cat ~/.ssh/id_rsa.pub
```

3. 위 명령어를 실행했을 때 나온 SSH 값을 복사

4. **Github** 페이지에서 **프로필** 클릭 > **Settings** 클릭

5. **Settings** 화면 좌측 메뉴에 **SSH and GPG keys** 클릭

6. 타이틀은 알아서 정하고 SSH 입력란에 아까 복사했던 SSH를 붙여넣기.

### 레포 로컬에 다운받기 (Clone)

1. 레포를 다운 받을 폴더로 이동
```bash
$ cd ~/Desktop/GuzoStudio
```

2. Clone 시작
```bash
$ git clone git@github.com:guzostudio/webpage.git
```

### 작업을 위해 브랜치 생성하기
네이밍 규칙: `{이름}/{작업제목-대쉬로-구분}`

1. 터미널을 열고 깃이 있는 폴더로 이동
```bash
$ cd ~/Desktop/GuzoStudio/webpage
```

2. `develop` 브랜치로 이동 (Check-out)
```bash
$ git checkout develop
```

3. 새 브랜치 생성 및 해당 브랜치로 이동
```bash
$ git branch jaesung/webpage-1
$ git checkout jaesung/webpage-1 
```

### 작업 내용 커밋하기

1. 커밋을 하려면 아래 명령어를 실행합니다. 

> **중요** 커밋 메세지는 필수!!!

```bash
git add .
git commit -m "Add guideline for git to README.md"
```

### 작업 완료하면 푸시하기

2. 커밋 기록은 푸시하기 전까지 로컬에만 있기 때문에 Pull Request 를 위해 반드시 원격저장소로 푸시해야합니다

```bash
git push origin jaesung/webpage-1
```
