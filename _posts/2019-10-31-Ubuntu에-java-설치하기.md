---
layout:     post
title:      "Ubuntu에 java 설치하기"
date:       2019-10-31 21:30:12
categories: 개발환경
tags:       개발환경 AWS
mathjax:    true
---

* Content
{:toc}

Ubuntu java 설치하기



## 자바 버전 확인하기

![](/img-in-posts/Ubuntu에-java-설치하기-1.png)

인스턴스를 생성하고 자바를 설치하지 않았으면 이렇게 뜰 것이다.

다음 명령어를 입력해 java를 설치하도록 하자.

## 자바 설치하기

```bash
sudo apt update
sudo apt install openjdk-8-jdk openjdk-8-jre
```

![](/img-in-posts/Ubuntu에-java-설치하기-2.png)

y를 누르고 나면 설치가 진행된다.

![](/img-in-posts/Ubuntu에-java-설치하기-3.png)

## 자바 버전 재확인하기

![](/img-in-posts/Ubuntu에-java-설치하기-4.png)

설치가 되었다.

## 자바 환경변수로 설정하기 및 확인 하기

```bash
cat >> /etc/environment <<EOL
JAVA_HOME= /usr/lib/jvm/java-8-openjdk-amd64
JRE_HOME=/usr/lib/jvm/java-8-openjdk-amd64/jre
EOL

sudo vi /etc/environment
```

![](/img-in-posts/Ubuntu에-java-설치하기-5.png)

## 환경변수 테스트 하기

```bash
echo $JAVA_HOME
```

![](/img-in-posts/Ubuntu에-java-설치하기-6.png)


## 인용

> [How to Install JAVA 8 on Ubuntu 18.04/16.04, Linux Mint 19/18](https://tecadmin.net/install-oracle-java-8-ubuntu-via-ppa/)

> [Ubuntu에 Java설치 및 환경 설정하는 방법](https://ourcstory.tistory.com/129)
