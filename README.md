# Arrays lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1

Create an array of strings called `colors` that contain "orange", "red", "yellow", "turquoise", and "lavender".

Then, using array subscripting and string interpolation, print out the String `"orange, yellow, and lavender are some of my favorite colors"`. 
```swift 
let colors = ["orange" , "red" , "yellow" , "turquoise", "lavender"]
print("\(colors[0])" + " " + "\(colors[1])" + " " + "\(colors[3])" + " " + "are some of my favorite colors.")

```


## Question 2

Remove "Illinois" and "Kansas" from the array below.

`var westernStates = ["California", "Oregon", "Washington", "Idaho", "Illinois", "Kansas"]
```swift 
var westernStates = ["California", "Oregon", "Washington", "Idaho", "Illinois", "Kansas"]
westernStates.remove(at: 4)
westernStates.remove(at: 4)
print(westernStates)


```

## Question 3

Iterate through the array below. For each each state, print out whether or not it is **in the continental United States.**

```Swift 
let moreStates = ["Hawaii", "New Mexico", "Alaska", "Montana", "Texas", "New York", "Florida"]
var outside = [String()]
var hawa = "Hawaii"
var alaska = "Alaska"
for states in moreStates {
if states == hawa || states == alaska {
print("\(states) is not in the continental united states")
continue
}
print("\(states) is in the continental United States!"  )
}



```


## Question 4

Print out how many non-whitespace characters are in `myString`:

`let myString = "This is good practice with Strings!"`

Iterate through the array below. For each sentence, print out how many non-whitespace characters are in it.

`let myFavoriteQuotes = ["To be or not to be, that is the question.", "The only source of knowledge is experience.", "Mr. Gorbachev, tear down this wall!", "Four score and twenty years ago..."]` 

```Swift 
let myString = "This is good practice with Strings!"
var spaceCount = 0
for spaces in myString {
if spaces == " " {
spaceCount += 1
continue
}
}
print("The amount of spaces is \(spaceCount)")



```


## Question 5

Iterate through `garden` and place any 🌷 that you find into the `basket`. Replace any 🌷 that you pick up with `"dirt"`. Then print how many 🌷 are in your `basket`.

```swift 
var garden = ["dirt","🌷","dirt","🌷","dirt","dirt","🌷","dirt","🌷","dirt"]
var basket = [String]()
var flowerCount = 0
var index = 0
for (index,stuff) in garden.enumerated() {

if  stuff == "🌷" {
flowerCount += 1
basket.append(stuff)
garden[index] = "dirt "


}
}
print("There are \(flowerCount) flowers in my basket \(basket) but my garden is just dirt now!! \(garden)")
```

## Question 6

The below array represents an unfinished batting lineup for a baseball team. **You, the coach,** need to make some last minute changes:

- Add "Suzuki" to the end of your lineup.
- Change "Jeter" to "Tejada".
- Change "Thomas" for "Guerrero"
- Put "Reyes" to bat 8th instead.

```Swift 

var battingLineup = ["Reyes", "Jeter", "Ramirez", "Pujols","Griffey","Thomas","Jones", "Rodriguez"]

for (index, player) in battingLineup.enumerated() {


if  player == "Jeter" {
battingLineup[index] = "Tejada"
continue
}
if  player == "Thomas" {
battingLineup[index] = "Guerrero"
continue
}
if  index == 7 {
battingLineup[index] = "Reyes "
continue
}


}
battingLineup.append("Suzuki")
battingLineup.removeFirst()
print("The new batting lineup is \(battingLineup)")
```


## Question 7

Given an array of Ints, find out if it contains a target number.  

(The built-in `contains(_:)` function will do this, but you aren't allowed to use it for this exercise.)


```swift
var numbers: [Int]

let target: Int = 32
```

Ex.1

```swift
numbers = [4,2,6,73,32,4,2,1]

target = 32

//true
```

Ex. 2

```swift
numbers = [32459,2,4,5,1,4,2,1]

target = 3

//false
``` 
```Swift 
var numbers = [5,36,689,64,66,44,11,2345,6,3246,645,65879,788]
var target = 6
for number in numbers {
   if number == target {
       print("the target number \(target) is equal to the \(number) which is in our data set")
    }
}
```


## Question 8

Find the largest value in an array of Int.  Do not use the built-in `max()` method.

```swift
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}

//This creates an array of 100 numbers in between 0 and 200.  For now, you don't need to worry about how it does that.
``` 

```Swift 
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}
var greatestNumber = 0
for number in arrayOfNumbers {
if number >= 200 {
greatestNumber = number

}

}
print(greatestNumber)
```


## Question 9

Find the smallest value in an array of Int.  Do not use the built in min() method.

```swift
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}
var lowestNum = 0
//This creates an array of 100 numbers in between 0 and 200.  For now, you don't need to worry about how it does that.
for number in arrayOfNumbers {

if number <= 1 {
lowestNum = number

}
}
print(lowestNum)

```


## Question 10

Iterate through `secondListOfNumbers`, and print out all the odd numbers.

```Swift 
var secondListOfNumbers = [19,13,14,19,101,10000,141,404]
var oddnumbers: [Int] = []
for number in secondListOfNumbers {
if number % 2 == 1  {
oddnumbers.append(number)
//        print(number)

}
}
print(oddnumbers)




```


## Question 11

Iterate through `thirdListOfNumbers`, and print out the sum.

```Swift 

var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]
var sum = 0
for number in thirdListOfNumbers  {
if number > 0 {
sum  += number
}
}
print(sum)





```

## Question 12

Iterate through `thirdListOfNumbers`, and print out the sum of all the even numbers.

```swift 
var thirdListOfNumbers = [11, 26, 49, 61, 25, 40, 74, 3, 22, 23]
var sumEven = 0
for number in thirdListOfNumbers {
if number%2 == 0 {
sumEven += number
}
}
print(sumEven)




```


## Question 13

Append every Int that appears in both `listOne` and `listTwo` to the `sharedElements` array. Then print **how many Ints** are shared.

```swift
var listOne = [28, 64, 7, 96, 13, 32, 94, 11, 80, 68]
var listTwo = [18, 94, 48, 6, 42, 68, 79, 76, 13, 7]
var sharedElements = [Int]()
var sharedElementsCount = 0

for number1 in listOne {
for number2 in listTwo {
if number1 == number2 {
//        sharedElementsCount += 1
sharedElements.append(number1)

}
}
}
print(sharedElements.count)
print(sharedElementsCount)
```


## Question 14

Write code such that `noDupeList` has all the same Ints as `dupeFriendlyList`, but has no more than one of each Int.

```swift
var dupeFriendlyList = [4,2,6,2,2,6,4,9,2,1]
var dupeList: [Int] = [4,6,2]
var noDupeList: [Int] = []
for (index,dupe) in dupeFriendlyList.enumerated() {
if dupeList.contains(dupe)  {
noDupeList.append(dupe)
}
else if dupe > 0{
noDupeList.append(dupe)
}
else if dupeList.contains(dupe) {
noDupeList.remove(at: index)
}


}
print(noDupeList)

```

## Question 15

Find the second smallest number in an Array of Ints

```Swift 
let arrayOfNumbers: [Int] = (1...100).map{ _ in Int.random(in: 0...200)}.map{Int($0)}
var secondLowest = 0
for number in arrayOfNumbers {
if number == 2 {
secondLowest += number
}
}

print(secondLowest)


```


## Question 16

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Find the sum of all the multiples of 3 or 5 below 1000. 

```Swift 
var multArray = [Int()]
var sum = 0
for number in 0...999  {
if number % 3 == 0 || number % 5 == 0 {
multArray.append(number)
sum += number
}
}
print(multArray)
print(sum)
```


## Question 17

Make an array that contains all elements that appear **more than twice** in `someRepeatsAgain`.

```swift
var someRepeatsAgain = [25,11,30,31,50,28,4,37,13,20,24,38,28,14,44,33,7,43,39,35,36,42,1,40,7,14,23,46,21,39,11,42,12,38,41,48,20,23,29,24,50,41,38,23,11,30,50,13,13,16,10,8,3,43,10,20,28,39,24,36,21,13,40,25,37,39,31,4,46,20,38,2,7,11,11,41,45,9,49,31,38,23,41,16,49,29,14,6,6,11,5,39,13,17,43,1,1,15,25]
var repeatsAgain = 0
var repeatsAgainCount = 0

var repeatsAgainArray = [Int()]

for number in someRepeatsAgain {
if number == repeatsAgain {
repeatsAgainArray.append(number)
continue
}
repeatsAgain = number
}
repeatsAgainArray.removeFirst()
print(repeatsAgainArray)

```


## Question 18

Identify if there are 3 integers that sum to 10 in the following array. If so, print them as a triplet. If there are multiple triplets, print all possible triplets.

var tripleSumArr = [-20,-14, -8,-5,-3,-2,1,2,3,4,9,15,20,30]

```Swift 
var tripleSumArr = [-20,-14, -8,-5,-3,-2,1,2,3,4,9,15,20,30]
var sumArr = [Int]()
var sumCount = 0
var sum = 0

for numbers in tripleSumArr {
if numbers
}




```
## Question 19

Given an array of Strings, find the the String with the most "a"s in it.

input: `["apes", "abba", "apple"]`

output: `"abba"`
```Swift 
var  animalArray = ["apes", "abba", "apple"]
var aCount = 0
var aCountArr = [Int()]

for animals in animalArray {
for letters in animals {
if letters == "a" {
aCount += 1
}
}

aCountArr.append(aCount)
aCount = 0

}
//aCountArr.removeFirst()
print("There are \(aCountArr.max() ?? 0) a's in \(animalArray[1]) containing the most a's ")



```

## Question 20

Given an Array of Arrays of Ints, find the Array of Ints with the largest sum:

Input: `[[2,4,1],[3,0],[9,3]]`

Output: `[9,3]` 
```swift 

var sumArray = [[2,4,1],[3,0],[9,3]]
var sum1 = 0
//var sum2 = 0
//var sum3 = 0
for array in sumArray  {
for number in array {
if number > -1 {
sum1 +=  number
}
}
print(sum1)
sum1 = 0
}



```


## Question 21

Given an Array of Tuples of type `(Int, Int)`, create an array containing all the tuples where the first Int is equal to the second Int.

Input: `[(4,2), (-3,-3), (1,1), (3,9)]`

Output: `[(-3,-3), (1,1)]`


## Question 22

Given an Array of Bools, make a variable called `allAreTrue` that is true if all of the Bools are true and false if any of them are false.

Input: `[true, false, true, true]`

Output: `false`


## Question 23

Given an Array of Ranges of Ints, create an array that has all the values from all the ranges in order from smallest to greatest with no duplicates.

Input: `[0..<3 , 2..<10, -4..<6, 13..<14]`

Output: `[-4,-3,-2,-1,0,1,2,3,4,5,6,7,8,9,10,13]`


## Question 24

Given an array of Characters, create a String ignoring and uppercase Characters and spaces.  Then uppercase every other character of the String.

Input: `let arr: [Character] = ["a", "p","P","l","E"," ","S","a","u","C,"e"]`

Output: `"ApLeAuE"`


## Question 25

Print out each element in `myMatrix`

`var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]`


## Question 26

Print out the sum of the diagonals of `myMatrix`.

`var myMatrix = [[10, 14, 12], [91, 1, 9], [31, 3, 21]]`


## Question 27

Using for loops, rotate `matrixToRotate` 90 degrees.

var matrixToRotate = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

![Matrix Rotation](images/rotated_matrix.jpeg)
