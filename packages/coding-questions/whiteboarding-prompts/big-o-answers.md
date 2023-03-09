# Solutions to Big O Prompts
## Q1
- Time complexity: `O(n)`
- Space complexity: `O(n)`

### How can you make this function more efficient?
Look to performing in-place operations:
```
const reverse = ({ stringToReverse }: ReverseStringArgs) : ReverseStringReturn => {
  let index = 0;
  let endIndex = stringToReverse.length - 1;
  let swapChar = '';
  
  while (index <= endIndex) do {
    swapChar = stringToReverse[index];
    stringToReverse[index] = stringToReverse[endIndex];
    stringToReverse[endIndex] = swapChar;
    index++;
    endIndex--;
  }

  return {
    reversedString: stringToReverse,
  }
}
```

This will change the complexities to:
- Time complexity: `O(3 + n/2)` => `O(n/2)`
- Space complexity: `O(3)` => `O(1)`

To show more mastery of js/ts, the above can be written as:
```
const reverse = ({ stringToReverse }: ReverseStringArgs) : ReverseStringReturn => {
  return stringToReverse.forEach((_char, index) => {
    const endIndex = stringToReverse.length - 1;

    if (index >= endIndex) { 
      // TODO: not sure how to exit early from the forEach loop, verify that this works
      return;
    }

    const swapChar = stringToReverse[index];
    stringToReverse[index] = stringToReverse[endIndex];
    stringToReverse[endIndex] = swapChar;
  })
}
```

This will change the complexities to:
- Time complexity: `O(n/2)`
- Space complexity: `O(1)`
