# Task01
#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    srand(time(0)); 

    int randomNumber = rand() % 100 + 1; 
    int userNumber;
    int attempts = 0;

    do {
        std::cout << "Guess the number: ";
        std::cin >>userNumber;
        attempts++;

        if (userNumber > randomNumber) {
            std::cout << "Too high! Try again.\n";
        } else if (userNumber< randomNumber) {
            std::cout << "Too low! Try again.\n";
        } else {
            std::cout << "Congratulations! You guessed the correct number in " << attempts << " attempts.\n";
        }
    } while (userNumber != randomNumber);

    return 0;
}
