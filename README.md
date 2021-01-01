# Sprintf Function 
 Sprintf Function in Assembly
 
* To implement the function, we must first parse the string, meaning we store what is between quotations into a character array known as “format”. 
* A function known as “ProcessInput” that takes whatever is in the input string, and looks for the possible occurrences that could occur. It takes whatever is in between quotations, and stores it in the format string. If a space is found that is not in between the quotations, the ProcessInput loop will iterate again, meaning that it will ignore its presence. If a comma is found, that means that its most likely in between the parameters, or the values that the sprintf is meant to take, meaning that those values will be stored. 
* These stored values are placed in registers $t5-$t9, so if the character ‘a’ is found that will automatically correspond to $t5 in our code, and so forth. Once the appropriate value is located, it will be stored in the stack, in the correct order. 
* To do that, we had to store the values normally, and then reverse the stack. All that is left now is to store the values in the character array known as the outbuf, as the format string, and parameters have been passed as arguments to the sprintf function. The sprintf function takes the format character array, and scans it for a % sign, once that's found its send to a function named findfunct, where it looks at the corresponding byte, and sends it straight to the appropriate function. 
* The function implements the conversion needed, and stores the output in the outbuf character array. Once the format has been fully iterated through, it returns back to the main where the outbuf will be printed, and the entire program will end.

# Contributors
- Ramy ElGedni
