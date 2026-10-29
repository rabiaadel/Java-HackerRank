This task isnt by far difficult it just had two tricks that i want to document for future using maybe 

heres the task
<img width="772" height="813" alt="image" src="https://github.com/user-attachments/assets/3e9be5c6-0f47-4a5c-941c-155012647a66" />

the first challenge is that when u open a scanner dont open it in a loop dont be dump just open it outside of the loop and then take the input inside the loop 
the second chaleenge that took time from me is how to mention  a variable i ndeclared inside the try function into the catch exception function and i cant declare it outside the try function 
cuz i make loop on it 
so the trick was just to get it from the object of the scanner it self with the function next(); which holds the cariable till givin it a new value thats an info that i didnt notice before and i wanted to document it


heres my code 

import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) 
    {
        Scanner in = new Scanner(System.in);
        int Iterations = in.nextInt();
        for(int i = 1; i<=Iterations; i++)
        {
            try
            {
            long x = in.nextLong();
            System.out.printf("%d can be fitted in:%n",x);
            if(x>=-128 && x<=127)System.out.println("* byte");
            if(x>=-32768 && x<=32767)System.out.println("* short");
            if(x>=-Math.pow(2,31) && x<=Math.pow(2,31)-1)System.out.println("* int");
            if(x>=-Math.pow(2,63) && x<=Math.pow(2,63)-1)System.out.println("* long");
            }
            catch(Exception Exception)
            {
                System.out.println(in.next()+" can't be fitted anywhere.");
            }
        }
        in.close();
    }
}
