# lightning-lectures

# MVC

Repo: https://github.com/LongTR11/SPCA-app 

Presentation slides:https://slides.com/aurorahampton/deck

Video: n/a

# CORS

Repo: https://github.com/ahay-agile6/lightning-cors-lecture

Presentation slides:https://slides.com/aurorahampton/cors

Video:https://zoom.us/recording/share/fXcz2EdKJ2VysCqz_t1IZcgCPzOCzUSLiokrjEu3Ao-wIumekTziMw 

# Distributing Candies Fairly

https://www.codewars.com/kata/distributing-candies-fairly/train/javascript
```
There are some candies that need to be distributed to some children as fairly as possible (i.e. the variance of result needs to be as small as possible), but I don't know how to distribute them, so I need your help. Your assignment is to write a function with signature distribute(m, n) in which m represents how many candies there are, while n represents how many children there are. The function should return a List (or Array etc. depending on the specific language) which contains the number of candies each child gains.

Notice
The candy can't be divided into pieces.
The list's order doesn't matter.
Requirements
The case m < 0 is equivalent to m == 0.
If n <= 0 the function should return an empty list.
If there isn't enough candy to distribute, you should fill the corresponding number with 0.
```
## Solution
```
function distribute(m, n) {   
  // how can i get an array with "n" items?
  // write a for loop that adds one item every loop
  // set the length of the loop to n
  // have a variable that says candies = 0; candies += 1; if (candies == m) {}
  // within for loop, make it stop when the total = m
  let students = [];
  
  if (n <= 0) {
    return students; 
  }  
  
  let candies = 0;
  
  // initializing each student with 0 candies
  for (let i = 0; i < n; i++) {
    students[i] = 0;  
  }
  
  let k = 0;
  
  // distribute candies here
  for (let j = 0; j < m; j++) {
    // give a student a candy
    // example students[0] = students[0] + 1;
    // how can i tell if all the students have gone through?
    if (k === n) {
      k = 0;      
    }
    students[k] = students[k] + 1;
    k += 1; 
  }
  
  return students;
}
```
