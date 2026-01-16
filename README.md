# Test GPG

GNU PG (GNU Privacy Guard) 의 사용법 테스트

## gpg 사용법

### 설치

```
$ brew install gpg
```

### key 생성

```
$ gpg --full-generate-key
```

### public key 추출

```
$ gpg --export -a <mail_address>
```

### key 확인

secret key

```
$ gpg --list-secret-keys --keyid-format=long
```

public key
```
$ gpg --list-keys --
```
* 서명용 subkey의 key id를 확인할 것.

## git에 GPG key 등록

```
$ gpg config user.signingkey <GPG_KEY_ID>
$ gpg config commit.gpgsign true
```

* `.git/config` 에 관련 설정이 기록됨.
* `<GPG_KEY_ID>` : 서명용 subkey


## GigHub에 GPG public key 등록

GitHub → Settings → SSH and GPG keys → New GPG key

## commit 하기

일반적으로 `gpg config commit.gpgsign true` 인 경우, `commit`을 하면 자동으로 서명이 이루어짐.

`false`로 된 경우엔 `commit -S` 로 `-S`옵션을 주면 된다.

