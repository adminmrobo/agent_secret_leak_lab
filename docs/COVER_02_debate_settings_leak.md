# 표지 지시문 — 02 토론의 밤

| 항목 | 내용 |
|---|---|
| 키 · 판 | cover_02 · L (16:9, 1920 이상) |
| 장소 (앵커) | B 연구실 — 연구실 안 작은 강당, 마주 보는 두 연단, 객석 |
| 주제 은유 | 무대 앞 탁자의 청록·빨강 투표함 두 개 사이로 빈 투표지가 떠다니고, 무대 위에 빛나는 노트 한 장 (글자 없음) |
| 등장 | 무대: 초파리(왼쪽 연단, 오른쪽을 봄) · 주판봇(오른쪽 연단, 왼쪽을 봄) · 박사(가운데 뒤, 사회) · 조수(옆, 집계판) / 무대 끝: 인턴 시아(작은 빈 깃발) / 객석 앞줄: 인턴 모아(응원) + 미공개 실루엣 셋 |
| 대체 글 (alt) | 연구실 강당 무대에서 초파리 연구원과 주판봇이 마주 서고, 박사와 조수가 진행하며, 인턴과 방청객이 객석에서 지켜보는 토론회 표지 |
| 앞 표지와 다른 점 | 01편은 복사기·금고·날아가는 종이, 02편은 강당·연단·투표함. 같은 노트 종이를 작게 이어 두어 연작임을 보여 줌 |
| 지킬 것 (캐릭터 팩 C9) | 미공개 X1~X3은 실루엣 그대로 — 성별·나이·실존 인물을 짐작하게 하는 묘사 금지, 얼굴 표정 없음. 결과 암시 금지(투표함 높이·표정 같게) |

**참고 이미지 (함께 올리기):** 박사·조수·초파리·주판봇 기본 그림 4장, 시아·모아 기본 그림(E13) 2장, X1~X3 실루엣 3장 (기준: GitHub `adminmrobo/fruitfly-lab-expressions`, `specs/sia/`, `specs/moa/`, `specs/spares/`). 참고 그림이 많으면 생성기가 섞을 수 있으니, 먼저 무대 네 캐릭터만으로 한 장을 만들고 같은 대화에서 "add the interns and silhouettes"로 더하는 순서를 권합니다.

**Genspark에 붙여 넣기 ↓**
```
웹페이지 맨 위에 거는 표지 그림 1장을 만들어 줘.
- 비율 16:9, 가로 1920px 이상
- 첨부한 참고 이미지의 캐릭터들을 같은 그림체·같은 외형으로
- 그림 안에 글자·숫자·로고를 넣지 말 것 (칠판·깃발·투표지는 비워 둘 것)
- 얼굴과 손은 가장자리에서 떨어진 가운데 영역에, 왼쪽 아래 구석은 어둡고 단순하게
아래 영어 프롬프트를 그대로 써 줘.

Website top cover illustration, wide 16:9.
Match the art style, proportions and colors of the attached reference images exactly (if there are no reference images: 16-bit RPG style pixel art, bold dark outline, 2–3 tone shading, small highlights).
Cozy night laboratory mood, purple light, soft magenta and green fluorescent accents.
Scene: a small lecture hall inside the same night lab world, a low wooden stage with two podiums facing each other, a blank chalkboard behind, rows of audience seats in the foreground, purple lab light spilling in from one side.
On stage, all four main characters:
  anthropomorphic fruit fly researcher, black body, big red compound eyes, blue helmet with a gold stripe and pink and blue cables, white lab coat over a black vest, black gloves, transparent wings, at the left podium facing right, one eye narrowed, pointing forward;
  boxy beige retro CRT-monitor robot, dark green screen face with mint pixel eyes and mouth, short antenna topped with a red-brown abacus bead, gray segmented arms, two small tank treads, at the right podium facing left, holding up a wooden abacus;
  chibi scientist, thin teal rectangular glasses, spiky black hair with one white streak, small ponytail, white lab coat over black vest and tie, standing at the back center between the podiums with one finger raised like a moderator;
  girl researcher, long pink hair with two round buns and a navy streak, blue eyes, white lab coat over lavender hoodie, jeans, at the side of the stage holding a tally board with blank striped rows.
At the stage edge: intern Sia, waist-length straight jet-black hair, side-swept bangs, no hair accessory, gray eyes, small silver drop earrings, long-sleeved charcoal-black maid dress with a large gray ribbon and an ankle-length white frilled apron, holding a small blank flag, calm.
In the front audience row: intern Moa, ash-beige long hair with wavy ends, white frilled maid headband and a white ribbon above the left ear, amber eyes, white shirt with a red and navy check ribbon tie, camel knit cardigan, white frilled apron, black skirt, cheering with a fist;
  next to her three small mysterious audience members drawn as dark navy silhouettes with tiny white dot eyes, each with one accent-colored prop (one pink ribbon, one pair of round teal glasses, one small gold bell), seated, faces unreadable.
Visual metaphor of the topic: two ballot boxes on a small table in front of the stage, one teal and one red, with blank paper slips floating between them; a faint glowing notebook page above the stage.
Composition: keep every face and hand inside the central safe area (12% margin left and right, 10% top, 18% bottom); keep the bottom-left corner dark and simple; the light falls on the two podiums and the ballot boxes.
Mood: lively debate night, friendly rivalry, the moment before the vote result.
No text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands.
```

**고칠 때 (같은 대화에서):** `Same characters, same art style and composition. Change only: {고칠 점}. Still no text.`

**받은 뒤:** SKILL 18-15 절차 → `<!-- lab-cover -->` 사이 대체 표지 교체 → `cover_manifest.json`의 `cover_02` 상태를 `received` → 반영 후 `ok`.
