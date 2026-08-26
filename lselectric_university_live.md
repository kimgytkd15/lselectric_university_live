# lselectric_university_live

> 경로: `C:\ws_vscode\lselectric_university_live`
> Git: https://github.com/kimgytkd15/lselectric_university_live.git (main) — **public**
> 분류: 배포 전용 저장소 (현재 사실상 비어 있음)

## 1. 어떤 프로젝트인가

`lselectric_university`(private, Docusaurus 문서 사이트)의 **공개 배포 대상 저장소**로 만들어 둔 껍데기다.
소스는 private 저장소에, 빌드 산출물만 이 public 저장소로 나가는 구조다.
로컬 폴더에는 `.git`과 빈 `README.md`만 있고, 커밋은 `live init` 하나뿐이다.

즉 **소스는 여기에 없다.** 실제 작업은 `C:\ws_vscode\lselectric_university`에서 한다.

## 2. 현재 상태

```
lselectric_university_live/
├─ .git/            origin: github.com/kimgytkd15/lselectric_university_live
└─ README.md        (빈 파일)
```

- 브랜치: `main`
- 마지막 커밋: `9380b87 live init` (2026-05-22)

## 3. 실행 방법

실행할 것이 없다. 빌드 산출물을 올리는 용도의 저장소다.

배포는 원본 프로젝트에서 수행한다:

```powershell
cd C:\ws_vscode\lselectric_university
npm run build
$env:GIT_USER="<GitHub 사용자명>"; npm run deploy
```

또는 `build/` 산출물을 이 저장소에 복사해 커밋·푸시하는 방식으로 운용할 수도 있다.

## 4. ⚠️ 공개 저장소라는 점

이 저장소는 **public**이다. `build/` 산출물을 복사해 올릴 때
private 쪽의 `README.md`(배포 토큰이 평문으로 들어 있음)나 `.env` 류가 함께 딸려가지 않도록 주의할 것.

## 5. 정리 제안

- 이 저장소를 계속 쓸 계획이면 `docusaurus.config.ts`의 `url`/`baseUrl`/`deploymentBranch` 설정과
  실제 배포 방식(수동 복사 vs `npm run deploy`)을 문서화해 둘 것.
- 쓰지 않을 계획이면 로컬 폴더를 정리해도 무방하다(원격 저장소는 그대로 남는다).
