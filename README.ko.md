# Same Page

[English](README.md) | [한국어](README.ko.md)

**이해를 맞추고, 계획을 합의하고, 함께 실행합니다.**

Same Page는 작성자와 AI가 업무 목적을 확인하고, 계획과 업무별 준수사항을 합의한 뒤 실행·검증하도록 돕는 Codex 스킬 플러그인입니다.

**자료 검토 → 중요한 질문 → 이해 확인 → 계획 합의 → 준수사항 확정 → 실행 → 검증**

대화 중 새로운 의견이 합의된 계획을 바꾸면 기존 계획과 차이 및 영향을 설명하고 계획 반영 여부를 확인합니다. 구체적으로 수정하라고 지시한 내용은 같은 승인을 다시 묻지 않고 반영합니다.

## 저장소 구성

- `.agents/plugins/marketplace.json`: 마켓플레이스 항목
- `plugins/same-page/.codex-plugin/plugin.json`: 플러그인 등록 정보
- `plugins/same-page/skills/same-page/SKILL.md`: 스킬 진입점
- `plugins/same-page/skills/same-page/references/workflow.md`: 전체 작업 절차와 업무 문서 양식
- `GLOBAL_INSTRUCTIONS.md`: 절차를 넓게 적용할 때 사용할 선택 지침
- `VALIDATION.md`: 완료한 검사와 실제 환경에서 추가로 확인할 항목

## 설치

플러그인을 지원하는 Codex 워크스페이스에서 다음 저장소를 마켓플레이스로 가져옵니다.

- Source: `https://github.com/kaa9900-ops/same-page`
- Path: 마켓플레이스 파일이 저장소 루트에 있으므로 비워 둡니다.

그 다음 해당 마켓플레이스에서 **Same Page**를 설치합니다. 마켓플레이스 가져오기, 플러그인 설치, 모든 대화에서의 자동 적용은 서로 다른 단계이며 워크스페이스 관리자 권한이 필요할 수 있습니다.

공식 안내: [플러그인 제작](https://learn.chatgpt.com/docs/build-plugins), [플러그인 관리](https://learn.chatgpt.com/docs/enterprise/plugin-management).

## 사용

새 대화에서 Same Page 플러그인 또는 스킬을 선택한 뒤 다음처럼 요청합니다.

> Same Page를 적용해. 첨부한 자료를 검토하고 이해가 필요한 내용을 질문해. 이해 내용을 확인받은 뒤 계획을 세워줘.

작업 중에는 다음과 같이 요청할 수 있습니다.

> 방금 이야기한 내용을 기존 계획과 비교해줘.

> 제안한 변경을 계획서와 준수사항에 반영해.

> 현재 계획서와 준수사항을 읽고 실제 파일을 확인한 뒤 다음 작업부터 이어서 진행해.

이 플러그인은 지침과 Markdown 문서 양식만 사용합니다. 별도 서버, API 키 또는 외부 서비스 연동은 필요하지 않습니다. 업무별 계획서와 준수사항은 플러그인 설치 폴더가 아니라 실제 작업 위치에 생성합니다.

## 넓게 적용하기

스킬을 설치하는 것만으로 모든 대화에 자동 적용되지는 않습니다. 기존 설정을 덮어쓰지 말고 `GLOBAL_INSTRUCTIONS.md`의 관련 문구를 전역 지침에 병합한 뒤 새 대화에서 동작을 확인합니다.

## 버전과 업데이트

현재 릴리스는 `v0.1.0`입니다. 업데이트할 때는 마켓플레이스 소스를 동기화하거나 다시 가져오고, 새 버전의 플러그인을 설치한 뒤 새 대화에서 확인합니다. 배포 파일은 [Releases 페이지](https://github.com/kaa9900-ops/same-page/releases)에서 받을 수 있습니다.

## 라이선스

Same Page는 [MIT License](LICENSE)로 배포됩니다.
