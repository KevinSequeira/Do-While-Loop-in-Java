# Do-While-Loop-in-Java
Hey people. Here's an example program demonstrating how the 'Do-While' loop works in Java.

001) Many a time, during real-world coding, you'll need to run the code within
     the 'while' loop at least once, irrespective of whether the condition
     within the parenthesis is met.
002) So Java provides us with a work-around in the form of the 'do-while' loop.
     The loop looks like this in it's general form:

do{
	//statements;
} while(conditions);

003) Check out the following code that demonstrates the working of a 'do-while'
     loop:

import java.util.Scanner;

public class doWhileLoop {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		Scanner scanner = new Scanner(System.in);
		System.out.print("Number 1: ");
		int a = scanner.nextInt();
		System.out.print("Number 2: ");
		int b = scanner.nextInt();
		
		float result;
		byte choice;
		
		do{
		
			System.out.println("");
			System.out.println("What would like to do?");
			System.out.println("1 : Addition");
			System.out.println("2 : Subtraction");
			System.out.println("3 : Multiplication");
			System.out.println("4 : Division");
		
			System.out.print("Enter your choice: ");
			choice = scanner.nextByte();
			System.out.println("");
			
			switch(choice){
			
			case 1:
				result = a + b;
				System.out.println(a + " plus " + b + " is " + result);
				break;
				
			case 2:
				result = a - b;
				System.out.println(a + " minus " + b + " is " + result);
				break;
				
			case 3:
				result = (float) a * b;
				System.out.println(a + " into " + b + " is " + result);
				break;
				
			case 4:
				result = (float) a / b;
				System.out.println(a + " divided by " + b + " is " + result);
				break;
			
			default:
				System.out.println("Please enter any one of the above given options");
				
			}
			
		} while((choice < 1) || (choice > 4));

	}

}

004) Let's analyze the output of the above given code. When the code is executed
     we are requested to enter the two numbers. Let's for example enter 2 and 22.
005) Next, we're requested to choose the operation we want to perform using these
     two numbers. Here's how the output looks:

Number 1: 2
Number 2: 22

What would like to do?
1 : Addition
2 : Subtraction
3 : Multiplication
4 : Division
Enter your choice: 

006) Here, you can see that the do-while loop has executed the statements
     immediately following the 'do' keyword atleast once. Let's say, I then enter
     '7' as a choice. What happens?
007) The 'choice' is first checked in the switch statement, the intended code is
     run accordingly, and then the following 'while' statement checks for the
     conditions. In this case, the condition is met [ choice < 1 or choice > 4 ].
008) As the condition is met, the program control is transferred back to the
     start of the loop. Thenceforth, the loop works as a traditional 'while'
     loop, until the condition returns a 'false' Boolean equivalent.

009) Here's how the final output looks like:

Number 1: 2
Number 2: 22

What would like to do?
1 : Addition
2 : Subtraction
3 : Multiplication
4 : Division
Enter your choice: 7

Please enter any one of the above given options

What would like to do?
1 : Addition
2 : Subtraction
3 : Multiplication
4 : Division
Enter your choice: 3

2 into 22 is 44.0
