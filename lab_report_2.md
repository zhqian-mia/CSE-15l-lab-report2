# Lab report 2
*part 1*  
First step, create a web server called `StringServer`. In order to do that, open the github desktop, and open the weaver by VS code.  
Then, you need to create a new file and named it `StringServer.java`    
Write your code inside the new file. Below is a screenshot of mine.  
![code1](https://github.com/zhqian-mia/CSE-15l-lab-report2/blob/main/%E6%88%AA%E5%B1%8F2023-04-24%20%E4%B8%8B%E5%8D%881.24.35.png?raw=true)  
Now in the command line, enter `javac Server.java StringServer.java` ,and then enter `java StringServer 7028`  (select any port number that you like).  
Now the terminal should look like this.
![terminal](https://github.com/zhqian-mia/CSE-15l-lab-report2/blob/main/%E6%88%AA%E5%B1%8F2023-04-24%20%E4%B8%8B%E5%8D%881.26.31.png?raw=true)  
Open the link using Google, you should see something like this initially.
![initial website](https://github.com/zhqian-mia/CSE-15l-lab-report2/blob/main/%E6%88%AA%E5%B1%8F2023-04-24%20%E4%B8%8B%E5%8D%881.33.30.png?raw=true)
Enter `/add-message?s=<string>`, replace the `<string>` with any string you want to show. Below is what you should get if you enter `/add-message?s=Good Morning!`  
![morning](https://github.com/zhqian-mia/CSE-15l-lab-report2/blob/main/%E6%88%AA%E5%B1%8F2023-04-24%20%E4%B8%8B%E5%8D%881.34.14.png?raw=true)
Now, let's try `/add-message?s=<string>` and replace the `<string>` with `What a lovely day!`. Now the website should look like this:
![lovely](https://github.com/zhqian-mia/CSE-15l-lab-report2/blob/main/%E6%88%AA%E5%B1%8F2023-04-24%20%E4%B8%8B%E5%8D%881.34.39.png?raw=true)


