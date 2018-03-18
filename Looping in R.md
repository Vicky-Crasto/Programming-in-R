Understanding Looping in R
--------------------------

Exercises are taken from

[Scripting Loops exercises
Vol.1](https://www.r-exercises.com/2016/06/01/scripting-loops-in-r/)

[Scripting Loops exercises
Vol.2](https://www.r-exercises.com/2016/12/01/scripting-loops-exercises-vol-2/)

### Exercise 1

write a repeat{} loop that prints all the even numbers from 2 - 10, via
incrementing the variable, "i &lt;- 0".

    i <- 1
    repeat{
      i <- i +1
      print(i)
      if(i >= 10){break}
    }

    ## [1] 2
    ## [1] 3
    ## [1] 4
    ## [1] 5
    ## [1] 6
    ## [1] 7
    ## [1] 8
    ## [1] 9
    ## [1] 10

### Exercise 2

Using the following variables:

msg &lt;- c("Hello") i &lt;- 1

Write a repeat{} loop that breaks off the incrementation of, "i", after
5 loops, and prints "msg" at every increment.

    msg <- c("Hello")
    i <- 1

    repeat{
      i <-  i+ 1
      print(msg)
      if(i==5){break}
    }

    ## [1] "Hello"
    ## [1] "Hello"
    ## [1] "Hello"
    ## [1] "Hello"

### Exercise 3

With, i &lt;- 1, write a while() loop that prints the odd numbers from 1
through 7.

    i <- 1
    while(i<8){
      print(i)
      i <- i + 2
    }

    ## [1] 1
    ## [1] 3
    ## [1] 5
    ## [1] 7

### Exercise 4

Using the following variables:

msg &lt;- c("Hello") i &lt;- 1

Write a while() loop that increments the variable, "i", 6 times, and
prints "msg" at every iteration.

    msg <- c("Hello")
    i <- 1

    while(i<7){
      print(msg)
      i <-i+1
    }

    ## [1] "Hello"
    ## [1] "Hello"
    ## [1] "Hello"
    ## [1] "Hello"
    ## [1] "Hello"
    ## [1] "Hello"

### Exercise 5

write a for() loop that prints the first four numbers of this sequence:
x &lt;- c(7, 4, 3, 8, 9, 25)

    x <- c(7, 4, 3, 8, 9, 25)

    for( i in 1:4){
         print(x[i])
    }

    ## [1] 7
    ## [1] 4
    ## [1] 3
    ## [1] 8

### Exercise 6

write a for() loop that prints all the letters in y &lt;- c("q", "w",
"e", "r", "z", "c")

    y <- c("q", "w", "e", "r", "z", "c")

    for( i in 1:length(y)){
      print(y[i])
    }

    ## [1] "q"
    ## [1] "w"
    ## [1] "e"
    ## [1] "r"
    ## [1] "z"
    ## [1] "c"

### Exercise 7

Using i &lt;- 1, write a while() loop that prints the variable, "i",
(that is incremented from 1 - 5), and uses break to exit the loop if "i"
equals 3.

    i<-1
    while(i< 5){
      i <- i + 1
     
      if( i == 3)break
      
       print(i)
    }

    ## [1] 2

### Exercise 8

Write a nested loop, where the outer for() loop increments "a" 3 times,
and the inner for() loop increments "b" 3 times. The break statement
exits the inner for() loop after 2 incrementations. The nested loop
prints the values of variables, "a" and "b".

    for( a in 1:3){
      for(b in 1:3){
       print(c(a,b))
       if(b==2){break}
      }
      
    }

    ## [1] 1 1
    ## [1] 1 2
    ## [1] 2 1
    ## [1] 2 2
    ## [1] 3 1
    ## [1] 3 2

### Exercise 9

Write a while() loop that prints the variable, "i", that is incremented
from 2 - 5, and uses the next statement, to skip the printing of the
number 3.

    i<- 1
    while( i < 6){
    i<- i +1
    if( i==3){next}
    print(i)
    }

    ## [1] 2
    ## [1] 4
    ## [1] 5
    ## [1] 6

### Exercise 10

write a for() loop that uses next to print all values except "3" in the
following variable:

i &lt;- 1:5

    i <- 1:5
    for( val in 1:5){
    if(val ==3){ next }
    print(val)

    }

    ## [1] 1
    ## [1] 2
    ## [1] 4
    ## [1] 5

### Exercise 11

Using the following variables:

x=1

i=c(1:10)

For this exercise, write a for() loop that increments x by two for each
i.

    x=1
    i=c(1:10)

    for(val in i){
      x <- x + 2
      print(c(val,x))
      
    }

    ## [1] 1 3
    ## [1] 2 5
    ## [1] 3 7
    ## [1] 4 9
    ## [1]  5 11
    ## [1]  6 13
    ## [1]  7 15
    ## [1]  8 17
    ## [1]  9 19
    ## [1] 10 21

### Exercise 12

Using the following variables:

x=1

y=40

i=c(1:10)

For this exercise, write a for() loop that increments x by three and
decrease y by two, for each i.

    x=1
    y=40
    i=c(1:10)
    for( j in i){
    x <- x + 3
    y <- y - 2
    print(c(j,x,y))
    }

    ## [1]  1  4 38
    ## [1]  2  7 36
    ## [1]  3 10 34
    ## [1]  4 13 32
    ## [1]  5 16 30
    ## [1]  6 19 28
    ## [1]  7 22 26
    ## [1]  8 25 24
    ## [1]  9 28 22
    ## [1] 10 31 20

### Exercise 13

Using the following variables:

a,b

For this exercise, write a nested for() loop (where the outer for loop
increment a from 2 to 8 by 1, and the inner for loop increment b from 1
to 6 by 1) that print "a, ' less than ',b" if a&lt;b.

    for(a in 2:8){
      for(b in 1:6){
        if( a<b){print(paste('a=',a," less than ", "b=",b,sep=""))}
      }
    }

    ## [1] "a=2 less than b=3"
    ## [1] "a=2 less than b=4"
    ## [1] "a=2 less than b=5"
    ## [1] "a=2 less than b=6"
    ## [1] "a=3 less than b=4"
    ## [1] "a=3 less than b=5"
    ## [1] "a=3 less than b=6"
    ## [1] "a=4 less than b=5"
    ## [1] "a=4 less than b=6"
    ## [1] "a=5 less than b=6"

### Exercise 14

Using the following variable:

x=c(2,4)

For this exercise, type a while () loop that adds even numbers to x,
while the length of x is less than 12.

For example, in the first iteration you get x = 2,4,6, and the third x
=2,4,6,8.

    x = c(2,4)
    i=6
    while(length(x)<12){
      x <- c(x,i)
      i <- i +2
      
    }
    print(x)

    ##  [1]  2  4  6  8 10 12 14 16 18 20 22 24

### Exercise 15

Using the following variable:

a=15:10 b=20:15

For this exercise, type a while () loop that computes a vector x=225 224
221 216 209 200 ,such that

x\[1\]=a\[1\]\*b\[6\]

x\[2\]=a\[2\]\*b\[5\]

x\[3\]=a\[3\]\*b\[4\]

. . x\[6\]=a\[6\]\*b\[1\]

    a <- c(15:10)
    b <- c(20:15)
    x<-c()
    i <- 1
    j <- 6

    while(i<7){
       x[i]<-a[i]*b[j]
       i <- i +1
       j <- j -1
       
    }
    print(x)

    ## [1] 225 224 221 216 209 200

### Exercise 15

Using the following variable:

a=1:10

For this exercise, type a while () loop that computes a vector x=1 3 6
10 15 21 28 36 45 55 ,such that

x\[1\]=a\[1\]

x\[2\]=a\[1\]+a\[2\]

x\[3\]=a\[1\]+a\[2\]+a\[3\]

    a <- c(1:10)
    x <- c()
    i<- 1
    while(i<=10){
      
    x[i]= sum(a[1:i])
    i <- i + 1
    }

    print(x)

    ##  [1]  1  3  6 10 15 21 28 36 45 55

### Exercise 16

Using the following variable:

i=10

x=10

For this exercise, type a repeat () loop that decreasing i computes
x=x/i until i=0.

    i=10
    x=10
    y=c()
    repeat{
      x=x/i
      print(x)
       i <- i-1
      if( i==0){break}
    }

    ## [1] 1
    ## [1] 0.1111111
    ## [1] 0.01388889
    ## [1] 0.001984127
    ## [1] 0.0003306878
    ## [1] 6.613757e-05
    ## [1] 1.653439e-05
    ## [1] 5.511464e-06
    ## [1] 2.755732e-06
    ## [1] 2.755732e-06

### Exercise 17

Using the following variable:

x=as.Date("10/11/2017","%d/%m/%Y")

For this exercise, type a repeat () loop that increment x until x is
equal to 31/12/2017.

    x=as.Date("10/11/2017","%d/%m/%Y")
    y = as.Date("31/12/2017","%d/%m/%Y")
    i <- 1

    repeat{
      x=x+1
      print(x)
      if(x==y){break}
    }

    ## [1] "2017-11-11"
    ## [1] "2017-11-12"
    ## [1] "2017-11-13"
    ## [1] "2017-11-14"
    ## [1] "2017-11-15"
    ## [1] "2017-11-16"
    ## [1] "2017-11-17"
    ## [1] "2017-11-18"
    ## [1] "2017-11-19"
    ## [1] "2017-11-20"
    ## [1] "2017-11-21"
    ## [1] "2017-11-22"
    ## [1] "2017-11-23"
    ## [1] "2017-11-24"
    ## [1] "2017-11-25"
    ## [1] "2017-11-26"
    ## [1] "2017-11-27"
    ## [1] "2017-11-28"
    ## [1] "2017-11-29"
    ## [1] "2017-11-30"
    ## [1] "2017-12-01"
    ## [1] "2017-12-02"
    ## [1] "2017-12-03"
    ## [1] "2017-12-04"
    ## [1] "2017-12-05"
    ## [1] "2017-12-06"
    ## [1] "2017-12-07"
    ## [1] "2017-12-08"
    ## [1] "2017-12-09"
    ## [1] "2017-12-10"
    ## [1] "2017-12-11"
    ## [1] "2017-12-12"
    ## [1] "2017-12-13"
    ## [1] "2017-12-14"
    ## [1] "2017-12-15"
    ## [1] "2017-12-16"
    ## [1] "2017-12-17"
    ## [1] "2017-12-18"
    ## [1] "2017-12-19"
    ## [1] "2017-12-20"
    ## [1] "2017-12-21"
    ## [1] "2017-12-22"
    ## [1] "2017-12-23"
    ## [1] "2017-12-24"
    ## [1] "2017-12-25"
    ## [1] "2017-12-26"
    ## [1] "2017-12-27"
    ## [1] "2017-12-28"
    ## [1] "2017-12-29"
    ## [1] "2017-12-30"
    ## [1] "2017-12-31"

### Exercise 18

Using the following variable:

x=100

y=50

i=1

For this exercise, type a repeat () loop that incrementing i computes
x=x-i and y=y+i until x&lt;y.

    x=100
    y=50
    i=1

    repeat{
      x = x-i
      y = y+i
      i<- i +1
      if(x<y){break}
      
      print(c(i,x,y))
    }

    ## [1]  2 99 51
    ## [1]  3 97 53
    ## [1]  4 94 56
    ## [1]  5 90 60
    ## [1]  6 85 65
    ## [1]  7 79 71

### Exercise 19

Using the following variable:
x=cbind(c(1,2,3,4,9,7,4,3),c(3,1,2,5,3,6,5,3))

For this exercise, type a for() loop that calculate y=3 8 18 44 126 140
100 84, such that

y\[1\]=x\[1,1\]\*x\[1,2\]

y\[2\]=x\[2,1\]\*sum(x\[1:2,2\])

y\[3\]=x\[3,1\]*sum(x\[1:3,2\]) . . . y\[8\]=x\[8,1\]*sum(x\[1:8,2\])

    x=cbind(c(1,2,3,4,9,7,4,3),c(3,1,2,5,3,6,5,3))
    y=c()

    for(i in 1:length(x[,1])){

      y[i]=x[i,1]* sum(x[1:i,2])  

    }
    print(y)

    ## [1]   3   8  18  44 126 140 100  84
