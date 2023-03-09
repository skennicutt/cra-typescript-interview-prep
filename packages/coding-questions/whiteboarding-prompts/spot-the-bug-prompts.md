# "Spot the Bug" Prompts

Identify what the actual output will be in comparison to the expected output.

## Simple Questions
### Q1
```
const reverse = (stringToReverse: string) : string => {
  let index = 0;
  let endIndex = stringToReverse.length - 1;
  let swapChar = '';
  
  while (index <= endIndex) do {
    swapChar = stringToReverse[index];
    stringToReverse[index] = stringToReverse[endIndex];
    stringToReverse[endIndex] = swapChar;
  }

  return {
    reversedString: stringToReverse,
  }
}
```

`reverse('bobs or vagana')` is expected to return `anagav or sbob`, what does it actually return?
