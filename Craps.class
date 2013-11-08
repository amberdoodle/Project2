import java.util.Scanner;
import java.util.Arrays;
  
public class Craps
{
  private static final int MIN_ROLL = 2;         // minimum value of a roll
  private static final int MAX_ROLL = 12;        // maximum value of a roll
  private static final int MAX_LENGTH = 36;      // maximum length of bars
  
   /**
   * main method:
   * ask the user how many dice rolls to make during this run
   * count occurances for each value of the throw of the dice
   * and draw a horizontal and vertical histogram of the counts
   */
  
  public static void main(String[] args)
  {
    // step 1:
    // declare an int array named "counts" to count dice roll occurences
    // ignore the 0th and 1st array elements (those values can't occur)
    int [] counts = new int [MAX_ROLL + 1];
    int [] countsLimited = Arrays.copyOfRange (counts, MIN_ROLL, MAX_ROLL + 1);
    //Uses the imported method from the Arrays to copy elements 2-13 to the new array

    // step 2:
    // initialize all of the values in the array to 0
    
    Arrays.fill (countsLimited, 0); 
    //Uses imported method from Arrays to initialize all values with 0
    //The source code for Arrays.fill creates a for loop that sets all integers to 0 using the
    //.length method and increments until the final array element is reached
    
   // instantiate two dice: myDie1 and myDie2
    Die myDie1 = new Die();
    Die myDie2 = new Die();
    
    // ask user for the number of rolls to make during this run
    Scanner scan = new Scanner(System.in);
    System.out.println("How many dice rolls do you want?");
    int total = scan.nextInt();

    // step 3:
    // roll the two dice and count the total of the two rolls n times
    for (int n = 1; n <= total; n++){
      int sum = myDie1.roll() + myDie2.roll(); 
    }
   
    // step 4:
    // print out the estimated probabilities of win, lose, and roll again

  /** 
     win = 7 or 11
     prob win = (#7 + #11)/total
     lose = 2, 3, or 12
     prob lose = (#2 + #3 + #12)/total
     roll again = 4, 5, 6, 8, 9, or 10
     prob roll again = (#4 + #5 + #6 + #8 + #9 + #10)/total
     */
    int win = countsLimited [7] + countsLimited[11];
    int lose = countsLimited [2] + countsLimited [3] + countsLimited [12];
    int ragain = countsLimited [4] + countsLimited [5] + countsLimited [6] + countsLimited [8] + 
      countsLimited [9] + countsLimited [10];
    //get # of times each roll occurs
    
    float pwin = (float) win/(float) total;
    float plose = (float) lose/(float) total;
    float pragain = (float) ragain/(float) total;
    
    System.out.println ("Estimated probablities for outcome of the first roll");
    System.out.println ("Win:" + pwin);
    System.out.println ("Lose:" + plose);
    System.out.println ("Roll again:" + pragain);
 
    // step 5:
    // instantiate an object of the Histogram class and 
    // call its two draw methods to draw the two histograms
    // with the array to be drawn, the indices of valid data,
    // and the maximum length of the bars in the histogram
 
  }
}
