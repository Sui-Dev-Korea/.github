# Translation Guidelines

## Purpose

영문으로 작성된 Sui 공식 문서를 한국어로 현지화한다.

## Priority

번역 시 아래 우선순위를 따른다.

1. 코드, 식별자, 경로, URL, import, 명령어, explicit heading ID, 구조용 front matter는 번역하지 않는다.
2. `temp-pr금지/KEEP_ORIGINALITY.md`에 있는 항목은 항상 원문을 유지한다.
3. `temp-pr금지/TRANSLATED_TERMINOLOGY.md`에 있는 항목은 한국어 번역을 우선 적용한다.
4. 두 용어장에 없는 항목은 문맥과 한국어 기술 문서 관용에 따라 판단한다.

## Scope

용어장 규칙은 기본적으로 본문 prose와 사용자에게 보이는 UI 텍스트에 적용한다. 코드의 인자 이름, 타입 이름, 함수명, 필드명, CLI 옵션, 파일명, 경로, URL, explicit heading ID에는 적용하지 않는다.

## Rules

### Core Rules

번역 시 다음 규칙을 반드시 지킨다.

- 종결 표현은 "~다 / ~이다"로 일관되게 유지한다.
- 전체 톤은 공식 문서 스타일에 맞춰 중립적이고, 간결하며, 정확하게 유지한다.
- 원문에 없는 설명, 해설, 각주는 임의로 추가하지 않는다.
- 원문에 있는 의미, 정보, 숫자, 코드, 함수명은 바꾸지 않는다.
- 콜론, 세미콜론, 괄호, 볼드체, 이탤릭체, 링크, 코드 등 원문 구조와 서식은 그대로 유지한다.
- 인라인 코드와 백틱 안의 내용은 번역하지 않는다.
- 문장 수는 가능한 한 원문과 비슷하게 유지하되, 한국어 가독성과 의미 명확성을 위해 필요한 경우 문장을 분리하거나 합칠 수 있다.
- 고유명사, 함수명, 변수명, 파일명, 명령어, 경로, URL은 원문을 유지한다.
- 단어장에 번역 단어가 있더라도 코드의 인자 이름, 타입 이름, 필드 이름, 키워드를 직접 가리키는 문맥이면 원문을 유지한다.
- 코드의 주석은 번역한다.
- 단어장은 항상 검토하고 업데이트한다. 새 항목을 등록할 때는 기존 항목과의 충돌, 합성어 여부, 문맥 의존 여부를 먼저 확인한다.

### Titles, Headings, and Link Text

- 문서 제목, 섹션 제목, 소제목, 본문 링크 텍스트는 사용자에게 보이는 텍스트이므로 번역한다.
- `temp-pr금지/DOCUMENT_STRUCTURE.md`에 포함된 문서 페이지는 제목을 번역 대상에 포함한다. 영문 제목을 기본값으로 남겨두지 않는다.
- 한 페이지의 제목을 번역할 때는 해당 페이지를 가리키는 링크 텍스트, 카드 제목, `sidebar_label`, `pagination_label`도 함께 찾아 같은 한국어 제목으로 맞춘다.
- 같은 대상 페이지를 가리키는 제목과 링크 텍스트는 문서마다 따로 번역하지 않고 하나의 canonical Korean title을 재사용한다.
- 본문 문장 안에서 링크를 사용할 때는 가능하면 링크 텍스트를 canonical title 그대로 두고, 조사나 설명은 링크 바깥에 둔다.
- 제목과 링크 텍스트에 포함된 고유명사, 제품명, 파일명, 명령어는 용어장과 일반 규칙에 따라 원문을 유지한다.
- 링크 URL, 상대 경로, 파일 경로, explicit fragment ID는 번역하지 않는다.
- 헤딩에 explicit ID (`{#...}`)가 있으면 그대로 유지한다.
- 헤딩을 번역한 결과 자동 생성 anchor가 바뀌어 내부 링크가 깨질 수 있으면 explicit ID를 사용하고, 해당 fragment 링크도 함께 맞춘다.

### Front Matter

- front matter의 구조는 원문 형식을 그대로 따른다.
- 사용자에게 보이는 front matter 값인 `title`, `sidebar_label`, `pagination_label`은 번역한다.
- `description`, `keywords`는 한국어 문맥에 맞게 번역할 수 있다.
- 같은 대상 페이지를 가리키는 `title`, `sidebar_label`, `pagination_label`은 가능한 한 같은 canonical Korean title을 사용한다.
- 라우팅 또는 참조에 영향을 주는 `id`, `slug`, `pagination_next`, `pagination_prev`, `sidebar_position`, `sidebar_key`, `displayed_sidebar`, `custom_edit_url` 등은 번역하지 않는다.
- front matter의 `description` 등 scalar 값에 백틱이나 YAML 파싱에 민감한 문자가 포함되면 값 전체를 큰따옴표(`"..."`)로 감싼다.

### Imports and Paths

- `import` 구문은 번역하지 않는다.
- 상대 경로 import가 i18n 구조에서 깨지는 경우, `@site` alias를 사용해 절대 경로로 수정한다.
- 내부 링크는 작업 중간 단계에서 억지로 맞추지 않는다. 완성된 한글 문서가 실제로 존재하는 경우에만 링크를 복구한다.

### Code Fences

- Markdown 예시 탭에서 코드 펜스(`` ``` ``)가 중첩되는 경우, 바깥쪽 코드 펜스는 백틱 4개(`` ```` ``)를 사용한다.

### Components

- Docusaurus 컴포넌트(`<Tabs>`, `<TabItem>`, `<ImportContent>`, `:::tip` 등)는 원문 그대로 유지한다.
- 컴포넌트 이름과 구조용 attribute(`value`, `id`, `key`, `className`, `groupId`, `src`, `to`, `href`, `path`, `slug`, `permalink`)는 번역하지 않는다.
- 사용자에게 보이는 attribute(`label`, `title`, `alt`, `summary`, `caption` 등)는 번역할 수 있다. 다만 해당 값이 식별자로도 쓰이는 문맥이면 원문을 유지한다.

### Terminology

아래 용어 기준을 따른다. 작업 중 새로 등록할 항목이 생기면 용어장에 추가한다.

- `temp-pr금지/TRANSLATED_TERMINOLOGY.md`
- `temp-pr금지/KEEP_ORIGINALITY.md`

용어장 관리 시 다음 원칙을 따른다.

- `KEEP_ORIGINALITY.md`에는 브랜드명, 파일명, 식별자, 표준명, 프로젝트에서 의도적으로 영어 유지하기로 합의한 용어만 넣는다.
- 문맥에 따라 번역 여부가 달라지는 일반 기술 용어는 `KEEP_ORIGINALITY.md`에 넣지 않는다.
- `TRANSLATED_TERMINOLOGY.md`에는 본문과 UI 텍스트에서 일관되게 번역해야 하는 항목만 넣는다.
- 여러 형태를 슬래시(`/`)로 묶지 않는다. 형태가 다르면 항목도 분리한다.
- 의미가 여러 개인 단어는 단일 강제 번역 대신 phrase-level 항목이나 예외 규칙으로 관리한다.

## Workflow

작업 폴더를 지정하면 다음 기준으로 작업한다.

- 먼저 `temp-pr금지/DOCUMENT_STRUCTURE.md`에서 현재 문서의 위치와 연결 문서를 확인한다.
- 기준 비교 대상은 현재 영문 원문 트리이다.
- 한글 문서는 영문과 직접 대응되는 경우에만 현재 문서 트리에 유지한다.
- 직접 대응 여부는 다음 순서로 판단한다.
  1. 동일 상대 경로
  2. 제목
  3. 본문 주제
  4. 내부 링크 구조
- 문서 제목을 번역할 때는 현재 문서의 상대 경로와 영문 제목을 모두 검색해, 같은 대상 페이지를 가리키는 링크 텍스트, 카드, `sidebar_label`, `pagination_label`을 함께 찾고 같은 한국어 제목으로 맞춘다.
- 영문 제목이 여러 문서에서 중복되면 제목 문자열만으로 매칭하지 말고 상대 경로와 `DOCUMENT_STRUCTURE.md`의 챕터 위치를 함께 확인한다.
- 영문 원문에 없거나 현재 구조에 직접 대응되지 않는 문서는 공개 문서 트리에서 제외하고 보류 보관소로 이동한다.
- 보류 문서는 `.pending-docs/current/...` 아래에 원래 상대 경로를 유지한 채 보관한다.
- 새 영문 문서를 작업할 때는 먼저 보류 보관소에 유사한 한글 번역이 있는지 확인한다.
- 유사한 문서가 있으면 이를 참고하거나 가져와서 작업하되, 원문에 없는 정보를 임의로 보완하지 않는다.
- 서로 다른 문서를 추측으로 합치지 않는다.
- 작업 중 용어장을 항상 확인하고, 등록이 필요한 항목을 발견하면 즉시 추가한다.

## Final Checks

- 위 조건을 모두 확인한 뒤, 조건을 위배하지 않는 범위에서만 문장이 자연스러운지 다시 검토하고 미세하게 조정한다.
- `DOCUMENT_STRUCTURE.md`에 포함된 문서의 `title`, `sidebar_label`, `pagination_label`, 카드 제목, 링크 텍스트가 같은 페이지에 대해 같은 한국어 제목을 사용하는지 확인한다.
- 제목, 링크 텍스트, fragment ID, 내부 링크가 현지화 후에도 일관되게 연결되는지 확인한다.
- 번역 완료 후 로컬에서 `docusaurus build`를 실행해 YAML 파싱 에러, MDX 컴파일 에러, import 경로 에러가 없는지 확인한다.
