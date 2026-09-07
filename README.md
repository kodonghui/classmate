# Corthex Classmate — Windows 다운로드

수업·강의 영상을 보면서, 옆 대화창에서 모르는 부분을 바로 질문하는 Chrome 사이드패널 튜터입니다.
이곳은 **설치 파일과 사용 안내만 배포**합니다. 개발 소스나 배포자의 수업 기록·인증 정보는 포함하지 않습니다.

## 다운로드

**Windows x64 · 0.0.6-beta2 (안내 보강판)**

- **[Windows 설치 ZIP 다운로드](https://github.com/kodonghui/corthex-classmate-downloads/releases/download/v0.0.6-beta2/Corthex-Classmate-0.0.6-beta2-windows-x64.zip)**
- [한국어 안내서 다운로드](https://github.com/kodonghui/corthex-classmate-downloads/releases/download/v0.0.6-beta2/Guide.html) — ZIP 안에도 있습니다. 다운로드한 HTML을 브라우저로 열어 주세요.
- [SHA-256 체크섬](https://github.com/kodonghui/corthex-classmate-downloads/releases/download/v0.0.6-beta2/Corthex-Classmate-0.0.6-beta2-windows-x64.zip.sha256)
- [릴리스 설명](https://github.com/kodonghui/corthex-classmate-downloads/releases/tag/v0.0.6-beta2)

GitHub가 자동 제공하는 **Source code (zip/tar.gz)**는 설치 파일이 아닙니다.
위의 **Corthex-Classmate-…-windows-x64.zip**을 받으세요. Git clone이나 소스 빌드는 필요 없습니다.

## 처음 설치하기

1. Chrome, Windows용 **Claude Code CLI + 본인 로그인**, Tiro를 준비합니다.
2. 설치 ZIP을 전부 압축 해제하고 `Guide.html`을 읽은 뒤 **Install.cmd**를 더블클릭합니다.
3. Chrome을 완전히 종료했다가 다시 열고 `chrome://extensions` → 개발자 모드 → **압축해제된 확장 프로그램을 로드**를 선택합니다.
4. 설치 완료 메시지에 표시된 `app\extension` 폴더를 선택합니다.
5. 본인 Tiro 공유 전사 페이지를 같은 Chrome 프로필에서 열고, 강의 영상 탭에서 Classmate 아이콘을 눌러 질문합니다.

Classmate 자체를 설치하는 데 개발용 Git·Node·Rust는 필요하지 않습니다. Claude Code 자체의 요구사항은 [공식 설치 안내](https://code.claude.com/docs/en/setup)를 따르세요.

## AI는 무엇을 보나요?

| 자료 | 전달 범위 |
|---|---|
| 내 질문 | 선택한 단어·문장 또는 직접 적은 질문 |
| 선생님 말씀 | Tiro 전사의 질문 대목 주변, 약 2,000자 예산. 중심 문단은 길어도 유지 |
| 화면 | 질문 순간 선택한 강의 탭 캡처를 시도. 성공한 이미지 파일을 참고하도록 전달 |
| 이전 문답 | 같은 교시의 완료된 최근 최대 6쌍, 합계 약 12,000자 |
| 편집기 코드 | 실제 연결로 받은 발췌가 있을 때만 선택적으로 포함 |

이 자료를 **내 PC의 로컬 도우미 → 내 PC의 Claude Code → Claude AI 서비스**로 전달하고, 설명을 사이드패널에 보여줍니다. 로컬 AI 모델만으로 처리하는 서비스는 아닙니다.

- 앞 질문에서 이어 물으면 원래 전사 맥락을 유지합니다. 화면은 현재 것이어서 예전 대목과 다를 수 있습니다.
- ‘뒤쪽 말씀’은 질문 시 이미 도착한 전사 중에서 고릅니다. 미래 발언을 기다리거나 하루 영상 전체를 계속 시청하는 방식은 아닙니다.
- 캡처에 실패하면 이전 프레임이 남거나 화면 없이 답할 수 있습니다. 이미지 경로 전달만으로 매번 이미지 읽기 성공이 보장되지는 않습니다.
- 전사 오류와 AI의 일반 지식 보충이 답에 영향을 줄 수 있습니다. 강사가 직접 한 말과 AI의 해설을 구분하세요.

## Claude는 자동으로 연결되나요?

**Classmate를 설치하는 그 PC, 같은 Windows 사용자 계정의 Claude Code 실행 파일을 설치기가 자동 탐색합니다.**
일반적인 네이티브 설치와 최신 npm 설치 내부의 `claude.exe`를 지원합니다. 경로를 찾으면 로컬 연결을 등록합니다.

다음은 별개입니다.

- **본인 로그인은 직접 해야 합니다.** 설치기가 토큰을 복사하거나 로그인하지 않습니다.
- Claude 웹/데스크톱 앱만 설치·로그인한 것은 Claude Code CLI 준비가 아닙니다.
- WSL에만 설치한 경우나 다른 물리적 PC에만 있는 Claude는 자동 연결하지 않습니다.
- 비표준 설치 경로, 오래된 CLI, 사용 한도, 인터넷 문제로 실패할 수 있습니다.
- `Diagnose.cmd`는 파일·경로·등록을 확인할 뿐 로그인이나 AI 답변 성공을 보장하지 않습니다.

## 현재 한계와 개인정보

- **Claude Code만 지원**합니다. Codex 연결은 아직 활성화되어 있지 않습니다.
- 수업·수험·회의 프로필이 있지만 전문 분야의 최신 법령·세법·회계 기준 정확성이나 매 질문의 웹 검색을 보장하지 않습니다.
- 각자의 Claude·Tiro 계정 및 요금제 한도가 적용됩니다. API 인증 환경은 API 비용이 발생할 수 있으며 무료·무제한 서비스가 아닙니다.
- **로컬 보관 / 선택한 AI 제공자로 전송될 수 있음 / Corthex 서버 기본 전송 없음.** 자료 사용은 강사·참가자의 허용 범위와 서비스 정책을 지켜 주세요.
- 같은 Windows 계정은 로컬 공부 저장소를 공유할 수 있습니다. 여러 사람은 Windows 계정을 분리하세요.
- **서명되지 않은 베타**입니다. 체크섬은 무결성 확인용이며 코드 서명을 대신하지 않습니다. 백신·조직 보안 정책을 끄지 마세요.
- 기존 설치를 덮어쓰지 않습니다. 자동 업데이트·마이그레이션은 미지원입니다. `Disconnect.cmd`는 연결을 해제하지만 프로그램·공부 기록을 삭제하지 않습니다.
- beta1과 beta2의 앱 파일은 같습니다. **beta1 사용자는 새 안내만 읽고 재설치하지 마세요.**

검증 범위: 개발 PC의 격리 설치·파일 무결성·로컬 도우미 통신, 안내서 390px/1100px 레이아웃. 별도 새 PC의 계정 로그인부터 실제 수업 답변까지는 첫 설치에서 확인해야 합니다.
오류를 공유할 때는 화면 속 수업 내용·계정 정보·Tiro 비공개 링크를 가려 주세요.

라이브러리와 폰트의 라이선스 고지는 ZIP의 `licenses/`에 포함되어 있습니다. 이 배포 저장소는 비공개 제품 소스 전체를 공개 오픈소스로 전환하거나 별도 라이선스를 부여하지 않습니다.
