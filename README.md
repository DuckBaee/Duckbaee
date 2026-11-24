<div align="center">

# 한종훈

### Game Client Programmer

게임플레이 기능을 구현하고,
개발 과정에서 발견한 문제를 **구조와 코드의 개선으로 연결하는 클라이언트 프로그래머**를 목표로 하고 있습니다.

`Unity` `C#` `Gameplay` `AI` `Data`

<br>

<!-- PDF 포트폴리오 완성 후 실제 링크로 교체 -->

[**Portfolio PDF**](https://github.com/DuckBaee/Portfolio)

</div>

---

## Featured Projects

### 🧩 Procedural Level Generator & Unity Room Editor

**Unity 6 · C# · UI Toolkit · AI 협업 개발**

**첫 주의 셀 범위 표시부터 맵 생성기·최적화·통합 제작 툴까지 발전시킨 프로젝트**입니다. 포털 정렬과 예약 영역 충돌 검사, 시나리오 기반 DFS·백트래킹을 개발하고 이후 공간·아트·포털·규칙 편집으로 확장했습니다. 요구사항과 설계 정책을 결정하고 AI의 구현 안내·코드 작성·검토와 실제 실행 피드백을 연결했습니다.

**AI Collaboration**

* 질문형 요구사항 점검 → 명세·수용 기준 → AI 구현 → 실행 검증 → 피드백·수정
* 45도 포털 문제를 계기로 셀 조립에서 예약 공간 중심의 제작 흐름으로 재설계
* AI 작성·수정 코드 포함 사실과 직접 결정한 설계·검증 범위를 공개

**Optimization & Highlights**

* 시나리오 깊이 기반 DFS, 후보 재시도, 유일 단계 대체 말단과 체크포인트 역순 복구
* AABB Broad Phase로 정밀 충돌 검사 후보 축소 및 예약 박스·경계 재사용
* 당시 사용자 측정 집계: 평균 생성 시간 **약 6.595초 → 0.601초(약 11배)**, 검사 진입 **약 4,443만 → 339만 회**
* 공간 검사 결과 재사용과 상태 관찰 주기 제한
* HashSet 기반 셀 중복 처리·no-op 감지
* 다중 Collider 이벤트 중복 억제와 머무름 실행 간격 제어
* 조건부 생성 1회 초기화와 방 인스턴스별 상태 분리
* Play 중 자동 편입 간섭 수정 후 생성 회귀 검사 40/40 PASS

생성 성능 수치는 OFF/ON 총 80회에 대한 당시 사용자 보고이며 이번에 재측정하지 않았습니다. 개별 로그·환경과 결과 동등성 재검증 한계는 최적화 문서에 명시했습니다. 완성 씬 FPS 개선 수치와 구분합니다.

→ [1주차부터 전체 개발 과정](https://github.com/DuckBaee/Unity-Room-Editor/blob/main/docs/PROJECT-HISTORY.md)

**`AI-assisted Development` `Editor Tool` `Optimization` `UI Toolkit` `Verification`**

→ **[View Repository](https://github.com/DuckBaee/Unity-Room-Editor)**

→ [AI 협업 과정](https://github.com/DuckBaee/Unity-Room-Editor/blob/main/docs/AI-WORKFLOW.md) · [최적화 접근](https://github.com/DuckBaee/Unity-Room-Editor/blob/main/docs/OPTIMIZATION.md)

---


### 🎮 DISTORIA

**3D Roguelike FPS · Unity · C# · 16인 팀 프로젝트**

여러 플레이어 행동의 충돌 관리부터 반동, 카메라 피드백, 사운드 데이터 자동화, Scene Loading까지 실제 게임 흐름에 필요한 클라이언트 시스템을 구현했습니다.

**Highlights**

* Action Flag + BlockCount 기반 Player Action 관리
* Curve · Kick · Noise · Spring 기반 Recoil System
* Camera Feedback 간 Transform 간섭 분리
* FMOD Bank → ScriptableObject Editor Pipeline
* SceneGroup 기반 Additive Loading Flow

**`Gameplay` `Architecture` `Camera` `Editor Tool` `Loading`**

→ **[View Repository](https://github.com/DuckBaee/Distoria-Client)**

---

### 🪢 DODODOIT!

**3D Rope Action Runner · Unity · C# · 12인 팀 프로젝트**

불확실했던 로프 액션을 여러 방식으로 프로토타이핑하고, 실제 플레이 결과를 바탕으로 이동 방식과 상태 구조를 단계적으로 개선했습니다.

**Evolution**

`SpringJoint Prototype`
↓
`Fixed Radius Swing`
↓
`Enter → Swing → Exit`
↓
`Targeting · Rotation · Camera · Sound Integration`

**Highlights**

* Grappling Control 방식 비교 및 프로토타이핑
* 고정 반경 · 회전 기반 Swing 구현
* Rope Lifecycle State 분리
* 로컬 축 기반 Target Detection
* Cinemachine · FMOD 연동 및 Release 안정화

**`Gameplay` `Prototyping` `State` `Physics` `Cinemachine`**

→ **[View Repository](https://github.com/DuckBaee/DoDoDoIt-Grappling)**

---

### 🌐 TCP Destination Sync

**Unity Client · C# · TCP Server**

현재 위치를 일정 주기로 전송하던 초기 구조에서, 클릭 이동 방식의 실제 의미에 맞춰 **목적지를 이벤트 시점에 전달하는 구조**로 변경했습니다.

```text
AS-IS
Current Position
→ every 0.5 sec
→ Server
→ SetDestination

TO-BE
Click Destination
→ Server
→ Broadcast
→ SetDestination
```

**Highlights**

* TCP Client / Server 통신
* Player ID 및 Socket Mapping
* 이동 · 채팅 Message 처리
* Position Snapshot → Destination Sync 변경
* 실제 구현 한계와 개선 방향 분석

**`Networking` `Client/Server` `Synchronization` `Protocol`**

→ **[View Repository](https://github.com/DuckBaee/TCP-Destination-Sync)**

---

### 🤖 AR Autobattler

**Unity 6 · C# · Unity Behavior · AR Foundation**

Autobattler의 전투 규칙을 Unity Behavior에 연결하고, 기본 Node만으로 표현하기 어려운 Target Selection을 Custom Action으로 확장했습니다.

**Highlights**

* 체력 비율 기반 Healer Target Selection
* Custom Behavior Action 구현
* Runtime Blackboard 기반 상태 데이터 관리
* Behavior Graph와 Gameplay Logic 연결
* AR Plane Raycast 기반 Battlefield 배치

**`AI` `Behaviour Tree` `Blackboard` `AR Foundation`**

→ **[View Repository](https://github.com/DuckBaee/AR-Autobattler)**

---

### 💾 Soul Gemstone

**Unity · C# · SQLite · Android**

하나의 JSON 목록으로 관리하던 기록 데이터를 `Book : Diary = 1:N` 구조로 분리하고, SQLite에 저장한 관계형 데이터를 다시 게임의 객체 구조로 복원했습니다.

```text
JSON
DailyLogData + logGroup

        ↓

SQLite
BookData 1 : N DiaryData
```

**Highlights**

* JSON → SQLite 데이터 구조 변경
* Book / Diary 1:N 관계 설계
* 관계 ID 기반 데이터 조회
* DB Row → C# Object Graph 복원
* 당시 구현의 한계와 개선 방향 정리

**`Data` `SQLite` `Persistence` `Object Mapping`**

→ **[View Repository](https://github.com/DuckBaee/SoulGemstone-Data)**

---

## Tech Stack

<table>
<tr>
<td><b>Engine</b></td>
<td>Unity</td>
</tr>

<tr>
<td><b>Language</b></td>
<td>C#</td>
</tr>

<tr>
<td><b>Gameplay</b></td>
<td>State · Physics · NavMesh · Cinemachine</td>
</tr>

<tr>
<td><b>AI</b></td>
<td>Unity Behavior · Behaviour Tree · Blackboard</td>
</tr>

<tr>
<td><b>Data</b></td>
<td>SQLite · JSON · ScriptableObject</td>
</tr>

<tr>
<td><b>Audio</b></td>
<td>FMOD Integration</td>
</tr>

<tr>
<td><b>Tools</b></td>
<td>Git · GitHub · Visual Studio</td>
</tr>
</table>

---

## Repository Guide

각 프로젝트 Repository는 실행 가능한 Unity 프로젝트를 재구성한 것이 아니라,
**프로젝트별 구현 코드, 개발 과정과 기여 범위를 검토하기 위한 코드 포트폴리오**입니다.

AI 협업 프로젝트인 Unity Room Editor에는 AI가 작성·수정한 코드가 포함되어 있으며, 직접 결정한 요구사항·설계 방향과 AI 활용 범위, 검증 근거를 별도로 설명합니다. 이 프로젝트의 공개 이력은 현재 상태의 스냅샷이며 원본 개발 커밋 이력을 재현한 것은 아닙니다.

```text
README
  ↓
문제와 구현 의도
  ↓
Architecture / Evolution
  ↓
실제 Source Code
  ↓
Git History / Code Ownership
```

팀 프로젝트에서는 다른 팀원의 코드와 외부 Asset을 제외하고,
공동 수정 파일은 Git History와 Blame을 기준으로 기여 범위를 별도로 표시했습니다.

---

<div align="center">

### 한종훈 · Game Client Programmer

`Unity` `C#` `Gameplay` `AI` `Data`

</div>
