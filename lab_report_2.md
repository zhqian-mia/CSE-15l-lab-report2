# Lab report 2
  
***part 1***   
  
**First step, create a web server called `StringServer`. In order to do that, open the github desktop, and open the weaver by VS code.**  
  
**Then, you need to create a new file and named it `StringServer.java`**    
  
**Write your code inside the new file. Below is a screenshot of mine.**  
![code1](https://github.com/zhqian-mia/CSE-15l-lab-report2/blob/main/%E6%88%AA%E5%B1%8F2023-04-24%20%E4%B8%8B%E5%8D%881.24.35.png?raw=true)  
  
**Now in the command line, enter the command below:**  
* `javac Server.java StringServer.java`
* `java StringServer 7028`  (select any port number that you like)
  
**Now the terminal should look like this.**
![terminal](https://github.com/zhqian-mia/CSE-15l-lab-report2/blob/main/%E6%88%AA%E5%B1%8F2023-04-24%20%E4%B8%8B%E5%8D%881.26.31.png?raw=true)  
  
**Open the link using Google, you should see something like this initially.**  
![initial website](https://github.com/zhqian-mia/CSE-15l-lab-report2/blob/main/%E6%88%AA%E5%B1%8F2023-04-24%20%E4%B8%8B%E5%8D%881.33.30.png?raw=true)
  
**Enter `/add-message?s=<string>`, replace the `<string>` with any string you want to show. Below is what you should get if you enter `/add-message?s=Good Morning!`**  
![morning](https://github.com/zhqian-mia/CSE-15l-lab-report2/blob/main/%E6%88%AA%E5%B1%8F2023-04-24%20%E4%B8%8B%E5%8D%881.34.14.png?raw=true)
* The `handleRequest` method are called.  
* The argument to this method is `http://localhost:7028/add-message?s=Good Morning!`  
* `content` is the field of the class. The initial value of the content is empty string.
* After we enter the `/add-message?s=<string>` request, the content's value become `"Good Morning!"`.  
  
**Now, let's try `/add-message?s=<string>` and replace the `<string>` with `What a lovely day!`. Now the website should look like this:**
![lovely](https://github.com/zhqian-mia/CSE-15l-lab-report2/blob/main/%E6%88%AA%E5%B1%8F2023-04-24%20%E4%B8%8B%E5%8D%881.34.39.png?raw=true)  
* The `handleRequest` method were called again.  
* The arguement now is `http://localhost:7028/add-message?s=What a lovely day!`
* The values of the relevant field of the class is `"Good Morning!\nWhat a lovely day!"`
* The value of the content was updated after we enter the new command. That is because in our code we want to keep the string content that was entered by us everytime.  
  
***part 2***  
  
* failure-inducing input:  
```
int[] input2 = {0, 1, 2, 3};
```
* input that does not induce failure: 
```
int[] input1 = {3};
```
* symptom 1 (failure-inducing input):  
![symptom 1](https://github.com/zhqian-mia/CSE-15l-lab-report2/blob/main/%E6%88%AA%E5%B1%8F2023-04-24%20%E4%B8%8B%E5%8D%883.50.11.png?raw=true)
* symptom 2: 
![symptom 2](https://github.com/zhqian-mia/CSE-15l-lab-report2/blob/main/%E6%88%AA%E5%B1%8F2023-04-24%20%E4%B8%8B%E5%8D%883.50.30.png?raw=true)
* Code before:   
```java
static void reverseInPlace(int[] arr){
  for (int i = 0; i < arr.length; i += 1){
    arr[i] = arr[arr.length - i - 1];
  }
}
```
* Code after:    
```java
static void reverseInPlace(int[] arr){
  for (int i = 0; i < arr.length; i += 1){
    int temp = arr[i];
    arr[i] = arr[arr.length - 1 - i];
    arr[arr.length -1 - i] = temp;
   }
}
```
  
***part 3***  
  
* In lab2, I learned to create a local server and increment the amount of time that I refersh the page by adding `/increment` in the end of path. 
* In lab 3, I learned to debug in a more comprehensive way. Such as when calculating the avergae value by rule out the smallest number, we need to minus the number of smallest number instead of just minus one. That is because it is possible that we have more than one smallest number, for example: `int[] {1, 1, 1, 9, 8, 4}`. In this condition, we need to minus three when divding by the total amount of numbers.
