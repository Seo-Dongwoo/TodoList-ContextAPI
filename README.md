# Context-API를 이용해서 TodoList 만들기

학습 목적
---
- useContext를 이용해서 상태 관리를 하기 위해서 학습하였다.
- useState로는 전역적인 상태 관리가 힘들기 때문에 학습하게 되었다.

학습 중 어려운 점
---
- 이번에는 styled-components를 써봤는데 props의 상태에 따른 css를 주는 부분에서 어려움을 겪었지만 styled-components 사이트에서 document를 보면서 해결하였다.
```
 ${(props) =>
    props.done &&
    css`
      border: 1px solid #38d9a9;
      color: #38d9a9;
    `}
```

- 할 일을 완료 처리하는 action.type인 TOGGLE의 return 부분에서 어려움을 겪었으나, 구글에 검색해서 해결하였다.
```
case "TOGGLE":
      return state.map((todo) =>
        todo.id === action.id ? { ...todo, done: !todo.done } : todo
      );
```

Netlify에 배포
---
todolist-context-api.netlify.app
