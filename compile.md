## 컴파일

dart 코드는 여러 CPU의 아키텍쳐에 맞게 컴파일 할 수 있음

### AOT & JIT

AOT(Ahead-of-Time)

- 최종 배포 시 사용되는 컴파일 방식
- 시스템에 맞게(기계어) 최적화된 바이너리를 생성하므로 컴파일에 많은 시간이 걸림

JIT(Just-In-Time)

- 개발 시 사용되는 컴파일 방식
- dart VM를 통해 코드의 결과를 화면상으로 바로 보여줌
- 가상 머신을 통해 동작하므로 조금 느림
- 디버깅 옵션 지원

### null safety

- 프로그래밍 언어에서 null을 참조 시 오류 발생
