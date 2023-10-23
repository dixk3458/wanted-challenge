`
## [챌린지 과제](https://gist.github.com/pocojang/e9ccaa847d7f23bc43c25f273400b585#%EC%B1%8C%EB%A6%B0%EC%A7%80-%EA%B3%BC%EC%A0%9C)

### [Q1. 내가 생각하는 클린 코드란?](https://gist.github.com/pocojang/e9ccaa847d7f23bc43c25f273400b585#q1-%EB%82%B4%EA%B0%80-%EC%83%9D%EA%B0%81%ED%95%98%EB%8A%94-%ED%81%B4%EB%A6%B0-%EC%BD%94%EB%93%9C%EB%9E%80)

코드를 작성한 사람 이외에 다른 사람이 코드를 봤을 때 읽기 편하고 이해가 되는 코드가 클린 코드라고 생각합니다. 방대한 양의 프로그램을 협업을 통해 만들어내는 개발자들은 서로가 작성한 코드를 이해해야 성공적인 성과물을 만들어낼수있기 때문입니다.

### [Q2. 내가 생각하는 (프론트엔드에서의) 클린 코드란?](https://gist.github.com/pocojang/e9ccaa847d7f23bc43c25f273400b585#q2-%EB%82%B4%EA%B0%80-%EC%83%9D%EA%B0%81%ED%95%98%EB%8A%94-%ED%94%84%EB%A1%A0%ED%8A%B8%EC%97%94%EB%93%9C%EC%97%90%EC%84%9C%EC%9D%98-%ED%81%B4%EB%A6%B0-%EC%BD%94%EB%93%9C%EB%9E%80)

다른 개발자, 기획자, 디자이너 등의 사람들이 쉽게 읽을 수 있는 코드입니다. 프론트엔드 개발자는 프론트엔드 개발자끼리 일하는것이 아닙니다. 백엔드 개발자, 기획자, 디자이너 등 다른 업무를 하는 사람들과 함께 의견을 나누고 공통된 목표를 향해 업무를 진행하기때문에 프론트엔드 개발 언어에 익숙하지 않은 사람이 코드를 봐도 의미를 이해할수있도록 작성해야합니다. 

그러한 코드를 작성하기 위해서 저는 다음과 같은 노력을 합니다.

1. 변수,함수의 이름을 명확하게 작성하여 해당 값을 파악하는데 도움을 줌
2. 클래스나 모듈을 작성할때 하나의 책임만 가지도록 작성한다.

### [Q3. 내가 클린코드보다 중요하게 생각하는 것은?](https://gist.github.com/pocojang/e9ccaa847d7f23bc43c25f273400b585#q3-%EB%82%B4%EA%B0%80-%ED%81%B4%EB%A6%B0%EC%BD%94%EB%93%9C%EB%B3%B4%EB%8B%A4-%EC%A4%91%EC%9A%94%ED%95%98%EA%B2%8C-%EC%83%9D%EA%B0%81%ED%95%98%EB%8A%94-%EA%B2%83%EC%9D%80)

웹 어플리케이션 성능을 향상시키기위해 코드를 작성할때 많은 시간을 보냅니다. 웹 어플리케이션은 사용자에게 제공되는 서비스입니다. 사용자가 빠르고 부드러운 서비스를 이용할수있도록 , 성능을 최적화시키는 코드를 작성해야합니다. 

### [Q4. 다음 중 선호하는 방식과 그 이유는?](https://gist.github.com/pocojang/e9ccaa847d7f23bc43c25f273400b585#q4-%EB%8B%A4%EC%9D%8C-%EC%A4%91-%EC%84%A0%ED%98%B8%ED%95%98%EB%8A%94-%EB%B0%A9%EC%8B%9D%EA%B3%BC-%EA%B7%B8-%EC%9D%B4%EC%9C%A0%EB%8A%94)

### [1.](https://gist.github.com/pocojang/e9ccaa847d7f23bc43c25f273400b585#1)

`Tab` vs `Space`

Tab ⇒ 한 번의 타이핑으로 여러번의 space의 효과를 줄수있어,  코드를 작성하는데 번거로움을 해결해준다.

### [2.](https://gist.github.com/pocojang/e9ccaa847d7f23bc43c25f273400b585#2)

`세미콜론 O` vs `세미콜론 X`

세미콜론 O ⇒ 실행 가능한 최소의 코드 조각을 의미하는 문의 끝을 구분해주어 가독성을 높이기때문에 세미 콜론을 사용한다.

### [3.](https://gist.github.com/pocojang/e9ccaa847d7f23bc43c25f273400b585#3)

`count++;` vs `count += 1;` vs `count = count + 1;`

count++ ⇒ 1번과 같은 이유로 편리하다는 이유로 사용한다.

### [4.](https://gist.github.com/pocojang/e9ccaa847d7f23bc43c25f273400b585#4)

`if (isLogin) {}` vs `if (isLogin === true) {}`

if(isLogin){} ⇒ boolean값으로 표현될수있는문에서는 보통 이렇게 작성하여 편리하게 사용하고있다.

### [5.](https://gist.github.com/pocojang/e9ccaa847d7f23bc43c25f273400b585#5)

`isLogin && <HelloWanted />` vs `isLogin ? <HelloWanted /> : <></>` vs `isLogin ? <HelloWanted /> : null` vs `isLogin ? <HelloWanted /> : undfined`

isLogin && <HelloWanted/> ⇒ 보통 React에서 조건에 따라 컴포넌트를 렌더링하기위해 위의 방식을 사용한다. 하지만 이것도 실행되는것의 수에 따라 달라지는것같다. 다양한 실행코드가 있다면 삼항연산자를 이용하기도 한다. 하지만 위의 경우는 HelloWanted 혹은 보여주지 않는것이기때문에 AND연산자를 이용한다.
`
