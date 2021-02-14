# date-picker 만들기(1) 
## javascript
---

1️⃣ 전체 월(month) 지정하기

 ```js
 const months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "Octobor", "November", "December"];
 document.querySelector(".date h1").innerHTML = months[date.getMonth()];
```

❗ const month = date.getMonth(); 로 지정하면 index가 0부터 시작하기 때문에 안맞는다.  따라서 각 월(month)로 배열을 만들어준 뒤, 
해당 배열에 date.getMonth()를 적용하면 index가 똑같이 0부터 시작한다

2️⃣ 전체 요일(days) 지정하기
    
```js
const firstDayIndex = new Date(date.getFullYear(), date.getMonth()).getDay();
//console.log(firstDayIndex);
```

❗  달력에서 현재 월이 시작되는 index   >> 월요일이면 1 출력(일요일부터 0)

