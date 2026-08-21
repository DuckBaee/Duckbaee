<div align="center">

# 한종훈

### Game Client Programmer

게임 플레이에 직접 연결되는 기능을 구현하고,
프로젝트에서 발견한 문제를 **구조와 코드의 개선으로 연결하는 클라이언트 프로그래머**를 목표로 하고 있습니다.

`Unity` `C#` `Gameplay` `Network` `AI` `Data`

<br>

<!-- 필요 시 PDF 포트폴리오 링크 추가 -->

**[Portfolio PDF](포트폴리오_링크)**

</div>

---

## Featured Projects

### DISTORIA

**3D Roguelike FPS · Unity · C#**

16인 팀 프로젝트에서 클라이언트 프로그래밍을 담당했습니다.

* 플레이어 액션 및 게임플레이 기능 구현
* 카메라 피드백 및 전투 연출 연결
* FMOD 기반 사운드 데이터 연동
* Scene Group 기반 로딩 구조 구현

**Key Topics**
`Gameplay` `Camera` `FMOD` `Scene Loading`

→ **[View Repository](DISTORIA_레포지토리_링크)**

---

### DODODOIT!

**3D Rope Action Runner · Unity · C#**

로프 액션의 조작 방식을 직접 프로토타이핑하고,
플레이 테스트 결과를 기반으로 조작 방식과 플레이어 상태 구조를 개선했습니다.

* Rigidbody 기반 플레이어 이동
* Grappling System 구현
* State Pattern 기반 플레이어 상태 관리
* Cinemachine 기반 카메라 연동
* 여러 로프 조작 방식 프로토타이핑 및 비교

**Key Topics**
`Gameplay` `State Pattern` `Physics` `Cinemachine`

→ **[View Repository](DODODOIT_레포지토리_링크)**

---

### Network Project

**Dedicated Server · Client / Server**

위치 동기화와 채팅 기능을 제공하는 Dedicated Server 프로젝트를 개발했습니다.

* Client / Server 통신 구조 구현
* 플레이어 위치 동기화
* 이동 데이터 전송 방식 설계
* 현재 위치 전송과 목적지 기반 동기화 방식 비교
* 네트워크 데이터 구조 설계

**Key Topics**
`Networking` `Dedicated Server` `Synchronization` `Protocol`

→ **[View Repository](NETWORK_레포지토리_링크)**

---

### AR AutoBattler

**Unity 6 · Behaviour Tree · AR**

Unity 6의 Behaviour Tree와 AR 기능을 활용해
오토배틀러 형식의 게임을 제작했습니다.

* Behaviour Tree 기반 유닛 행동 구현
* 기본 노드의 한계를 보완하기 위한 Custom Action 제작
* Runtime Blackboard를 활용한 데이터 관리
* AR Foundation 기반 카메라 시점 이동
* Android 환경에서 동작하는 게임플레이 구현

**Key Topics**
`Behaviour Tree` `AI` `AR Foundation` `Unity 6`

→ **[View Repository](AR_레포지토리_링크)**

---

## Additional Engineering Experience

이력서에서 비중 있게 다루지 않았지만, 프로젝트를 진행하며 직접 구현하거나 개선한 경험입니다.

### Gameplay Prototyping

* 확정되지 않은 게임 사양을 빠르게 검증하기 위한 기능 프로토타입 제작
* 여러 Grappling 조작 방식을 실제 플레이 가능한 형태로 구현
* 플레이 테스트 결과를 기반으로 조작 방식 비교 및 수정
* 기능 추가 과정에서 발생한 상태 관리 복잡도를 구조 개선으로 연결

---

### Client Architecture

* 플레이어 행동을 상태 단위로 분리하여 기능별 책임 관리
* 기능 확장 과정에서 클래스 간 역할과 의존성 재정리
* 게임 로직과 데이터의 역할 분리
* 새로운 기능 추가 시 기존 코드 수정 범위를 줄이기 위한 구조 개선

---

### Networking

* Client / Server 간 데이터 송수신 구현
* 플레이어 위치 동기화 방식 설계
* 전송 데이터의 의미와 크기를 고려한 구조 변경
* 현재 위치 Snapshot과 목적지 기반 이동 데이터 방식 비교

---

### Data Management

* JSON 기반 게임 데이터 관리
* SQLite 기반 데이터 저장 구조 구현
* 데이터 간 `1:N` 관계 구성
* DB 데이터를 게임에서 사용할 수 있는 객체 형태로 매핑
* 데이터와 게임 로직의 결합도를 줄이기 위한 구조 개선

---

## Tech Stack

<table>
<tr>
<td><b>Game Engine</b></td>
<td>Unity</td>
</tr>

<tr>
<td><b>Language</b></td>
<td>C#</td>
</tr>

<tr>
<td><b>Gameplay</b></td>
<td>State Pattern · Physics · NavMesh · Cinemachine</td>
</tr>

<tr>
<td><b>AI</b></td>
<td>Behaviour Tree · Blackboard</td>
</tr>

<tr>
<td><b>Network</b></td>
<td>Client / Server · Dedicated Server · Position Synchronization</td>
</tr>

<tr>
<td><b>Data</b></td>
<td>SQLite · JSON</td>
</tr>

<tr>
<td><b>Tools</b></td>
<td>Git · GitHub · Visual Studio</td>
</tr>
</table>

---

## Repository Guide

대표 프로젝트 Repository에서는 다음 내용을 중심으로 정리합니다.

```text
README
 ├─ Project Overview
 ├─ My Contribution
 ├─ Architecture
 ├─ Core Systems
 └─ Source Code Guide

Source
 ├─ Gameplay
 ├─ System
 ├─ Network / Data
 └─ Utility

Docs
 └─ Architecture / Flow Diagram
```

팀 프로젝트의 경우 **제가 직접 작성한 코드 중 공개 가능한 부분만 별도로 정리하며,
다른 팀원의 코드와 프로젝트 에셋은 포함하지 않습니다.**

---

<div align="center">

### Contact

**GitHub** · 현재 페이지
**Portfolio** · PDF Portfolio

</div>
