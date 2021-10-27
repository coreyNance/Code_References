# Code References based on syntax
<br>

# FOR LOOPS


## BASIC FOR LOOP SYNTAX (Using reverse staircase as example)

### JavaScript Syntax 
One part I learned is that javaScript's log outputs return to the next line after 
each output.  The example here is used to make a reverse staircase
```
              #
             ##
            ###
```
This is the older style of javaScript for loops and I declared the variables outside 
the loops so that I can use then within each forloop freely.  Most of this style matches C++ except to account for the automatic return line after output, I instead created variables within the outer loop to increment after each loop and just output them together.  You will see with c++ how its set up a little different. 
```
function staircase(n) {
    
   let i;
   let p;
   let j;
    
    for(i = 0; i < n; ++i) {
        let space = " "
        let hash = "#"
        let spaceFill = "";
        let hashFill = "";
        
        for(p = n-1; p > i; p--) {
           spaceFill = spaceFill + space;
        }
        for(j = 0; j <= p; j++) {
              hashFill = hashFill + hash;
        }
        
        console.log(spaceFill + hashFill);
    }
    
   
}

```
### C++ Syntax 
Most of the code syntax and logic in this example doesnt change with c++.  The main difference here is the int declaration and the cout statement is for output.  To go to the next line you have to use endl either after your output or as a stand alone as I did.  Without an endl, C++ will always output on the sameline.  For this reason is why I didnt need to add extra variables to increment then output, I just output within the nested forloops and the just have the outer forloop end the line.  This method creates the same out put as the example above. 
```
void staircase(int n) {
    int i;
    int j;
    int p;
    
    for(i = 0; i < n; ++i) {
        for(p = n-1; p > i; p--) {
            cout << " ";
        }
        for(j = 0; j <= p; j++) {
              cout << "#";
        }
        cout << endl;
    }
}
```


<br>

## HOW TO USE A FOR LOOP TO SUM AN ARRAY

### JavaScript Syntax

```
let arrayTotal = 0;
    
    for (let i = 0; i < arrray.length; i++) {
        arrayTotal = arrayTotal + array[i];
    }
        return arrayTotal;
```

### C++ Syntax

```
int arrayTotal = 0;
    
    for (int i = 0; i < array.size(); i++) {
        arrayTotal = arrayTotal + array[i];
    }
        return arrayTotal;
```

### Java Syntax (For using a List)
Example using a function with a List as the argument

```
public static int simpleArraySum(List<Integer> ar) {
    
        int arrayTotal = 0;
    
    for (int i = 0; i < ar.size(); ++i) {
        arrayTotal = arrayTotal + ar.get(i);
    }
        return arrayTotal;
        
    
    }
```




## HOW TO SPLIT AN INTEGER INTO AN ARRAY 

### JavaScript Syntax

```
let integer = 123456789

let integerArray = String(interger).split("");
```
Return String back to integer
```
integerArray.map(x => parseInt(x));
```


-------------------------------------------------------------------------------------

## HOW TO SPLIT A WORD INTO AN ARRAY

### JavaScript Syntax

```
let word = Corey

let wordArray = word.split('');
```


---------------------------------------------------------------------------------------

## HOW TO FIND THE MAX NUMBER OR NUMBERS IN AN ARRAY

### JavaScript Syntax

```
let numberArray = [1,2,3,4,5,6,7];

let highestNumber = (Math.max(...Array));
```
---------------------------------------------------------------------------------------

## HOW TO ROUND TO THE NEAREST MULTIPLE OF 5

### JavaScript Syntax 

```
Math.ceil(argument/5) * 5
```

---------------------------------------------------------------------------------------

## HOW TO DO FOR LOOPS ON ARRAYS

### JavaScript Syntax

```
for(let i = o; i < array.length; ++i) {
    info here
}
```

---------------------------------------------------------------------------------------

## HOW TO SUM AN ARRAY

### JavaScript Syntax
 ```
 Array.reduce((a,b) => a + b, 0);
 ```