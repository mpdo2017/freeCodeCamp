---
title: Find One or More Criminals in a Hunt
---
# Find One or More Criminals in a Hunt

---
## Problem Explanation 

A group of criminals escaped from jail and ran away, but you don't know how many. However, you do know that they stay close together when they are around other people. You are responsible for finding all of the criminals at once.


---
## Hints

### Hint 1 
Are you surrounding your regexp in slashes? 
```javascript
let regexp = /t.[a-z]*t/;
```

### Hint 2
Are you using the '+' flag in your regexp?
```javascript
let regexp = /E+/; // returns E, EE, EEE patterns
```


---
## Solutions

<details><summary>Solution 1 (Click to Show/Hide)</summary>

```javascript
let crowd = "P1P2P3P4P5P6CCCP7P8P9";

let reCriminals = /C+/; // Change this line

let matchedCriminals = crowd.match(reCriminals);
console.log(matchedCriminals);
```

</details>