# Questions & Answers

## What is the complexity of each of the four search methods in terms of array or list size n?
- findTeamPosition for array - `Optional<Integer> findTeamPosition(final Team[] arr, final String key)`
  
- findTeamPosition for List - `Optional<Integer> findTeamPosition(final List<Team> list, final String key)`

- findTeamMinFunding (linear search) - `Optional<Integer> findTeamMinFunding(final Team[] arr, final int minFunding)`

- findTeamMinFundingFast (binary search) - `Optional<Integer> findTeamMinFundingFast(final Team[] arr, final int minFunding)`

## What happens in the case of binary search if the array is not sorted?
  I tried switching t2 and t3 in the array, and here is what happened. Array element with funding of 600 could not be found. Elements with 500 and 700 are still the same. <br /> 
  
  `Main` runs like following when search for min funding of 600: <br />
  
`Enter min funding to search: 600` <br />
`Looking for min funding 600` <br />
`Found!` <br />
`Name: Germany` <br />
`Head coach: Löw` <br />
`Funding: 700` <br />
`Array index: 1` <br />
`Ranking: 2` <br />

## What is the purpose of constructor argument validity checking?
The purpose of constructor argument validity checking is to make sure the parameters are not empty before running, that is, to check the compiling errors in early type. <br />

By doing so, it will trow `Exception` before method executive. when set the parameters as `null` or `0`, the following reminds are showed: <br />
`Exception in thread "main" java.lang.IllegalArgumentException: name is null` <br />
`Exception in thread "main" java.lang.NumberFormatException: funding is 0` <br />

However, when I removed the validity checking constructors, even if the parameters are set empty,  class `main` still runs as usual, and return different answers.

## What is the purpose of using the keyword `final`with variables and arguments?
The purpose of using the keyword `final` is to declare the value of variables and arguments are constant and could not be altered. When you try to redefine a `final` varialble, in Intellij, it will remind you with red underlines and right cursor hint like `Cannot assign a value to final variable "size"`. <br />

On the other hand, by doing so could optimize the program for faster performance, since everytime using `final` variales, it will use the value of the varialble directly.

## What are alternatives to using `Optional` and how do they compare?
`Optional<Integer>` could be replaced by `int`. <br />
`Optional.of(i)` could be replaced by `i`.<br />
`Optional.empty()` could be replaced by `-1`. <br />

The main difference between the two is when using the integer objects of `int`, the integer could be used directly, while using `Optional`, it needs special methods like `isPresent()`, `get()`, and etc.