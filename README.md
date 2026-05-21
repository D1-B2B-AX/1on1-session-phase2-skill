# 세션스킬 사용 가이드

`세션스킬`은 AX팀 1:1 세션에서 LD case를 빠르게 분류하기 위한 Claude Code 스킬입니다. Claude Code에서 `/세션스킬`을 실행하면 현재 단계, 추천 영역, 패턴, 실행 양식, 다음 액션을 짧게 정리해줍니다.

## 1. 스킬 다운로드

터미널에서 아래 명령어를 실행합니다.

```bash
git clone https://github.com/D1-B2B-AX/1on1-session-phase2-skill.git
cd 1on1-session-phase2-skill
```

GitHub 화면에서 직접 받을 수도 있습니다.

1. https://github.com/D1-B2B-AX/1on1-session-phase2-skill 접속
2. `Code` 버튼 클릭
3. `Download ZIP` 클릭
4. 압축 해제
5. 압축을 푼 폴더로 이동

## 2. Claude Code에서 열기

다운로드한 폴더 안에서 Claude Code를 실행합니다.

```bash
claude
```

이미 Claude Code를 열어둔 상태에서 스킬이 보이지 않으면 Claude Code를 한 번 다시 시작합니다.

## 3. 스킬 실행

Claude Code 입력창에 `/세션스킬`을 입력하고, 아래처럼 case 내용을 붙입니다.

```text
/세션스킬

업무 유형: 강의 만족도 조사 분석
현재 해결 방식: LD가 엑셀에서 직접 분류
시도한 도구·결과물: Claude 프롬프트 1차본
LD 발화 일부: 분류 기준이 매번 달라요
```

정상 작동하면 `추천 패턴 분류 결과`가 출력됩니다.

## 4. 입력할 때 포함하면 좋은 정보

- 업무 유형: 어떤 업무를 도와주는지
- 현재 해결 방식: 지금 LD가 어떻게 처리 중인지
- 시도한 도구·결과물: 프롬프트, 코드, 산출물, 검증 자료 등
- LD 발화 일부: 실제로 막힌 지점이나 고민 표현

모든 항목을 완벽하게 채울 필요는 없습니다. 정보가 부족하면 스킬이 추가 확인 질문을 냅니다.

## 5. 최신 버전으로 업데이트

터미널에서 스킬 폴더로 이동한 뒤 `git pull`을 실행합니다.

```bash
cd 1on1-session-phase2-skill
git pull
```

ZIP으로 받은 경우에는 GitHub에서 ZIP을 다시 받아 압축을 새로 풉니다.

## 6. 안 될 때 확인할 것

- Claude Code를 `1on1-session-phase2-skill` 폴더 안에서 실행했는지 확인
- 명령어를 `/세션스킬`로 입력했는지 확인
- `git pull`로 최신 버전을 받았는지 확인
- 그래도 보이지 않으면 Claude Code를 재시작
