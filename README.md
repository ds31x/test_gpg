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
$ gpg --list-keys
```

## git에 GPG key 등록

```
$ gpg config user.signingkey <GPG_KEY_ID>
$ gpg config commit.gpgsign true
```

## GigHub에 GPG public key 등록

GitHub → Settings → SSH and GPG keys → New GPG key



