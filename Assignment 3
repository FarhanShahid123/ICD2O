import java.util.Scanner; // Import Scanner for user input

public class Assignment3 { // Main class

    public static void main(String[] args) { // Main method
        Scanner input = new Scanner(System.in); // Create Scanner to take input

        int playerWins = 0, computerWins = 0, ties = 0; // Counters for wins, losses, and ties

        // Ask the player how many games they want to play
        System.out.println("How many games do you want to play?");
        int totalGames = input.nextInt(); // Store the number of games

        for (int i = 0; i < totalGames; i++) { // Loop for each game
            // Ask the player for their choice
            System.out.println("\nEnter your choice: r (rock), p (paper), or s (scissors):");
            char playerChoice = input.next().toLowerCase().charAt(0); // Read player's choice

            // Check if the input is valid
            if (playerChoice != 'r' && playerChoice != 'p' && playerChoice != 's') {
                System.out.println("Invalid choice! Try again."); // Print error message
                i--; // Don't count this round
                continue; // Restart the loop
            }

            // Generate the computer's random choice (0 = rock, 1 = paper, 2 = scissors)
            int random = (int) (3 * Math.random());
            char computerChoice = (random == 0) ? 'r' : (random == 1) ? 'p' : 's';

            // Show the player what the computer picked
            System.out.println("Computer chose: " + computerChoice);

            // Check who won
            if (playerChoice == computerChoice) {
                System.out.println("It's a tie!"); // Both chose the same
                ties++; // Add to ties
            } else if ((playerChoice == 'r' && computerChoice == 's') || // Rock beats scissors
                       (playerChoice == 'p' && computerChoice == 'r') || // Paper beats rock
                       (playerChoice == 's' && computerChoice == 'p')) { // Scissors beat paper
                System.out.println("You win!"); // Player wins
                playerWins++; // Add to player's wins
            } else {
                System.out.println("Computer wins!"); // Computer wins
                computerWins++; // Add to computer's wins
            }
        }

        // Show the final results after all games
        System.out.println("\n--- Final Results ---");
        System.out.println("You won: " + playerWins); // Player's wins
        System.out.println("Computer won: " + computerWins); // Computer's wins
        System.out.println("Ties: " + ties); // Total ties
        System.out.println("Goodbye!"); // Say goodbye

        input.close(); // Close the scanner
    }
}
