# Java-HackerRank
Just My solutions that i wanna document for future using or if i tried to give them some sort of enhancements

the Java loops task which took from me about one whole day thinkin abt it بنت ال*****

just an arithmitic equation that i needed to use loops to identify its solution with the help of computer <img width="707" height="204" alt="java-loops-2" src="https://github.com/user-attachments/assets/385fc7bf-cc7b-45a8-9f99-d9b6e492eb13" />

and thats it in this pic 

its all about the line of 2*b which b is constant all the time and 2 is exponented to a number till reaching n-1 and the barrier there was nothing of what i mentioned yet its just that i need everytime to add the value of that line to the value of it itself again and again and again till reaching the finite state of 2 exponented to n-1 multiplied by b

which is easy now to read cuz i understood it but not easy to think about how to solve this shit at 3 am while cursing the time and ur head 

 whatever...

 i tried to put like static class and just make it return the value at first but i found alot of constraints like otherwise the main function in a method of a class of ur own u cant return the value inside a for loop to represent whats is to be returned from the whole method like in the for loop thats cosidered as a local var there so if i tried to return it outside of that scope like what i did it will just throw a new error at ur face so i dropped that idea after like 2 hours of playing with types of functions and trying to declare a void one and depend on sout only but again i was too stupid at that point

 so when it came to using the main function
 just the solution came easy by just havin the number of iterations in the n var and used the for loop for exponenting 2 by the var in the for loop which starts with zero and ends with n-1 so i dont need to make it again the equation and just in the sout add a to that solution that was tooooooooooooooo easy after u just know how to devide the proplem properly and actually heres the part i enjoyed 



 i just looked at the proplem in a devision of steps 
 the first step was that a is just treated as a constant which just need to be added in the final line so no need to put it in any loop otherwise the main loop of the app itself

 and the line 2exponented to a number till n-1*b is just repeaed so i knew i had to add just this line to itself till it reach its final state bby  just adding a var that holds its value and adding itself again and again "I just made a stupid mistake there where i declared that r inside the loop and it kept givin itself the value of 0 again and again this shitty error was destructive to my mind "
 also i didnt knew taht java doesnt have that ** exponent built in function so i knew about pow method at the the math class which is imported from the java.lang.Math lib.

 so here came the solution and heres the code:





import java.util.*;
import java.io.*;
import java.lang.Math;



class Solution{
    public static void main(String []argh){
        Scanner in = new Scanner(System.in);
        int t=in.nextInt();
        for(int i=0;i<t;i++){
            int a = in.nextInt();
            int b = in.nextInt();
            int n = in.nextInt();
            if (t >= 0 && t<=500)
        {
            if (a >= 0 && a <=50 )
            {
              if(b >= 0 && b <=50)  
              {
                if (n>=1 && n<=15)
                {
                   int r = 0;
                   for (int l = 0 ; l <n; l++)
                    {
                        r = r + (int)(Math.pow(2, l)*b);
                        System.out.print(a+r+" ");
                    
                    } 
                   System.out.println(); 
                }
              }
            }
        }
        }
        in.close();
        
        
    }
}


heres a new solution i found cuz after i thought abt again i  found out that i was right using a void method at the first lines of the code to simplify it and i did it actually and the error i found by declaring r inside a scope of the loop was my fault cuz it was just initialize r again and again with zero so heres the enhanced code from my pov

import java.io.*;
import java.util.*;
import java.lang.Math;


public class Solution {
    public static void getSolution(int a,int b, int n){
    
    int r =0 ;
    
    for(int i = 0; i<n;i++)
    {
        r=(int)(r+Math.pow(2,i)*b);
        System.out.print(a+r+" ");
  
    }
    
}

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        
        int q = in.nextInt();
        for(int i = 0;i<q;i++)
        {
            int a = in.nextInt();
            int b = in.nextInt();
            int n = in.nextInt();
            if (q>=0&&q<=500)
            {
               if (a>=0&&a<=50)
               {
                if(b>=0&&b<=50)
                {
                    if(n>=1&&n<=15)
                    {
                       getSolution(a, b, n); 
                       System.out.println();
                    }
                }
               } 
            }
        }
        in.close();
    }
}
 

