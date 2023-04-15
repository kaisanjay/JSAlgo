#### Trapping Rain Water
```
Given n non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it can trap after raining.
```
https://leetcode.com/problems/trapping-rain-water/



###### Brute Force Solution thinking

###### Points
- flag up and down
- first for loop for checking every index
- second for loop ; starts from i+1 whenever it incounters a up make a **Block**
- third loop inside that loop to check how much block of water.

### WIP
```
const height = [4,2,0,3,2,5]; answer : 9

for (let i = 0; i < height.length; i++) {
  let currentI = i;
  let ivalue = height[i]
  
  for(let j= i; j< height.length; j++) {
    if (height[j]> ivalue) {
      let blockEnd = j;
      for(let k = i+1; k <= blockEnd; k++) {
        console.log('i:', i, 'k:', k)
      }
      break
    }
  }
}
```
```
i: 0 k: 1
i: 0 k: 2
i: 0 k: 3
i: 0 k: 4
i: 0 k: 5
i: 1 k: 2
i: 1 k: 3
i: 2 k: 3
i: 3 k: 4
i: 3 k: 5
i: 4 k: 5
```

Open Points:

```
Block1
i: 0 k: 1
i: 0 k: 2
i: 0 k: 3
i: 0 k: 4
i: 0 k: 5
```


- ye block me saare water block aagye so baaki ke blocks ka koi sense ni hai na
- but har problem me esa ni hoga.
- jo blocks count hogyi hai wo apan ko minus karna hai 
current specific case me Block1 me saare areas count ho gye hai already  ![IMG_7495 (1)](https://user-images.githubusercontent.com/16288226/232232991-e226d449-1032-4b47-9eae-08b22cc14b05.jpg)



