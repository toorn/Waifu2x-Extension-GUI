# 한국어 QM 적용 및 검증

2026-10-25: 제공받은 `v3.142.01 source code.zip` 내부의 Qt 번역 소스는 `SRC_v3.41.01-beta`입니다. **이 버전의 UI 문자열과 최신 릴리스의 UI가 동일하다고 확인된 것은 아닙니다.**

## 별도 배포된 한국어 패치 파일 사용

한국어 번역 패키지에는 `language_Korean.ts`, `language_Korean.qm`, 시험용 `language_English.qm`이 포함됩니다.

1. 프로그램을 종료합니다.
2. 프로그램 폴더에서 기존 `language_English.qm`을 `language_English.qm.bak`으로 백업합니다.
3. 시험용 `language_English.qm`을 프로그램 폴더로 복사합니다.
4. 프로그램을 실행하고 **English**를 선택한 뒤 필요하면 재시작합니다.
5. 작동하지 않으면 백업 파일을 복원합니다.

이것은 기존 언어 선택 항목을 활용한 **테스트 방법**이며, 새 Korean 메뉴를 추가하는 패치는 아닙니다. 현재 공개 소스에서는 언어 파일명을 코드에서 선택하므로, 새 Korean 메뉴는 별도의 소스 수정·빌드가 필요합니다.

## 번역 및 호환성 범위

- 첨부된 소스에 포함된 메시지: 626개
- 626개에 한국어 번역을 준비했고, XML 및 `%1`·`%2` 자리표시자를 점검했습니다.
- 생성된 QM 파일의 내부 구조 검사와 Qt 5.15 `QTranslator::load` 확인을 완료했습니다.
- **Windows 최신 v3.142.01 실행 프로그램에서의 적용·기능 테스트는 아직 실시되지 않았습니다.**
- 번역의 자연스러움과 긴 도움말의 문구는 실제 GUI에서 추가 검토가 필요합니다.

## Qt 번역 파일 빌드

Qt Linguist를 설치한 뒤:

```powershell
lrelease language_Korean.ts -qm language_Korean.qm
lrelease language_Korean.ts -qm language_English.qm
```

원본 영어 QM을 반드시 백업하고 교체하세요.

**주의:** 이 저장소의 기존 `SRC_v3.41.01-beta/.../language_Korean.ts`는 초기 작업본입니다. 별도로 제공한 완역 TS가 해당 파일보다 새 버전이며, 저장소 파일을 완역으로 덮어쓴 상태라고 오해하지 마세요.
