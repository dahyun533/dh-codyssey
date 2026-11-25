# [세미나 A] AI 기반 UI/UX 디자인 시안 제작 — PlayHub

여러 게임이 모인 게임 플랫폼 PlayHub의 데스크탑 웹(16:9) 시안.

## 사용한 도구 테스트
| 도구 | 쓴 곳 | 쓴 이유 |
|---|---|---|
| ChatGPT 이미지 생성 | 화면 이미지 생성 | Midjourney는 구독이 없어 변경. 대화로 앞 이미지를 레퍼런스로 이어 쓸 수 있음 |
| Python (Pillow) | 후가공 (아이템 칸 교체, 상단 메뉴 통일) | Figma 대신 사용. 픽셀 단위로 정확히 잘라 붙이고 세 화면 메뉴 위치를 같은 좌표로 맞추며 원본 해상도 유지 |
| Figma | 화면 배치, Hotspot·화면 전환 | 미션 권장 도구 |
| Claude (Claude Code) | 기획 질문, 프롬프트 작성, 후가공 코드, Figma 배치·Hotspot 연결 보조 | AI 협업 워크플로우 실습  |

## Figma 보기 링크
- 프로토타입(바로 클릭해 보기): https://www.figma.com/proto/x3suDwV8hS8B4xMWeB1wvH?node-id=1-8&starting-point-node-id=1-8&scaling=scale-down-width
- 디자인 파일(프레임·Hotspot 보기): https://www.figma.com/design/x3suDwV8hS8B4xMWeB1wvH
- 화면 흐름·Hotspot 캡처: [figma/화면흐름_Hotspot.png](figma/화면흐름_Hotspot.png)
- 프로토타입에서 상단 메뉴·로고·Play Now·View More·프로필을 누르면 화면 이동

## 화면
| 화면 | 최종본 | ChatGPT 원본 | 후가공 |
|---|---|---|---|
| 1. 홈 | [ui/화면1_홈.png](ui/화면1_홈.png) | [원본](ui/원본_ChatGPT/화면1_홈_원본.png) | 상단 메뉴 위치·활성 칸 통일 |
| 2. 게임 목록 | [ui/화면2_목록.png](ui/화면2_목록.png) | [원본](ui/원본_ChatGPT/화면2_목록_원본.png) | 상단 메뉴 위치·활성 칸 통일 |
| 3. 내 아바타 | [ui/화면3_아바타.png](ui/화면3_아바타.png) | [원본](ui/원본_ChatGPT/화면3_아바타_원본.png) | Hat 탭의 옷·신발 칸 → 모자로 교체, 상단 메뉴 위치·활성 칸 통일 |

- 후가공 수정사항: [후가공/수정사항.md](후가공/수정사항.md)
- 수정 전/후 비교: [아이템 칸](후가공/아바타_전후비교.png), [상단 메뉴](후가공/메뉴_전후비교.png)
- 깨진 글자: 세 장 모두 없음

## 화면 흐름
| 출발 화면 | 누르는 곳 | 도착 화면 |
|---|---|---|
| 1 홈 | 'Games' 메뉴 / 'Play Now' / 'View More' | 2 게임 목록 |
| 1 홈 | 'Avatar' 메뉴 / 프로필 | 3 내 아바타 |
| 2 게임 목록 | 'PlayHub' 로고 / 'Home' 메뉴 | 1 홈 |
| 2 게임 목록 | 'Avatar' 메뉴 / 프로필 | 3 내 아바타 |
| 3 내 아바타 | 'PlayHub' 로고 / 'Home' 메뉴 | 1 홈 |
| 3 내 아바타 | 'Games' 메뉴 | 2 게임 목록 |

- 흐름 시작점: 1 홈 / 클릭 영역(Hotspot) 12개 / 전환: Dissolve

## 문서
- [기획서](md/기획서.md)
- [작업로그](md/작업로그.md) — 프롬프트 1단계 초안 → 2단계 수정 → 3단계 최종, 바꾼 이유
- [코랩세션리포트](코랩세션리포트.md)
- 생성 결과 캡처: `대화 캡처/` (`v1_*` 초안 결과, `v2_*` 수정·최종 결과)
