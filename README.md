# Git-diff-wargame-lv2

# Lv.2 — Can you find a flag?

## 문제
`lv2.py`를 실행하면 플래그를 입력하라고 한다.
이번엔 커밋이 여러 개다.
git log로 수상한 커밋을 찾아서 플래그를 찾아라.

## 실행 방법
```bash
python lv2.py
```

## 풀이 흐름
1. 커밋 히스토리 확인
2. 수상한 커밋 메시지 찾기
3. git diff로 해당 커밋 변경사항 확인
4. 복원된 파일 실행 후 플래그 입력

## 명령어 설명
- `git log --oneline` : 커밋 히스토리를 한 줄로 출력
- `git diff <커밋1 해시> <커밋2 해시>` : 두 커밋 사이의 변경사항 출력. `-`로 시작하는 줄은 삭제된 줄, `+`로 시작하는 줄은 추가된 줄

## 주의사항 (PowerShell 환경)
PowerShell에서는 `>` 대신 아래 명령어를 사용해야 한다.
```powershell
git diff <커밋1 해시> <커밋2 해시> | Out-File -FilePath fix.patch -Encoding utf8
```