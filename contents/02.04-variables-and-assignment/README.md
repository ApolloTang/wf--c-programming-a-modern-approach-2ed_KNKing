               


## Types


### float

The value of a float type is only approximation. For example storing 0.1 in float type will be round to 0.09999999999999987. 



## Declarations

Variable declaration in c has the following syntax:

```c
int height; 
float profit;
```

If several variables have the same type, their declarations can be combined:

```c
int height, length, width, volume; 
float profit, loss;
```





### Declarations section

Prior to C99 **all** *declarations* must come before *statements*:

```c
int main(void)
{
  // Declaration section
  <declarations of variable a>
  <declarations of variable b> 
      
  // Statements start after declartion section  
  <statements that use a>
  <statements that use b>
}
```

With C99 declaration is not necessary until it is needed:

```c
int main(void)
{
  <declarations of variable a> 
  <statements that use a>
   
  <bunch of statements here>
  
  <declarations of variable b> 
  <statements that use b>
}
```



## Assignment

You must declare a variable before you use them:

```c
int height;
height = 8; 
```
but not
```c
height = 8; 
int height;
```

It is a good practice to apend a letter f to a constant that contains a decimal point if the number is assigned to a float:

```c
float profit;
profit = 2150.48f;
```

Mix type is possible but unsafe:

```c
int height;
height = 2150.48f;
```

## Printing the value of a variable

By default, `%f` displays a number with six digits after the decimal point.
```c
profit = 2150.48f;
printf("Profit: $%f\n", profit); 
```
Result:
```
Profit: $2150.479980
```
To display `p` digits after the decimal point, we can put `.p` between `%` and `f`: 
```c
printf("Profit: $%.2f\n", profit);
```
Result:
```
Profit: $2150.48
```
[link to ipynb](./printing-the-value-of-a-variable.ipynb)