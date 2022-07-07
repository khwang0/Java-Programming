<style>
    ol {
        list-style-type: upper-alpha;
    }
    .ss  ol {
        list-style-type: lower-roman;
    }

    body {
        counter-reset: h3counter;
    }

    div.row {
        /* display: inline; */
        -webkit-column-count: 2;
        -moz-column-count: 2;
        column-count: 2;
        -webkit-column-gap: 20px;
        -moz-column-gap: 20px;
        column-gap: 20px;
        counter-reset: h3counter;
        column-rule-style: solid;
        column-rule-color: #000;
        column-rule-width: 1px;
        width: 98%;
    }
    div.question {
        display: inline-block;
        vertical-align: top;
    }
    h3:before {
        content: "Q" counter(h3counter);
        font-weight: bold;
        counter-increment: h3counter;
    }
    h3 {
        margin-bottom: 10px;
    }
    code {
        background-color: rgba(200, 200, 200, 0.2);
    }
    .vscode-light pre {
        background-color: rgba(200, 200, 200, 0.2);
    }
    .hljs-number {
        color: initial;
        font-weight: bold;
    }
    input +  div  ans { display: none; }
    input +  div  ans:before { display: none; }
    input:checked +  div  ans {
        display: inline ;font-weight: bold; color: blue;
    }
    input:checked +  div  ans:before {
        display: inline;
        content: "☑️";
    }
    input {
        display: block;
        width: 200px;
    }
    input:before {
        content: 'Reveal Answer';
    }
</style>

# Exercise 1

## A. Reflection Questions


<input type='checkbox'>
<div class=question>

### 
What is the proper way to write a comment in Java?
<div class=ss>

1. Begin a line with `#`.
2. Begin a line with `//`.
3. Enclose the comment with a pair of `###`.
4. Enclose the comment with a pair of `/*` and `*/`.
</div>

1. i only
2. ii only
3. i and iii only
4. ii and iv only<ans/>
5. all of above

<ans>Comments in Java an Python are quite different!</ans>

</div>

<input type='checkbox'>
<div class=question>

### 
Which of the following primitive types can store the decimal value 9.9?
1. `long`
2. `byte`
3. `float` <ans/>
4. `char`
5. `boolean`

<ans>Decimal values stores in float and double only.</ans>

</div>

<input type='checkbox'>
<div class=question>

###
What is the output of the following if `score` is 75? Be careful please.

```java
if (score > 40) { 
    System.out.println("C"); 
} else if (score > 65) { 
    System.out.println("B"); 
} else if (score > 80) { 
    System.out.println("A"); 
} 
if (score < 40) { 
    System.out.println("F"); 
}
```

1. A
2. B
3. C <ans/>
4. F
5. It prints more than one character. 

<ans>The order of `if` are important!</ans>
</div>

# B. Programming exercise

### 
Use `println` statement to create the following ASCII art. Be careful of the escape characters!
```
    /\/\/\
   /------\        
   | *  + |
   |   .  |
    \____/
```
### 
Try to print from 1 to 10 on the same line
### 
Try to print from 10 to 1 on different line
### 
Try to print from 1 to 100 but skipping all numbers ends with 7.

> Hint: try `%` operator and `if`

### 
Try to print from 1 to 100 but skipping all numbers ends with 7 or it is a multiple of 7.

> Hint: try `%` operator

# C. A bigger problem

Given the following code, complete the program so that it prints a nice look calendar of the month.

```java
...
public static void main(String args[]) {
    String month = "July";
    int days = 31;
    int firstDay = 5; //   1/7/2022 is on Friday 
}

```

Expected output
```txt
            July
Sun Mon Tue Wed Thu Fri Sat
                      1   2
  3   4   5   6   7   8   9
 10  11  12  13  14  15  16
 17  18  19  20  21  22  23
 24  25  26  27  28  29  30
 31
```

> Hint: Try to print the first three lines.