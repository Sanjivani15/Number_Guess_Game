# Number_Guess_Game
package Game_Number;
import java.util.Scanner;
import java.util.Random;


public class Number_Guess {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();
        
        int target=random.nextInt(100)+1;
        int attempts = 0;
        
        System.out.println("Welcome to Guess Number Game");
        System.out.println("You Will Be Asked To Guess A Number To Win The Game");
        System.out.println("You have Maximum 5 Attempt Limit");
        
      
        
        
        while(attempts<5){
            System.out.print("Enter your guess number between 1 and 100 ");
            int guess = scanner.nextInt();
            attempts++;
            
            if (guess < target) {
                System.out.println("Your Guess Number is Smaller");
            } else if (guess > target) {
                System.out.println("Your Guess Number is Greater");
            } else {
                System.out.println("OOhhOO!, Your Number is Correct. You Win the Game! " + target
                		+ " in " + attempts + " guesses.");
                break;
            }
        } 
        
        if (attempts==5) {
        	System.out.println("Sorry, you have used all your attempts.The correct number was:"+target);
        }
        
        scanner.close();
    }
}
