# Elevens-Lab-Activity7

1. What items would be necessary if you were playing a game of Elevens at your desk (not on the
computer)? You would need the deck of cards, 11 card slots, a discard pile

List the private instance variables needed for the ElevensBoard class.

number of games played
Number of games won
Board size


2. Write an algorithm that describes the actions necessary to play the Elevens game.

Shuffle deck, deal deck for 11 cards, any two cards that add to 11 remove and replace with
To from the top of deck, if there are 3 different face cards, remove them and replace with
3 cards from top of deck.

3. Now examine the partially implemented ElevensBoard.java file found in the Activity7
Starter Code directory. Does the ElevensBoard class contain all the state and behavior
necessary to play the game?
It does contain everything needed to play eleven

4. ElevensBoard.java contains three helper methods. These helper methods are private
because they are only called from the ElevensBoard class.

a. Where is the dealMyCards method called in ElevensBoard?


In the constructor of ElevenBoard
In the newGame function.



b. Which public methods should call the containsPairSum11 and containsJQK
methods?


anotherPlayIsPossible
isLegal



c. It’s important to understand how the cardIndexes method works, and how the list that it
returns is used. Suppose that cards contains the elements shown below. Trace the execution
of the cardIndexes method to determine what list will be returned. Complete the diagram
below by filling in the elements of the returned list, and by showing how those values index
cards. Note that the returned list may have less than 9 elements.

0,1,3,6,7

![My image](https://bsimps3.github.io/Elevens-Lab-Activity7/cards.png)

d. Complete the following printCards method to print all of the elements of cards that are
indexed by cIndexes.
    public static printCards(ElevensBoard board) {
    List<Integer> cIndexes = board.cardIndexes();
    Card temp;
    for(int item : cIndexes)
    {
      temp = cards.get(item);
      System.out.println(temp.toString());
    }
  
    }
  
  
  e. Which one of the methods that you identified in question 4b above needs to call the
      cardIndexes method before calling the containsPairSum11 and containsJQK
      methods? Why? anotherPlayIsPossible because if the indexes are all null then the game cant provide new cards and therefore doesn't add more cards.
