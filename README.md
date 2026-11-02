# V1C — Valorant Lineup Library

발로란트 맵별 **각귀체 / 각불 / 각리콘** 라인업을 찾아보는 개인용 정적 웹사이트입니다.

**사이트:** https://mmanimalmm.github.io/V1C/

## 사용법
- 상단에서 라인업 유형(각귀체, 각불, 각리콘)을 선택하세요.
- 맵, 공격/수비, 사이트, 요원, 검색어로 원하는 라인업을 필터링할 수 있습니다.
- 카드에서 **자세히 보기**를 누르면 설명과 영상(등록된 경우)을 확인할 수 있습니다.
- 다크/라이트 테마를 전환할 수 있습니다.

## 라인업 추가
`data/lineups.json`의 `lineups` 배열에 객체를 추가하세요.

```json
{
  "version": 1,
  "updatedAt": "2026-11-02",
  "lineups": [
    {
      "id": "example-001",
      "kind": "ghost",
      "map": "어센트",
      "side": "atk",
      "site": "A",
      "agent": "페이드",
      "title": "라인업 이름",
      "note": "던지는 위치, 조준점, 활용법을 작성하세요.",
      "thumbnail": "media/example-001.jpg",
      "video": "media/example-001.mp4",
      "url": "https://www.youtube.com/watch?v=..."
    }
  ]
}
```

- `kind`: `ghost`(각귀체), `molly`(각불), `recon`(각리콘)
- `side`: `atk`(공격), `def`(수비)
- `site`: `A`, `B`, `C`, `미드` (상황에 맞게)
- `video`: 직접 재생할 영상 경로(예: `media/filename.mp4`)
- `url`: 외부 영상 링크(예: YouTube). 직접 재생하는 영상 파일은 아닙니다.
- `thumbnail`: 선택 사항. 목록 카드의 미리보기 이미지입니다.
- `id`: 라인업마다 고유한 문자열을 권장합니다.
- `note`, `video`, `url`, `thumbnail`는 상황에 맞게 비워 두어도 됩니다.
- 실제 영상이나 이미지는 `media/` 폴더에 업로드하세요.

기존 대전 기록은 메인 브랜치에서 삭제되었습니다. 이전 웹사이트 및 데이터는 `backup/v1c-stats-2026-11-02` 브랜치에서 확인할 수 있습니다. 단, Git 기록 자체는 남습니다.

본 사이트는 비공식 팬 프로젝트이며 Riot Games와 관계가 없습니다.
