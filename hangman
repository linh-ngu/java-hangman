import java.util.*;

class Main {

  static String[] words = {"blizzard", "glowworm", "haphazard", "awkward", "zigzagging", "stronghold", "xylophone", "oxygen"};

  static String guessWord = words[(int) (Math.random() * words.length)];

  static ArrayList <String> numUnderscores = new ArrayList<String>();
  static ArrayList <String> guessedLetters = new ArrayList<String>();

  public static void main(String[] args) {

    for (int i = 0; i < guessWord.length(); i++) {
      numUnderscores.add("_");
    }

    Scanner in = new Scanner(System.in);

    System.out.println("\nWelcome to Hangman!");

    int count = 0;

    while (true) {
      
      printGameBoard(count);

      System.out.print("\nPlease enter your guess: ");

      char guess = in.next().charAt(0);

      System.out.println("\n--------------------------------");

      boolean found = false;

      String Guess = String.valueOf(guess);

      if (validLetter(guessedLetters, Guess)) {
        System.out.println("\nAlready guessed that letter");
        continue;
      }

      for (int i = 0; i < guessWord.length(); i++) {
        if (guessWord.charAt(i) == guess) {
          numUnderscores.set(i, Guess);
          guessedLetters.add(Guess);
          found = true;
        }
      }

      if (!found) {
        System.out.println("\nNot a correct letter");
        count += 1;
        guessedLetters.add(Guess);
      }

      if (winCondition()) {
        printGameBoard(count);
        System.out.println("\nYou win ^_^");
        break;
      }

      if (loseCondition(count)) {
        printGameBoard(count);
        System.out.println("\nYou lose ;-;");
        break;
      }
    }
    in.close();
  }
  
  public static void printGameBoard(int count) {
    if (count == 0) {
      System.out.println("  ______");
      System.out.println("  |    |");
      System.out.println("  |");
      System.out.println("  |");
      System.out.println("  |");
      System.out.println(" _|_");
      System.out.println("");
      System.out.println(numUnderscores);
    }
    else if (count == 1) {
      System.out.println("  ______");
      System.out.println("  |    |");
      System.out.println("  |    o");
      System.out.println("  |");
      System.out.println("  |");
      System.out.println(" _|_");
      System.out.println("");
      System.out.println(numUnderscores);
    }
    else if (count == 2) {
      System.out.println("  ______");
      System.out.println("  |    |");
      System.out.println("  |    o");
      System.out.println("  |    |");
      System.out.println("  |");
      System.out.println(" _|_");
      System.out.println("");
      System.out.println(numUnderscores);
    }
    else if (count == 3) {
      System.out.println("  ______");
      System.out.println("  |    |");
      System.out.println("  |    o");
      System.out.println("  |   /|");
      System.out.println("  |");
      System.out.println(" _|_");
      System.out.println("");
      System.out.println(numUnderscores);
    }
    else if (count == 4) {
      System.out.println("  ______");
      System.out.println("  |    |");
      System.out.println("  |    o");
      System.out.println("  |   /|\\");
      System.out.println("  |");
      System.out.println(" _|_");
      System.out.println("");
      System.out.println(numUnderscores);
    }
    else if (count == 5) {
      System.out.println("  ______");
      System.out.println("  |    |");
      System.out.println("  |    o");
      System.out.println("  |   /|\\");
      System.out.println("  |   /");
      System.out.println(" _|_");
      System.out.println("");
      System.out.println(numUnderscores);
    }
    else if (count == 6) {
      System.out.println("  ______");
      System.out.println("  |    |");
      System.out.println("  |    o");
      System.out.println("  |   /|\\");
      System.out.println("  |   / \\");
      System.out.println(" _|_");
      System.out.println("");
      System.out.println(numUnderscores);
    }   
  }

  public static boolean winCondition() {
    if (!(numUnderscores.contains("_"))) {
      return true;
    }
    else {
      return false;
    }
  }

  public static boolean loseCondition(int count) {
    if (count == 6) {
      return true;
    }
    else {
      return false;
    }
  }

  public static boolean validLetter(ArrayList<String> guessedLetters, String Guess) {
      if (guessedLetters.contains(Guess)) {
        return true;
      }
      else {
        return false;
      }
  }
}
