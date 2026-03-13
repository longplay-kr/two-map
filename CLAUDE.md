# Terminus Map - Sweet Home, Oregon Interactive Map

## 프로젝트 개요

좀비 아포칼립스 턴제 생존 게임(C:\dev\two)의 **팀 공유용 인터랙티브 월드맵**.
플레이어는 Terminus라는 피난처를 찾아가는 것이 목표.

## 세계관

- **Sweet Home, Oregon** (Linn County) 실제 지리 기반
- **Terminus** = Sweet Home Station (Albany & Eastern Railroad 종점)에 세워진 생존자 피난처
- Walking Dead의 Terminus 컨셉 차용 — Atlanta의 원래 이름이 "Terminus"였던 것처럼, 철도 종점 = Terminus
- 지명은 실제 Sweet Home 지명 사용 (South Santiam River, U.S. Route 20, Sankey Park 등)
- 상세 지명 문서: C:\dev\two\PLACES.md

## 기술 스택

- **Leaflet.js** (CDN) — 인터랙티브 맵 뷰어
- **map.png** — Unity 월드 에디터에서 캡처한 탑다운 맵 이미지
- **places.json** — 지명 데이터 (이름, 타입, 좌표, 줌 레벨)
- 서버 없이 정적 파일만으로 동작 (GitHub Pages 호스팅 예정)

## 파일 구조

- `index.html` — Leaflet 뷰어. 줌 레벨별 지명 표시, 타입별 색상, 호버 툴팁
- `places.json` — 지명 데이터. x/y는 퍼센트(0-100), minZoom으로 표시 줌 레벨 제어
- `map.png` — 월드맵 이미지 (C:\dev\two 월드 에디터에서 캡처)

## 지명 타입과 색상

| type | 색상 | 설명 |
|------|------|------|
| city | 흰색 #fff | 도시명 |
| landmark | 노랑 #f59e0b | Terminus, Foster Dam 등 |
| station | 빨강 #f87171 | 역/간이역 |
| river | 파랑 #60a5fa | 강/하천 |
| road | 회색 #d1d5db | 도로 |
| park | 초록 #4ade80 | 공원 |
| direction | 회색 #a1a1aa | 맵 외곽 방향 표시 |

## 현재 상태

- places.json의 좌표(x, y)는 **임시값** — 맵을 보면서 실제 위치에 맞게 조정 필요
- 로컬 실행: `python -m http.server 8080` 후 http://localhost:8080
- GitHub Pages 호스팅 미설정

## 게임 프로젝트 참조

- 게임 리포: C:\dev\two
- 지명 문서: C:\dev\two\PLACES.md
- 월드맵 데이터: C:\dev\two\Assets\StreamingAssets\Worlds\World_01\World_01.json
- 월드 섹터: 5x5 그리드 (Sector_0_0 ~ Sector_4_4), 섹터당 400m

## 한국어 사용

- 주석, 커밋 메시지는 한국어
- 지명은 영어 (실제 미국 지명)
