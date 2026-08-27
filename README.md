# MABC_AGENT

**MABC 2026 (Making AI Beneficial Challenge)** 출품 스킬 저장소.

Timely AI 스킬 스토어에 올릴 **이력서 × 채용공고 역량 매칭 스킬 3종**입니다.

## 스킬 3종

| 스킬 | 입력 | 출력 |
|---|---|---|
| [이력서 역량 추출기](skills/resume-skill-extractor/SKILL.md) | 이력서 | 역량 프로필 + 공백 진단 |
| [채용공고 요구역량 분해기](skills/jd-skill-extractor/SKILL.md) | 채용공고 | 필수/우대/숨은 요구사항 분해 |
| [역량 매칭 리포트](skills/skill-matcher/SKILL.md) ⭐ | 이력서 + 공고 | 적합도 점수 + 근거 + 보완 전략 |

세 스킬은 [공통 스킬 레코드 스키마](skills/_SCHEMA.md)를 공유합니다.
1·2번의 JSON 출력을 3번에 그대로 넣을 수 있고, 3번은 **원문만으로도 단독 동작**합니다.

## 설계 원칙

- **모든 판정에 원문 인용 근거를 붙인다** — 환각 방지, 사용자 신뢰
- **이력서는 과장, 공고는 축약** — 서로 다른 왜곡을 각각 보정
- **점수 계산 과정을 공개한다** — 근거 없는 숫자는 신뢰할 수 없다
- **없는 경력을 만들지 않는다** — 표현을 다듬을 뿐 창작하지 않는다

## 문서

| 파일 | 내용 |
|---|---|
| [docs/00-competition-brief.md](docs/00-competition-brief.md) | 대회 규정·일정 정리 |
| [docs/01-idea-design.md](docs/01-idea-design.md) | 아이디어 설계 근거 |

## 진행 상황

- [x] 대회 정보 조사
- [x] 아이디어 확정
- [x] 스킬 3종 초안 작성
- [ ] Timely AI 스킬 스토어 형식 확인 및 변환
- [ ] 실제 이력서/공고 샘플로 동작 테스트
- [ ] 스토어 업로드
