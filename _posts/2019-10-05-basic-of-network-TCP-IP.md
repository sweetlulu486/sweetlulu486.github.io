---
layout: post
title:  "네트워크의 기본 TCP/IP"
date:   2019-10-05 10:45:12
categories: network
tags: basic
---

* Content
{:toc}

> [그림으로 배우는 HTTP & Network Basic(영진닷컴, 이병억)](http://www.kyobobook.co.kr/product/detailViewKor.laf?ejkGb=KOR&mallGb=KOR&barcode=9788931447897&orderClick=LEA&Kc=)
> 에 있는 내용을 정리한 것입니다.

# TCP/IP는 프로토콜의 집합
컴퓨터와 네트워크 기기가 상호간에 통신하기 위해서는 서로 같은 방법으로 통신해야 합니다. 그렇기 때문에 모든 요소에 규칙을 결정합니다. 즉, `통신 방법에 대한 규칙을 프로토콜`이라고 부릅니다.
프로토콜에는 여러 가지가 있습니다. 케이블 규격이랑 IP 주소 지정 방법, 떨어진 상대를 찾기 위한 방법과 그 그곳에 도달하는 순서 , 그리고 웹을 표시하기 위한 순서 등입니다.
TCP와 IP 프로토콜을 가리켜 TCP/IP라고 부르기도 하지만, IP 프로토콜을 산용한 통신에서 사용되고 있는 프로토콜을 총칭해서 TCP/IP라는 이름이 사용되고 있습니다.

# 계층으로 관리하는 TCP/IP
TCP/IP에서 중요한 개념 중 하나가 계층입니다. 계층화가 된 것은 메리트가 있기 떄문입니다. 예를 들면, 인터넷이 하나의 프로토콜로 되어 있다면 어디선가 사양이 변경되었을 때 전체를 바꿔야 하지만, `계층화가 되어 있으면 사양이 변경된 해당 계층만 바꾸면 됩니다.` 각 계층이 연결되어 있는 부분만 결정되어 있어, 각 계층의 내부는 자유롭게 설계할 수 있습니다.
또한, 계층화를 하면 설계를 편하게 할 수 있습니다. 애플리케이션 층에서 애플리케이션은 자기 자신이 담당하는 부분만 고려하면 되고, 상대가 어디에 있는지 어떠한 루트로 메세지를 전달하는지, 전달한 메세지가 확실하게 전달되고 있는지 같은 고려를 하지 않아도 됩니다.

# TCP/IP 각 계층의 역할
- 애플리케이션 계층 : 유저에게 제공되는 애플리케이션에서 사용하는 통신의 움직임 결정
- 트랜스포트 계층 : 애플리케이션 계층에 네트워크로 접속되어 있는 2대의 컴퓨터 사이의 데이터 흐름 제공
    - TCP의 단위는 세그먼트
    - UDP의 단위는 데이터그램
- 네트워크 계층 : 네트워크 계층은 네트워크 상에서 패킷의 이동 관리
    - 데이터 전송의 단위는 패킷
- 링크 계층 : 네트워크에 접속하는 하드웨어적인 부분 관리

# TCP/IP 통신의 흐름
![test](/_img/2019-10-05-basic-of-network-TCP-IP-1.png)
