# Process Writeup

## Name: Josiah Benitez
## Course: SEP12
## Period: 7
## Concept: Unit 7

### Overview

Unit 7 is all about ArrayLists which are similar to regular arrays but it only stores a reference to the data that it contains. ArrayLists also can be changed wihout losing or removing any data.
## First Challenge
### Counting executions of expressions 

On the Unit 7 exam I got question 15 wrong and here is the code to that question

```java
public static void sort(int[] arr)
{
  for (int j = arr.length - 2; j >= 0; j--)
  {
    int move = arr[j];
    int k = j + 1;

    while (k < arr.length && move > arr[k])
    {
      arr[k - 1] = arr[k]; /* Shuffle elements upwards */
      k++;
    }

    arr[k - 1] = move; /* Insert value into position */
    /* end of for loop */
  }
}
```
 
The question is asking how many times the expressions marked with shuffle upwards and insert value will execute. During my evaluation of this problem I miscounted the insert value expression count by one and ended up with 10 shuffle executions and 5 insertions. In reality the answer was 10 shuffles and 4 insertions. I miscounted and thought that I would have to insert each one back in but at the end of going through what would happen with the code one of the values are already in correct order without having to insert it. This mistake was pretty annoying for me to see as I honestly thought this question was on the easier side so I rushed it.


## Second Challenge
### Sorting Issues

Question 7 on the exam was such a small question but it made my brain hurt a bit. The reasoning behind this is that it was asking me "Which of the two calls sort(a), and sort(b) will result in line 8 being executed more times?" when I was given this code.

```java
ArrayList<Integer> a = new ArrayList<Integer>();
a.add(1);
a.add(2);
a.add(3);
a.remove(2);

ArrayList<Integer> b = new ArrayList<Integer>();
b.add(4);
b.add(3);
b.add(2);
b.add(1);

sort(a);
sort(b);
```
I had a hard time choosing a choice because I didnt know the specific way that the sort method was used so it was hard for me to determine which one would cause line 8 to execute more times. I can attribute this mistake mainly to me overthinking a pretty simple question, since sort(b) is using the b list it makes the most sense for sort(b) to be the one that causes b.add(4) to occur more than once. I tend to feel like im being tricked when a questions seems to easy to be true so I need to evaluate these questions better.


### Takeaways

* Take your time with questions that you think are easy because that is when mistakes happen.
* If a question looks simple in projectstem it actually is a lot of the time so dont overthink it.
* Put more time towards questions that require more reading of code so you are less likely to skim over important code.
* In multiple choice questions pick an answer that is right even if another answer already included that choice in it.
