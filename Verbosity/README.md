# Verbosity: Language Features and Syntax

Writing documentation is tedious and annoying. On the other hand, missing documentation is vexing when trying to read and understand new code.

Verbosity virtually elimantes the need to write documentation by blurring the lines between code, pseudocode, and documentation. The result is a language that reads more like an essay or a mathematical proof rather than traditional code.

## Comments
Commenting an entire line:
```
%% This is a commented out line.
%% This is another commented line.
```
Writing inline comments:
```
If true, return false. ++This is an inline comment.++ Otherwise return false.
```

## Main Function
The main function is the entry point to your program. This function is annotated with a single hashmark `#`. For example:
```
# Example Program
Print "hello world!"
```

## Classes
Classes are created using two hashmarks `##`. The `->` symbol indicates the properties of the class. The body text under the class heading is the initialization code. For example:
```
## Dog
-> name, age, breed

Let Dog's name be name.
Let Dog's age be age.
If breed is not nil, let Dog's breed be "unknown".
Otherwise let Dog's breed be breed.
```

## Functions
Functions are declared using three hashmarks `###`. The `->` symbol indicates the inputs of the function. The `<-` symbol indicates the outputs of the function. Optionally, alternate function call forms can be enumerated under the `* Idiomatic Usage` section. For example:
```
### Hatch
-> egg
<- success
* Idiomatic Usage
    * "`Hatch` `egg`"
    * "whether `egg` `Hatch`es"
    * "`egg` `Hatch`es"

If egg's Incubation-Time is greater than egg's time-to-hatch, do the following:
    Set egg's state to "Hatched".
    return true.
Otherwise, return false.
```

We can call the `Hatch` function and assign it to a variable `success` like so:
```
Let success be the result of Hatch with input egg.
```
Or we can discard the result and call the function like this:
```
Execute Hatch.
```

But since we specified alternate function call forms under `* Idiomatic Usage`, we can also use this function as follows:
```
Let success be whether egg Hatches.
```
or
```
Hatch egg
```
Because we specified custom idiomatic usage for `Hatch`, function calls read a lot more like natural English.
