package vendingmachine;
import java.util.Scanner;

public class NewClass {
    
                 public static void main(String[] args){
                          //Initializing variables
    int COLA = 100; 
    int CHIPS =50; 
    int CANDY = 65; 
    
    int quarters, dimes, nickels, pennies;
    int choice;
    int money ;
    int amount;
                           //initial output statements
    System.out.println("VENDING MACHINE");
    System.out.println("Press 1 for Cola--$1.00");
    System.out.println("Press 2 for Chips--$0.50");
    System.out.println("Press 3 for Candy--$0.65");
    
    System.out.println("Please enter your selection.");
    Scanner input = new Scanner(System.in);
    choice = input.nextInt();
     
                           //user input
       System.out.println("Please enter your amount you have paid(in cents):");
        
        money = input.nextInt();
        
    switch(choice)
         
    {
        case 1:            // Block for COLA
             
            System.out.println("You entered: " +money);
            System.out.println("You chose COLA: 100 cents");
            amount = money - COLA;
            double k=CHIPS-money;
            if(amount==0){
                System.out.println("Please take your item, Thank you!");
            }else if(amount<0){
                System.out.println("Please pay"+" "+k+ " "+ "cents more and take your item");
                System.out.println("Thank you!");
            } else if(amount>0){             
            System.out.println("Please take your item, Thank you!");
            System.out.println("Your change is: " + amount + "cents");
            System.out.println("Take your " +amount + " cents as: ");
             
            quarters = amount/25;
            amount = amount % 25;
            dimes = amount/10;
            amount = amount % 10;
            nickels = amount/5;
            amount = amount % 5;
            pennies = amount;
             
            System.out.println(quarters + " quarter(s)");
            System.out.println(dimes + " dime(s)");
            System.out.println(nickels + " nickel(s) and");
            System.out.println(pennies + " pennies");
            System.out.println("Thank you!");
            }
            break;
             
        case 2:       // Block for CHIPS
             
            System.out.println("You entered: " +money);
            System.out.println("You chose CHIPS: 50cents");
            amount = money - CHIPS;
            double j=CHIPS-money;
            if(amount==0){
                System.out.println("Please take your item, Thank you!");
            }else if(amount<0){
                System.out.println("Please pay"+" "+j+ " "+ "cents more and take your item");
                System.out.println("Thank you!");
            } else if(amount>0){
            System.out.println("Your change is: " + amount + " cents");
            System.out.println("Take your " +amount + " cents as: ");
             
            quarters = amount/25;
            amount = amount % 25;
            dimes = amount/10;
            amount = amount % 10;
            nickels = amount/5;
            amount = amount % 5;
            pennies = amount;
             
            System.out.println(quarters + " quarter(s)");
            System.out.println(dimes + " dime(s)");
            System.out.println(nickels + " nickel(s) and");
            System.out.println(pennies + " pennies");
            System.out.println("Thank you!");
            }
             
            break;
             
        case 3:            //Block for CANDY
                   System.out.println("You entered: " +money);
            System.out.println("You chose CANDY: 65cents");
            amount = money - CANDY;
            double i=CANDY-money;
            if(amount==0){
                System.out.println("Please take your item, Thank you!");
            }else if(amount<0){
                System.out.println("Please pay"+" "+i+ " "+ "cents more and take your item");
                System.out.println("Thank you!");
            } else if(amount>0){
            System.out.println("Your change is: " + amount + " cents");
            System.out.println("Take your " +amount + " cents as: ");
             
            quarters = amount/25;
            amount = amount % 25;
            dimes = amount/10;
            amount = amount % 10;
            nickels = amount/5;
            amount = amount % 5;
            pennies = amount;
             
            System.out.println(quarters + " quarter(s)");
            System.out.println(dimes + " dime(s)");
            System.out.println(nickels + " nickel(s) and");
            System.out.println(pennies + " pennies");
            System.out.println("Thank you!"); }
             
            break;
             
                    
        default:
            System.out.println("You must enter a selection between 1 and 3. Thank you!");
            
}

                 }
}
