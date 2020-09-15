---
title: "[JavaScript]배열 정렬함수 sort()"
date: 2020-09-15
categories: JavaScript
---

배열 정렬하기 sort
=================

문법
```javascript
배열.sort(function(a, b){
  return 비교값;
})
```
비교값 > 0 : a가 b보다 작은 숫자의 인덱스를 가짐<br>
비교값 < 0 : b가 a보다 작은 숫자의 인덱스를 가짐<br>
비교값 = 0 : a와 b의 위치를 변경하지 않음<br>

**EXAMPLE**
```javascript
const numArr1 = [2, 0, 3, 4, 1];
const numArr2 = [2, 0, 3, 4, 1];
const objArr = [
    {id:2, name: 'Leo'},
    {id:0, name: 'Daniel'},
    {id:3, name: 'Asher'},
    {id:4, name: 'Chioe'},
    {id:1, name: 'Chioe'}
];

numArr1.sort(function(a, b) {return a - b;}); //오름차순 
numArr2.sort(function(a, b) {return b - a;}); //내림차순
objArr.sort(function(a, b){ //문자 오름차순
    if (a.name > b.name) return 1;
    else if (b.name > a.name) return -1;
    else return 0;
});

//id순으로 정렬
var sortingid = "id";
objArr.sort(function(a, b) {
    return a[sortingid] - b[sortingid];
}); 


console.log(`오름차순 : ${numArr1}`); //오름차순 : 0,1,2,3,4
console.log(`내름차순 : ${numArr2}`); //내림차순 : 4,3,2,1,0
console.log(objArr); //문자 오름차순
//[ {id:3, name: 'Asher'}
//  {id:4, name: 'Chioe'},
//  {id:1, name: 'Chioe'},
//  {id:0, name: 'Daniel'},
//  {id:2, name: 'Leo'}
//]
```

참고 및 출처 : 책'초보자를 위한 JavaScript 200제' p230 중급 093번

