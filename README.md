# 띄어쓰기 점프 레이스 — 아케이드 맵 (2인 턴제)

초등 1~2학년용 띄어쓰기 학습 게임. 클릭만으로 2인 턴제 경쟁, 테마 랜덤, 아이템, 보스전 지원.

## 폴더 구조
```
spacing-race-game/
├─ index.html
├─ questions.json        # 문제은행(정답/오답 확정, 보스전 별도)
└─ assets/
   └─ sfx/
      ├─ bgm.wav
      ├─ correct.wav
      ├─ wrong.wav
      ├─ item.wav
      └─ boss.wav
```

## 로컬 미리보기
1) `index.html`을 더블클릭(브라우저로 열기)
   - 일부 브라우저는 로컬 파일에서 `fetch(questions.json)` 보안 제한이 있을 수 있어요.  
     안 되면 VSCode의 Live Server 확장 또는 아무 로컬 서버 사용 권장.

## GitHub Pages 배포
1) GitHub에 새 레포를 만들고(예: `spacing-race-game`), 위 파일들을 업로드
2) Settings → *Pages* → **Deploy from a branch**
3) Branch: `main` / Folder: `/ (root)` → Save
4) 잠시 후 Pages 주소가 활성화됩니다. (예: `https://ID.github.io/spacing-race-game/`)

## 문제 추가/수정
- `questions.json`의 `regular` 또는 `boss` 배열에 객체를 추가하세요.
- 형식: 
```json
{ "q": "나는밥을먹어요", "correct": "나는 밥을 먹어요", "wrong": "나는밥을 먹어요" }
```
- 저장 후 브라우저 새로고침하면 반영됩니다.

## 커스텀 팁
- `index.html`에서 THEMES를 수정하면 배경/발판 색감 변경 가능
- 보스 위치: `S.bossAt` 값으로 조정
- 아이템 확률: `if(Math.random()<0.35)` 값 조정
- 5연속 정답 시 자동 부스트(2칸 전진)
