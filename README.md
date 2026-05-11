# 🛒 Shopping List App

바닐라 JS로 만든 간단한 쇼핑 리스트 웹앱입니다. localStorage에 데이터를 영속화하며, Playwright MCP로 자동화 테스트를 수행했습니다.

## 데모

별도의 빌드 없이 `index.html`을 브라우저에서 열거나 정적 서버에서 호스팅하면 동작합니다.

```bash
python3 -m http.server 8765
# 브라우저에서 http://localhost:8765/index.html 접속
```

## 기능

- 항목 추가 (버튼 클릭 / Enter 키)
- 체크박스 토글 (완료 시 취소선)
- 개별 항목 삭제 (× 버튼)
- 전체 삭제 (confirm 다이얼로그)
- `localStorage` 자동 저장/복원
- 카운터(`N개 항목 · N개 완료`) 실시간 동기화
- 공백 입력 방어

## 파일 구성

```
.
├── index.html        # 앱 본체 (HTML + CSS + JS 단일 파일)
├── TEST_REPORT.md    # Playwright 자동화 테스트 보고서
└── screenshots/      # 테스트 단계별 스크린샷
```

## 테스트 결과

8개 시나리오 전부 통과 ✅. 상세 내용은 [`TEST_REPORT.md`](TEST_REPORT.md) 참고.

## 기술 스택

- HTML / CSS / Vanilla JavaScript (외부 의존성 없음)
- Playwright MCP (자동화 테스트)
