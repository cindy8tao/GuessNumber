import java.util.Random;
import java.util.Scanner;

public class guessNumber {
    
    /**
     * Store random number
     */
    private int randNum;

    /**
     * Store the total score
     */
    private int score;

    /**
     * Read user input
     */
    static Scanner scanner = new Scanner(System.in);

    /**
     * Constructor that initialize the variables
     */
    public guessNumber(){

	this.score = 0;
	this.randNum = 0;

    }

    /**
     * Generate random numbers from 1 to 10
     */
    public void generateRandomNumber(){

	// Generate random number
	Random random = new Random();
	randNum = random.nextInt(10) + 1;
	
	// Debugging (print out the random number)
	System.out.println(randNum);
	
	return;

    }

    /**
     * Compare the user guess with the random number 
     * @param numGuess, number guessed by the user
     * @return true if the number matches
     */
    public boolean guessCorrect(int numGuess){
	return randNum == numGuess;
    }

    /**
     * Game implementation 
     */
    public void game() {
	
	// Initialize variables
	String userGuess = "";
	this.score = 0;
	// Generate random numbers
	this.generateRandomNumber();
	
	// while true ask the user to guess a number
	// if the user number matches the random number then game is over
	while (true) {	    
	    System.out.println("Please guess a number from 1 to 10: ");	    
	    if (scanner.hasNext()) {
		userGuess = scanner.nextLine();
	    }
	    try {
		int numGuess = Integer.parseInt(userGuess);
		// Increase score 
		this.score++;
		if(this.guessCorrect(numGuess)) {
		    System.out.println("GAME OVER");
		    System.out.println("Congrat! You guessed the right number");
		    System.out.println("Total guesses: " + this.score);
		    break;
		}
	    } catch (Exception e) {
		System.out.println("Invalid input, please try again");
	    }
	}
    }

    /**
     * Main method for the game
     * @param args
     */
    public static void main(String[] args) {
	
	// Call the game
	guessNumber guess = new guessNumber();
	guess.game();
	
	// Ask if the user wants to play again
	while(true) {
	    String playAgain = "";
	    System.out.println("Would you like to play again? Y/N");
	    if(scanner.hasNext()) {
		playAgain = scanner.nextLine();		
	    }
	    if(playAgain.equalsIgnoreCase("Y")) {
		guess.game();
	    }
	    else if (playAgain.equalsIgnoreCase("N")) {
		System.out.println("Thank you for playing!");
		break;
	    }
	    else {
		System.out.println("Invalid input, please enter 'Y' or 'N'");
	    }

	}
	
	// Close the scanner 
	scanner.close();
    }

}
