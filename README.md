# MABC_AGENT

**MABC 2026 (Making AI Beneficial Challenge)** 출품 스킬 저장소.

Timely AI 스킬 스토어에 올릴 **이력서 × 채용공고 역량 매칭 스킬 3종**입니다.

## 스킬 3종

| 스킬 | 푸는 문제 | 사용 시점 |
|---|---|---|
| [이력서 역량 진단기](skills/resume-skill-extractor/SKILL.md) | 내 경력이 문서에서 **증명되고 있는가** | 이력서를 고칠 때 |
| [채용공고 해부기](skills/jd-skill-extractor/SKILL.md) | 이 공고가 **실제로 원하는 게 뭔가** | 공고를 처음 볼 때 |
| [지원 판단 리포트](skills/skill-matcher/SKILL.md) ⭐ | 이 공고에 **지원할 가치가 있는가** | 지원 버튼 누르기 전 |
| [지원동기 인터뷰어](skills/cover-letter-interviewer/SKILL.md) | 쓸 이야기가 **떠오르지 않는다** | 자소서 백지 앞에서 |

## 자소서 3부작 (경력자용) — 결과지로 이어지는 세트

| 스킬 | 푸는 문제 | 입력 → 출력 |
|---|---|---|
| [자소서 소재 은행 인터뷰](skills/career-material-bank/SKILL.md) ⭐ | 소재는 한 번만 캐면 되는데 **매번 처음부터 캔다** | 30~40분 인터뷰 → 결과지 |
| [경력기술서 작성기](skills/career-history-writer/SKILL.md) | 경력기술서가 **업무 나열**이 된다 | 결과지 + 공고 → 경력기술서 |
| [자소서 작성기](skills/cover-letter-writer/SKILL.md) | 문항이 묻는 것에 **답하지 않는다** | 결과지 + 문항 → 문항별 답안 |

세 스킬은 인터뷰 결과지를 매개로 이어집니다. 결과지의 `[대표 성과 한눈에]`·`[경력 연혁]`을
경력기술서가, 에피소드 A~F와 강도 판정을 자소서 작성기가 그대로 참조합니다.
각 스킬은 결과지 없이도 단독 동작합니다.

앞의 세 스킬은 **문서의 왜곡 방향이 서로 다릅니다** — 이력서는 과장되고(근거 검증으로 보정),
공고는 축약되며(숨은 요구 복원으로 보정), 매칭은 양쪽을 동시에 보정합니다.
네 번째는 성격이 다릅니다 — **분석이 아니라 인터뷰**이고, 입력이 문서가 아니라 **대화**입니다.

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
| [docs/00-competition-brief.md](docs/00-competition-brief.md) | 공식 규정·심사 배점·제출 절차 (확정본) |
| [docs/01-idea-design.md](docs/01-idea-design.md) | 아이디어 설계 근거 |
| [docs/02-ncs-decision.md](docs/02-ncs-decision.md) | NCS 활용 방식 결정 |
| [docs/03-scoring-strategy.md](docs/03-scoring-strategy.md) | 배점표 → SKILL.md 작성 전략 |
| [docs/04-submission-text.md](docs/04-submission-text.md) | 구글 폼용 스킬명·요약·상세설명 |
| [docs/05-timely-handoff.md](docs/05-timely-handoff.md) | 타임리 이관 및 제출 절차 |
| [docs/06-timely-brief.md](docs/06-timely-brief.md) | 타임리 첫 대화용 간단 명세 |
| [samples/TEST-PLAN.md](samples/TEST-PLAN.md) | 테스트 케이스 29종 (정상 + 예외 + 재현성) |

## 테스트 샘플

전부 가상 인물·가상 기업입니다. 실제 이력서·공고는 개인정보와 저작권 문제로 쓰지 않습니다.

| 이력서 | 의도 | 채용공고 | 의도 |
|---|---|---|---|
| [R1 데이터엔지니어](samples/resumes/R1-데이터엔지니어-3년.md) | 근거 충실 | [J1 직함 불일치](samples/jobs/J1-직함불일치-데이터.md) | 진짜 직무 판정 |
| [R2 신입](samples/resumes/R2-신입-무경력.md) | 무경력 예외 | [J2 담당업무만](samples/jobs/J2-담당업무만-있음.md) | 자격요건 부재 |
| [R3 과장형](samples/resumes/R3-과장형-마케터.md) | 증명 실패 탐지 | [J3 마케터](samples/jobs/J3-마케터.md) | 근거 없는 충족 방지 |

## 진행 상황

- [x] 대회 정보 조사
- [x] 아이디어 확정
- [x] 공식 규정 및 심사 배점표 반영
- [x] 스킬 7종 작성 (배점표 대응)
- [x] 테스트 샘플 및 테스트 계획 작성
- [x] 구글 폼용 텍스트 작성
- [ ] **타임리 편집창에서 스킬 제작** (제5조 1항 — 타 서비스 제작 시 실격)
- [ ] 새 대화창 + 처음 보는 입력으로 동작 테스트 → 프롬프트 조정
- [ ] 스토어 업로드 (태그 `mabc-final`) + 구글 폼 제출

> 🚨 이 저장소의 `SKILL.md`는 **원고**입니다. 로컬에서 zip으로 압축해 제출하면 실격입니다.
> 반드시 타임리 편집창에 옮겨 제작·테스트하고 **[내려받기]한 `skill.zip`** 을 제출하세요.
