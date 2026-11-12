# 01번 「승인 한 번이 유출이 되기까지」 이미지 제작 명세서

| 항목 | 내용 |
|---|---|
| 페이지 | 01_settings_leak_probability.html |
| 모드 / 주 앵커 | 교과서 / B 연구실 (실험 노트 → 복사기 → 도서관, 금고 문) |
| 분야 | 통계학(주) + 인공지능·경제학(보조) |
| 시즌 | 기본 |
| 대결 | 공개 저장소 99개, 무작위 10개 vs 전수 99개 → 결과 R(주판봇 승), 차이 84.4%p |
| 새로 그릴 그림 | P1 1장 · P2 1장 · P3 1장 |
| 재사용 | 표정 15키 (캐릭터 팩 `character_pack` 1.3에 모두 있음) |
| 그림이 없을 때 | 페이지는 대체 표지(CSS 금고 + 픽셀 캐릭터 넷)와 팩 그림으로 이미 완성 상태 |

## 1. 그림체와 고정 외형
- 스타일: 캐릭터 팩 18-3 (16비트 RPG 픽셀아트, 굵은 외곽선, 2~3단계 명암)
- 고정 외형: 캐릭터 팩 18-4 표 그대로
- 이 페이지 장소: 밤의 연구실 전경, 복사기와 벽의 둥근 금고 문, 열린 문 너머 서가
- 장소 영어 묘사: *wide night laboratory with test tube racks, stacks of lab notebooks, a boxy office photocopier glowing softly, and a large round vault door set into the back wall*

## 2. 필요한 그림 전체

| # | 키 | 판 | 크기 | 상태 | 우선 | 들어가는 곳 | 대신 쓰는 그림 |
|---|---|---|---|---|---|---|---|
| 0 | cover_01 | L | 1920×1080 | 새로 (COVER_01_settings_leak_probability.md) | P1 | 맨 위 글 표지 | 대체 표지 (CSS 금고 + 팩 그림 넷) |
| 1 | doc_think | A | 192×192 | 재사용 | — | 표지, 히어로 첫마디, 대결 판정 전 | doc_front |
| 2 | doc_front | A | 192×192 | 재사용 | — | 등장인물, 아웃트로 | — |
| 3 | doc_judge | A | 192×192 | 재사용 | — | ④ 말풍선, 대결 판정 후 | doc_front |
| 4 | asst_smile / asst_firm / asst_report / asst_spark | B | 180×220 | 재사용 | — | 히어로, 대결 발표, ②·꾸러미 말풍선, 아웃트로 | asst_smile |
| 5 | fly_point / fly_clip / fly_magnify / fly_coffee | C | 220×220 | 재사용 (왼쪽을 보는 그림이라 CSS 좌우 반전) | — | 히어로, 대결 전, ① 말풍선, 아웃트로 | fly_clip |
| 6 | fly_cry | C | 220×220 | 재사용 | — | 대결 후 (차이 10%p 이상) | fly_coffee |
| 7 | robo_coin / robo_smile / robo_calc / robo_happy | D | 180×200 | 재사용 | — | 히어로, 대결 전·후, ③ 말풍선, 행동 캔버스, 아웃트로 | robo_smile |
| 8 | thumb_01 | I | 600×400 | 새로 (cover_01을 3:2로 자르기) | P2 | 목차 카드 | 색 카드 |
| 9 | og_01 | K | 1200×630 | 새로 (cover_01 자르기) | P3 | 공유 미리보기 | 없음 |
| — | 행동으로 보기(카드·바구니·나무) | — | — | 코드 | — | 캔버스 | — |

## 3. 새로 그릴 그림 상세

### 3-1. `cover_01` — 승인 기록이 복사기를 지나 날아가는 밤의 연구실
| 항목 | 내용 |
|---|---|
| 판 · 크기 | L · 1920×1080 (2배 가능) |
| 배경 | 그림 전체 |
| 구도 | 초파리 왼쪽 앞(오른쪽을 봄), 주판봇 오른쪽 앞(왼쪽을 봄), 박사 가운데 뒤, 조수 왼쪽 옆. 날아가는 종이가 화면 가운데 위 |
| 표정·몸짓 | 박사 doc_think, 조수 셈하는 몸짓, 초파리 fly_point, 주판봇 robo_calc에 가까운 몸짓 |
| 소품 | 복사기, 둥근 금고 문, 줄무늬만 있는 노트·종이, 시험관 선반 (글자 없음) |
| 빛·분위기 | 보라 조명, 종이와 금고 손잡이에 노란빛 |
| 피할 것 | 승패 암시, 그림 속 글자, 실존 브랜드 복사기, 현미경·초파리 해부 소품 |
| 대체 글 (alt) | 밤의 연구실에서 네 캐릭터가 복사기를 지나 날아가는 빛나는 노트 종이와 벽의 금고 문을 바라보는 표지 |
| 대신 쓰는 그림 | 대체 표지 |

**프롬프트:** COVER_01_settings_leak_probability.md의 "Genspark에 붙여 넣기" 블록 그대로.

### 3-2. `thumb_01`, `og_01`
cover_01을 받은 뒤 `build_character_pack.py --ingest ./받은그림 --plates thumb_01=I,og_01=K`로 잘라 만든다. 새로 생성하지 않는다.

## 4. 일관성 지침
- 참고 이미지: 표정 기본 그림 4장 + 설정샷 k01(단체)·k12(키 비교)
- 키 순서: 박사 ≥ 조수 > 주판봇 > 초파리 (1.00 · 0.90 · 0.72 · 0.41)
- 투명 배경이 필요 없음 (L판)

## 5. 넘겨받은 뒤 처리
1. 비율 16:9, 그림 속 글자, 네 캐릭터 외형 확인
2. WebP 1600×900 (220 KB 이하) — 단일 파일이므로 base64 하나만
3. `<!-- lab-cover -->` 사이 블록을 SKILL 18-14-5 `<picture>` 블록으로 교체
4. 390·768·1280 폭 점검, 페이지 그림 합계 표지 포함 600 KB 이하 (현재 표정 팩 약 88 KB)

## 6. 체크리스트
- [x] HTML의 모든 `data-img` 키가 이 명세서에 있음
- [x] 대결 후 표정이 5-8 표와 일치 (R, 차이 ≥ 10%p → fly_cry, robo_happy)
- [x] 결과 전 그림에 승패 암시 없음 (fly_point, robo_coin)
- [x] 생물 앵커가 아니므로 현미경·해부 소품 없음
- [x] P1 1장 (6장 이하)

## 7. 매니페스트
```json
{
  "page": "01_settings_leak_probability",
  "anchor": "B:lab-copier-vault",
  "season": "default",
  "duel": {"result": "R", "gap": 0.844},
  "images": [
    {"key":"cover_01","plate":"L","size":[1920,1080],"status":"new","priority":"P1","slot":"cover","fallback":"css-pixel-four","alt":"밤의 연구실에서 네 캐릭터가 복사기를 지나 날아가는 빛나는 노트 종이와 벽의 금고 문을 바라보는 표지"},
    {"key":"thumb_01","plate":"I","size":[600,400],"status":"new-crop","priority":"P2","slot":"index-card","fallback":"color-card"},
    {"key":"og_01","plate":"K","size":[1200,630],"status":"new-crop","priority":"P3","slot":"og","fallback":null},
    {"key":"doc_think","plate":"A","status":"reuse"},{"key":"doc_front","plate":"A","status":"reuse"},{"key":"doc_judge","plate":"A","status":"reuse"},
    {"key":"asst_smile","plate":"B","status":"reuse"},{"key":"asst_firm","plate":"B","status":"reuse"},{"key":"asst_report","plate":"B","status":"reuse"},{"key":"asst_spark","plate":"B","status":"reuse"},
    {"key":"fly_point","plate":"C","status":"reuse"},{"key":"fly_clip","plate":"C","status":"reuse"},{"key":"fly_magnify","plate":"C","status":"reuse"},{"key":"fly_coffee","plate":"C","status":"reuse"},{"key":"fly_cry","plate":"C","status":"reuse","slot":"duel-after"},
    {"key":"robo_coin","plate":"D","status":"reuse"},{"key":"robo_smile","plate":"D","status":"reuse"},{"key":"robo_calc","plate":"D","status":"reuse"},{"key":"robo_happy","plate":"D","status":"reuse","slot":"duel-after"}
  ]
}
```
