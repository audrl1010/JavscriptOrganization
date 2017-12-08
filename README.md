# JavscriptOrganization
자바스크립트 ECMAScripts5, ECMAScripts6를 정리하는 저장소 입니다.

# 자료형(Data Type)

## 기본 자료형

### Number
```javascript
var number = 3; // Number
```

### String
```javascript
var name = 'name'; // String
```

### Boolean
```javascript
var check = true; // Boolean
```

## 복합 자료형

### 객체(Object)
```javascript
var object = { name: 'name', color: 'white' }; // Object
```

### 배열(Array)
```javascript
var names = ['a', 'b', 'c', 'd']; // Array Object
```

## 특수 자료형

### undefined
'값이 없음'을 나타낸다. 보통 변수가 초기화되어 있지 않은 경우, 존재하지 않는 객체 프로퍼티나 배열의 원소 값에 
접근하려고 할 때 얻는 변수의 값이다. 또한 반환 값이 없는 함수와 인자가 없는 함수 매개변수의 값에 의해 반환된다.
```javascript
var name; // undefined
```
### null
'아무 값도 갖지 않음'을 가리킬 때 사용된다.
```javascript
var name = null;
```

# 클래스

## 상속
```javascript
// ES5
function Parent(name) {
  this.name = name;
}

Parent.prototype.getName = function() {
  return this.name;
}

function Child(name) {
  Parent.call(this, name);
  this.age = 0;
}

Child.prototype = Object.create(Parent.prototype);
Child.prototype.constructor = Child;

Child.prototype.getAge = function() {
  return this.age;
}

let c = new Child("name");
```

```javascript
// ES6
class Parent {
  constructor(name) {
    this.name = name;
  }

  getName() {
    return this.name;
  }
}

class Child extends Parent {
  constructor(name) {
    super(name);
    this.age = 0;
  }

  getAge() {
    return this.age;
  }
}

let c = new Child("name");
```



# 모듈










