# VARIABLES

### main

- main method 는 Dart 프로그램의 Entry point 임
- main method 는 항상 존재 해야함

### semicolon

- dart 에서는 semicolon의 여부에 따라 의미가 달라지기에 자동으로 추가해주지 않음
- 수동으로 추가해주어야함

### 변수 선언

- 함수나 메소드 내부에 지역 변수를 선언할 때에는 var를 사용함
- class에서 변수나 property를 선언할 때에는 타입을 지정해줌(String)

### Dynamic Type

- 여러가지 타입을 가질 수 있음
- 변수의 타입을 사전에 특정할 수 없는 경우(json 등) 유용함

```markdown
void main() {
	var name; // dynamic name;으로도 선언 가능
	name = 'geon';
	name = 12;
	name = false;
}
```

### Null Variables

- dart에는 null safety 기능이 있어, null을 참조하면 에러가 발생함
- 그러나 아래와 같이 타입 뒤에 `?` 를 붙혀주면 해당 변수의 타입이 지정 타입 혹은 null 일 수도 있음을 명심함

```markdown
void main() {
	String? name; = 'geon'; 
	name = null;
	name?.isNotEmpty; 
	//name.isNotEmpty 를 그대로 사용하면, name이 null 일 수 있음으로 에러가 발생되지만, 
	//name 변수명 뒤에 ?를 추가함으로서 null 일 수 있음을 명시함	
}
```

### Final Variables

- 최초에 선언한 변수의 값이 수정되지 않기를 원할 때 사용

`final name = 'geon';`

### Late Variables

- 변수의 값을 나중에 부여할 수 있음

```markdown
void main() {
	late final name;
	name = 'geon';
}
```

### Const Variables

- dart에서 const는 compile-time constant임
- final과 마찬가지로 최초의 값을 수정할 수 없음
- 정적인 값을 기입할 때 사용하며, 동적인 값을 기입할 땐 final을 사용함
    - const는 compile 이전에 값을 인지해야하기 때문
