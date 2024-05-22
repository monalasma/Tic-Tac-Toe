# Tic-Tac-Toe
First individual work in .java
```java
import java.util.Scanner;
import java.util.Random;
public class Main {
  public static void main(String[] args) {
    /*
    | |x| |
    |x| | |
    | | |x|
    */
    String [][] board = {
      {"| ", " ","|"," ", " |"," ", " |"},
      { "| ", " ","|"," ", " |"," ", " |"},
      {"| ", " ","|"," ", " |"," ", " |"}
    };
    printGameBoard(board);
    while(true){
      Scanner scanner = new Scanner(System.in);
      System.out.println("Enter your place (1-9): ");
      int numb = scanner.nextInt();
      placeSymbolInBoard(board, numb, "player");
      System.out.println("Don't choose the same place as the other player.");
      Random rand = new Random();
      int otherNumb = rand.nextInt(9) + 1; // the range of numbers
      placeSymbolInBoard(board, otherNumb, "other");
      printGameBoard(board);
    }
  }
  public static void printGameBoard(String [][] board){
    for(String[] row: board){
      for(String element: row){ // takes each value of the row
        System.out.print(element); // prints out the current element
      }
      System.out.println();
    }
  }
  public static void placeSymbolInBoard(String [][] board, int numb, String user){
    String symbol = user.equals("player") ? "X" : "O";
    switch (numb){
      case 1:
        board[0][1] = symbol;
        break;
      case 2:
        board[0][3] = symbol;
        break;
      case 3:
        board [0][5] = symbol;
        break;
      case 4:
        board [1][1] = symbol;
        break;
      case 5:
        board [1][3] = symbol;
        break;
      case 6:
        board [1][5] = symbol;
        break;
      case 7:
        board [2][1] = symbol;
        break;
      case 8:
        board [2][3] = symbol;
        break;
      case 9:
        board [2][5] = symbol;
        break;
      default:
        break;
    }
  }
```

