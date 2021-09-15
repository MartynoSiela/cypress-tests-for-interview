# Solutions for practical task by TeleSoftas
This document contains solutions for the tasks and/or any other information that might be useful for the review process.
## Task 1
TODO
## Script task (task 2 and task 3)
### Tools
For the following tasks I have decided to use the Cypress framework. Some of the reasoning for this decision:
- I wanted to use a JavaScript framework because I want to gain more experience with this language
- I have never used Cypress before and this was a great opportunity to get familiar with it
- I have some experience with Protractor framework, but wanted to be able to compare it with Cypress
- I wanted to learn something new
### Issues
I am more used to writing e2e tests using C# and Selenium and Javascript acts a bit differently. Moreover Cypress itself seems to be a bit different compared to Protractor. It might be my limited knowledge of Javascript that led me to the following issues:
- A value cannot be returned from a method for further use
    - I found a workaround for storing a value with can be seen in use in both task 2 and task 3
- I have more experience with POM and am used to it
    - In Cypress it is sometimes hard to implement a POM as separation between POM methods and assertions for tests is not possible
 ~~TODO write a different implementation of the scripts avoid POM~~
- Cypress does not natively support Iframes
    - I found a solution which uses custom Cypress Commands but it was not a stable one
    - I found another solution with uses custom functions and this seems to be working consistently
### Task 2
Some of the previously mentioned issues arose because of how the task is given. Following the task word by word allows to create a script that has no assertions which in my understanding is a bad test. In the original implementation i have added an assert of what was entered to the search field, but asserted the value to be not empty and for it to be a number which seems strange. Original solution can be launched with the following command:
```
npm run task2
```

~~TODO In the alternative implementation of task 2 I will assume that that there are always 9 images displayed in the iframe and assert the count to be equal to 9. With this assumption I can also assert the search bar input to be equal to 9 as well.~~

Alternative implementation asserts that the count of images is equal to 9. It get's the actual count and passes the value to the search bar and also asserts that it was entered to the search bar. Alternative solution can be launched with the following command:
```
npm run task2-alt
```

### Task 3 
The last point of this task (...read and print the text...) in my mind translates, that the value has to be stored in a variable after reading and printed from that variable. Here I again face the issue that value cannot be passed further on in Cypress. I end up with storing the value internally which does not seem to be a good usage of the framework. Also i do not assert the value as this is not asked in the task. Original solution can be launched with the following command:
```
npm run task3
```

~~TODO In the alternative implementation of task 3 I will not store the value but just get it and print it. I will assert the value for the test to have an assert at the end. I will try to find a way to hide the errors that can be seen in the console when visiting the page as they are not relevant for the provided test case and just look not nice and misleading.~~

In the alternative implementation the value is read and stored in **this context** although this needs arrow function to be replaced by regular functions. Assertion of the text was not implemented. Hiding of errors in the console was not implemented as an old solution that I have found was deprecated since Cypress version 6. However the errors might be due to my home network setup (Pi-hole is blocking some domains...). Alternative solution can be launched with the following command:
```
npm run task3-alt
```

## Extra task
TODO
