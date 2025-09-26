# Implement Monkey Console Application

요약
- C# 콘솔 애플리케이션을 추가해 모든 원숭이 목록 조회, 이름으로 특정 원숭이 상세 조회, 무작위 원숭이 선택 기능을 제공한다.

요구사항
- `Monkey` 모델 클래스(예: `Name`, `Location`, `Population` 등 속성 포함)를 사용한다.
- 콘솔 UI에서 ASCII 아트를 표시해 시각적 즐거움을 제공한다.
- 기능:
  - 전체 원숭이 목록 나열
  - 이름으로 원숭이 상세 조회(대/소문자 무시)
  - 무작위 원숭이 선택 및 출력
- 별도의 콘솔 프로젝트로 추가(권장 이름: `MyMonkeyApp`)

레이블(제안)
- enhancement
- good first issue

구현 아이디어
- Repository 패턴: `IMonkeyRepository` 인터페이스와 `InMemoryMonkeyRepository` 구현을 만들어 테스트와 확장성을 확보한다.
- `Monkey` 모델(속성: `Name`, `Location`, `Population`)과 static `MonkeyHelper` 또는 서비스 클래스로 데이터 관리.
- `Program.cs`에서 단순 메뉴 기반 루프(번호 입력)로 사용자 상호작용을 구현한다.
- ASCII 아트를 상단에 출력해 동작할 때마다 표시.
- 단위 테스트: `GetMonkeys()`, `GetMonkeyByName()`, `GetRandomMonkey()`의 해피패스 및 경계 케이스 테스트 추가.

체크리스트
- [ ] 새 콘솔 프로젝트 추가(`MyMonkeyApp`)
- [ ] `Monkey` 모델 구현
- [ ] `IMonkeyRepository` 및 `InMemoryMonkeyRepository` 구현
- [ ] UI 메뉴 및 ASCII 아트 추가
- [ ] 기능: 목록, 상세조회(이름), 랜덤 선택 구현
- [ ] 기본 단위 테스트 추가(NUnit 또는 xUnit)
- [ ] README에 사용법 및 실행 예시 추가

추가 노트
- 확장: 이후 파일/DB 기반 저장소로 교체 가능하도록 설계하세요.
- 에러 처리: 이름 조회 실패 시 친절한 메시지 출력, 빈 목록 상태 처리.

간단한 ASCII 예시
```
  @..@
 (----)
( >__< )
 ^^ ~~
```

---

참고: 이 저장소의 GitHub Issues가 현재 비활성화되어 있거나 이 에이전트의 권한으로는 원격 이슈를 직접 생성할 수 없습니다. 이 파일은 로컬/원격 저장소에 작업 항목을 기록하기 위한 대체 방식입니다. 저장소에서 Issues를 활성화하면 이 내용을 기반으로 GitHub 이슈를 생성하면 됩니다.
