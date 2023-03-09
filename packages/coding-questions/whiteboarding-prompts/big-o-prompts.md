# Big O Prompts

Answer the following questions for each problem:
- what is the time complexity of `function()`?
- what is the space complexity of `function()`?
- how can you make this function more efficient?

## Simple Questions
### Q1
```
interface ReverseStringArgs {
  stringToReverse: string;
}

interface ReverseStringReturn {
  reversedString: string;
}

const reverse = ({ stringToReverse }: ReverseStringArgs) : ReverseStringReturn => {
  let reversedString = '';

  let reverseIndex = stringToReverse.length - 1;

  while (reverseIndex >= 0) do {
    reversedString = reversedString + stringToReverse[reverseIndex];
  }

  return {
    reversedString
  }
}
```
