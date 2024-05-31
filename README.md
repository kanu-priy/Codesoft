#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std

int main()
{
    // Generate a random secret number between 1 and 100
    srand(time(0));
    int secretNumber = rand() % 100 + 1;

    int guess;
    int attempts = 0;
    

    cout << "Welcome to the Number Guessing Game!" << endl;
    cout << "I have selected a secret number between 1 and 100." << endl;
    cout << "Try to guess it!" << endl;

    while (true) 
    {
        cout << "Enter your guess: ";
        cin >> guess;
        attempts++;

        if (guess == secretNumber)
        {
            cout << "Congratulations! You guessed the correct number in " << attempts << " attempts." << endl;
            break;
        }
        else if (guess < secretNumber)
        {
            cout << "Too low! Try a higher number." << endl;
        }
        else
        {
            cout << "Too high! Try a lower number." << endl;
        }
    }

    return 0;
}
