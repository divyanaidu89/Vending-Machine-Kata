
package vendingmachine;
import java.util.Scanner;
public class VendingMachine{

public static void main(String[] args){
        //Initializing variables
	    int COLA = 100; 
	    int CHIPS = 50; 
	    int CANDY = 65;     
	    int quarters, dimes, nickels, pennies;
	    int choice;
	    int money ;
	    int change;
	    double extraCentsTobePaid = 0;
	    boolean correctSelection = true;
	    int continueAgain;
	    
	     //initial output statements
	    do{
		    correctSelection = true;
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
		   System.out.println("You entered: " +money);
		   switch(choice)         
		   {
		        case 1:// Block for COLA          
		        	System.out.println("You chose COLA: 100 cents");
		            extraCentsTobePaid = COLA-money;
		            break;
		             
		        case 2:// Block for CHIPS
		            System.out.println("You chose CHIPS: 50cents");
		            extraCentsTobePaid = CHIPS-money;           
		            break;             
		            
		        case 3: // Block for CANDY
		            System.out.println("You chose CANDY: 65cents");
		            extraCentsTobePaid = CANDY-money;
		            break;
		                                
		        default:
		        	System.out.println("You must enter a selection(item) between 1 and 3. Thank you!");   
		        	correctSelection = false;
		     } 
		     if(correctSelection){
			     if(extraCentsTobePaid ==0){
			         System.out.println("Please take your item, Thank you!");
			     }else if(extraCentsTobePaid > 0){
			         System.out.println("Please pay "+ extraCentsTobePaid +" cents more and take your item");
			         System.out.println("Thank you!");
			     } else if(extraCentsTobePaid < 0){  
			    	 change = (int)(extraCentsTobePaid*(-1)) ;
				     System.out.println("Please take your item, Thank you!");
				     System.out.println("Your change is: " + change + "cents");
				     System.out.println("Take your " + change + " cents as: ");
				      
				     quarters = change/25;
				     change = change % 25;
				     dimes = change/10;
				     change = change % 10;
				     nickels = change/5;
				     change = change % 5;
				     pennies = change;
				     
				     System.out.println(quarters + " quarter(s)");
				     System.out.println(dimes + " dime(s)");
				     System.out.println(nickels + " nickel(s) and");
				     System.out.println(pennies + " pennies");
				     System.out.println("Thank you!");
			   }
		     }
		     System.out.println("Please enter 2 to exit or any other number to select an item again");
		     continueAgain = input.nextInt();
	    }while(continueAgain !=2);
   }
}

