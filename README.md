Character is a vowel or consonant in C
Here, in this section we will discuss the program to check whether the character is a vowel or consonant in C.
Character is a vowel or consonant
Working:-
Take character input from the user
Check if Input is a lowercase of upper case vowel
If yes then print vowel
If not then print consonant
Can also additional check if it’s a non-character item
We will discuss various methods to do the same thing.

Method 1
Method 1
Run
// C Program to check whether alphabet is vowel or consonant
#include <stdio.h>

// main function
int main()
{
    char c='F';

    
        
    //checking for vowels	
    if(c=='a'||c=='e'||c=='i'||c=='o'||c=='u'||
    c=='A'||c=='E'||c=='I'||c=='O'||c=='U')
    {
        printf("%c is a vowel", c);  // condition true input is vowel
    }
    else
    {
        printf("%c is a consonant", c);  // condition true input is consonant
    }

    return 0;
}
Output
F is a consonant
Method 2
The issue with the previous method was that we were not checking if the user entered a non-alphabet character like ‘3’ or ‘%’ etc. We will see an alternate approach and also handle this non-alphabet case.
Method 2 (Code in C)
Run
#include <stdio.h>

int isLowercaseVowel(int c){
    // returns 1 if char matches any of below
    return (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u');
}

int isUppercaseVowel(int c){
    // returns 1 if char matches any of below
    return (c == 'A' || c == 'E' || c == 'I' || c == 'O' || c == 'U');
}
int main() {
    char c='J';
    
    

    // show error message if c is not an alphabet
   
      
    if (isLowercaseVowel(c) || isUppercaseVowel(c))
        printf("%c is a vowel", c);  
        
    else
        printf("%c is a consonant", c);  

    return 0;
}
Output
J is a consonant
Related Pages
Juggling algorithm for array rotation
 
Balanced Parenthesis Problem
 
Check whether a character is a alphabet or not

Find the ASCII value of a character

Length of the string without using strlen() function

Method 3
The above method has two separate functions of upper case vowels and lowercase vowels we can reduce that down to one single method using an inbuilt function that converts any lowercase case charter to uppercase.
Method 2 (Code in C)
Run
#include <stdio.h>

// single function for both uppercase and lowercase
int isVowel(int c){
    // converts to uppercase if it wasn't already
    c = toupper(c);
    
    // returns true if char matches any of below
    return (c == 'A' || c == 'E' || c == 'I' || c == 'O' || c == 'U');
}
int main() {
    char c='i';
   

    // show error message if c is not an alphabet
    
      
   if (isVowel(c))
        printf("%c is a vowel", c);  
        
    else
        printf("%c is a consonant", c);

    return 0;
}
Output
i is a vowel
