# Rock-paper-scissors-using-C
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int playerChoice, computerChoice;
 
    srand(time(NULL));

    printf("Enter 0 for Rock, 1 for Paper, or 2 for Scissors: ");
    scanf("%d", &playerChoice);

    computerChoice = rand() % 3;

    printf("You chose: ");
    if (playerChoice == 0) printf("Rock\n");
    else if (playerChoice == 1) printf("Paper\n");
    else printf("Scissors\n");

    printf("Computer chose: ");
    if (computerChoice == 0) printf("Rock\n");
    else if (computerChoice == 1) printf("Paper\n");
    else printf("Scissors\n");

    if (playerChoice == computerChoice) {
        printf("It's a tie!\n");
    } else if ((playerChoice == 0 && computerChoice == 2) ||
               (playerChoice == 1 && computerChoice == 0) ||
               (playerChoice == 2 && computerChoice == 1)) {
        printf("You win!\n");
    } else {
        printf("Computer wins!\n");
    }

    return 0;
}
