# KC Skills

KC Skills는 한국어를 사용하는 현업 담당자가 개발 용어와 Git 명령을 몰라도 자연어로 제품 정의, 구현, 데이터 연결, 문제 해결, 검증, 복구와 배포를 진행하도록 돕는 Agent Skills 모음입니다.

## 설치

Claude Code 프로젝트에 전체 Skill을 설치합니다.

```bash
npx skills add taehalim/kc-skills --skill '*' --agent claude-code --yes
```

Codex 프로젝트에 설치하려면 대상 에이전트만 바꿉니다.

```bash
npx skills add taehalim/kc-skills --skill '*' --agent codex --yes
```

대화형으로 설치할 Skill과 에이전트를 직접 고를 수도 있습니다.

```bash
npx skills add taehalim/kc-skills
```

설치 결과는 다음 명령으로 확인합니다.

```bash
npx skills list
```

## 포함된 Skills

| Skill | 하는 일 |
| --- | --- |
| `kc-init` | 빈 폴더에 Git, 프로젝트 지침과 최초 저장점을 준비합니다. |
| `kc-define` | 아이디어와 자료를 구현 가능한 제품 정의 또는 PRD로 구체화합니다. |
| `kc-build` | 확인된 요구사항을 작동하는 기능으로 구현합니다. |
| `kc-generate-sample-data` | 실제 개인정보 없이 시연·검증용 가상 데이터를 만듭니다. |
| `kc-connect-data` | 핵심 사용자 흐름에 필요한 영구 데이터 읽기·쓰기를 연결합니다. |
| `kc-fix` | 기대와 다른 동작을 재현하고 원인을 수정합니다. |
| `kc-recover` | Git 용어를 몰라도 이전 정상 상태로 되돌리거나 다시 적용합니다. |
| `kc-verify` | 요구사항과 핵심 사용자 흐름이 실제로 작동하는지 검증합니다. |
| `kc-publish` | 명시적으로 요청받은 서비스를 배포하고 공개 URL을 확인합니다. |

Skill 이름을 외울 필요는 없습니다. 각 `SKILL.md`의 `description`을 기반으로 에이전트가 자연어 요청에 맞는 Skill을 선택합니다.

## 지원 형식

- Agent Skills 표준의 `SKILL.md`, `references/`, `assets/` 구조를 사용합니다.
- Claude Code나 Codex 전용 UI 메타데이터를 Skill 본체에 포함하지 않습니다.
- Skill은 전역이 아니라 현재 프로젝트에 설치하는 방식을 권장합니다.

