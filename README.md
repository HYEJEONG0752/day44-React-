### **React의 핵심 개념 이해**

- **질문**: React에서 컴포넌트란 무엇이며, 어떤 두 가지 형태로 작성할 수 있나요?
- **답변**: UI를 구성하는 독립적인 단위로 재사용이 가능합니다. 컴포넌트는 클래스형 컴포넌트와 함수형 컴포넌트 두가지 형태로 작성할 수 있습니다.

### **JSX의 역할**

- **질문**: JSX란 무엇이며, React에서 어떤 역할을 하나요?
- **답변**: JavaScript XML의 약자로,<br>
JavaScript 코드안에서 HTML과 유사한 구문을 사용할 수 있게 해줍니다.
이를 통해 React에서 컴포넌트를 작성할 때 직관적인 UI구성을 할 수 있으며, Babel을 통해 JavaScript로 변환됩니다.

### **State와 Props의 차이**

- **질문**: React에서 **state**와 **props**의 차이점을 설명하세요.
- **답변**: 
    - **state**는 컴포넌트의 내부 데이터로, 변경될 수 있으며 컴포넌트 상태를 저장합니다.
    - **props**는 부모 컴포넌트로부터 전달되는 읽기 전용 데이터로, 컴포넌트 간 데이터 전달에 사용됩니다.

### **이벤트 처리 방식**

- **질문**: React에서 이벤트를 처리할 때 주의해야 할 두 가지 사항은 무엇인가요?
- **답변**:
**(1)** 이벤트 핸들러는 화살표 함수나 `bind`를 사용하여 `this`의 컨텍스트를 유지해야 합니다.<br>
**(2)** 이벤트 객체를 사용할 때 SyntheticEvent라는 가상 객체를 사용하여 성능 최적화를 지원합니다. 

### **컴포넌트 내 조건부 렌더링**

- **질문**: 컴포넌트에서 조건부 렌더링을 구현하는 일반적인 방법 두 가지는 무엇인가요?
- **답변**: 조건부 렌더링은 삼항 연산자와 `&&`연산자를 사용하여 구현할 수 있습니다. 삼항 연산자는 조건에 따라 반환할 요소를 구체적으로 지정할 때 유용하며, `&&`연산자는 조건이 참일 때만 특정 요소를 렌더링할 때 사용됩니다.

### **리스트 렌더링과 Key**

- **질문**: React에서 배열을 렌더링할 때 각 요소에 `key`를 부여하는 이유는 무엇인가요?
- **답변**: `key`는 각 요소를 고유하게 식별하기 위해 사용됩니다. 이를 통해 React는 각 요소를 효과적으로 비교하고 업데이트할 수 있으며, 리스트 렌더링 성능을 최적화할 수 있습니다.

### **useState Hook의 기본 사용법**

- **질문**: 함수형 컴포넌트에서 `useState` Hook을 사용하여 상태를 관리하는 기본적인 방법을 설명하세요.
- **답변**: `useState`는 상태 변수와 상태 업데이트 함수를 반환하는 Hook입니다.<br>
`const [state, setState] = useState(initialValue);`형태로 호출되며, `setState`를 통해 상태를 변경할 수 있습니다.

### **useEffect Hook의 역할**

- **질문**: `useEffect` Hook은 어떤 용도로 사용되나요?
- **답변**: `useEffect`는 컴포넌트가 렌더링된 후 특정 작업을 수행하도록 하는 Hook입니다. 예를 들어 API호출, 구독 설정, 타이머 시작 등의 부수효과(side effects)를 처리하는 데 사용됩니다.

### **Props로 함수 전달하기**

- **질문**: 부모 컴포넌트에서 자식 컴포넌트로 함수를 props로 전달하는 이유는 무엇인가요?
- **답변**: 부모 컴포넌트의 상태나 데이터를 자식 컴포넌트에서 변경해야 할 때 함수를 전달합니다., 자식 컴포넌트에서 부모 컴포넌트의 상태를 업데이트할 수 있어 상호작용을 가능하게 합니다.

### **컴포넌트의 생명주기 메서드**

- **질문**: 클래스형 컴포넌트에서 컴포넌트가 마운트된 직후에 호출되는 생명주기 메서드는 무엇인가요?
- **답변**: `componentDidMount`메서드는 컴포넌트가 마운트된 직후에 호출됩니다. 주로 외부 데이터 로딩이나 구독 설정 등의 작업을 수행하는 데 사용됩니다.

### **고차 컴포넌트(HOC)의 기본 개념**

- **질문**: 고차 컴포넌트(HOC)란 무엇인가요?
- **답변**: HOC는 컴포넌트를 인수로 받아 새로운 컴포넌트를 반환하는 함수입니다. 주로 컴포넌트의 재사용 가능한 로직을 분리하여 적용할 때 사용됩니다.

### **고차 컴포넌트의 네이밍 컨벤션**

- **질문**: HOC의 이름을 지을 때 일반적으로 어떤 접두사를 사용하나요?
- **답변**: HOC는 일반적으로 `with`접두사를 사용하여 네이밍됩니다.

### **Context API의 목적**

- **질문**: React에서 Context API는 어떤 문제를 해결하기 위해 사용되나요?
- **답변**: Context API는 계층 구조가 깊은 컴포넌트들 간에 데이터를 전달할 때 발생하는 props drilling문제를 해결합니다. 이를 통해 중간 컴포넌트를 거치지 않고 필요한 데이터에 접근할 수 있습니다.

### **Redux의 주요 요소**

- **질문**: Redux에서 상태 관리를 위한 세 가지 핵심 요소는 무엇인가요?
- **답변**:
    - **store** : 중앙에서 관리되는 상태 저장소<br>
    - **actions** : 상태 변경을 요청하는 객체<br>
    - **reducers** : 상태를 변경하는 순수 함수<br>

### **React Router의 기본 사용법**

- **질문**: React Router에서 URL 경로에 따라 컴포넌트를 렌더링하기 위해 사용하는 컴포넌트는 무엇인가요?
- **답변**: React Router에서 `Route`컴포넌트를 사용하여 특정 URL 경로에 따라 다른 컴포넌트를 렌더링할 수 있습니다.
`Route`는 `path`와 `element`속성을 통해 경로와 컴포넌트를 지정합니다.