///ROCK PAPER SCISSOR SHOOT!///

#include <iostream>
#include <stdlib.h>
#include <ctime>
#include <conio.h>

using namespace std;

int main()
{
    string player_name;
    cout << "Welcome to ROCK PAPER SCISSOR SHOOT.....Enter Your Name:" ;
    cin >> player_name ;
    int rounds;
    cout << player_name << " We will being playing best out of 7 rounds so enter 7 to proceed :" ;
    cin >> rounds;
    int player_score = 0, computer_score = 0  ;
    for(int round= 0; round<=rounds; round++)
    {

        int player_choice,computer_choice;
        cout << "Round No: " << round << "/" << rounds << endl;
        cout << player_name << "'s Score = " << player_score << endl;
        cout << "Computer Score = " << computer_score << endl;
        cout << "1. Rock" << endl;
        cout << "2. Paper" << endl;
        cout << "3. Scissor" << endl;
        do{

            cout << " Pick your choice: " ;
            cin >> player_choice ;
        }while(player_choice != 1 && player_choice != 2 && player_choice != 3);
        srand(time(0));
        computer_choice = (rand()%3)+1;
        if(player_choice == 1 && computer_choice ==3)
        {
            cout << "Player Wins Round!" << endl;
            player_choice+= 1;}

        else if (player_choice == 2 && computer_choice ==1)
        {
            cout << "Player Wins Round!" << endl;
            player_score++;}
       else if(player_choice == 3 && computer_choice ==2)
       {
           cout << "Player Wins Round!" ;
           player_choice ++;}
       else if (player_choice == computer_choice)
       {
           cout << "Tied" << endl;
       }
       else
       {
           cout << "Computer Wins Round!" << endl;
           computer_choice ++;
       }
        cout << " Press any key to continue..." << endl;
        getch();

    }
    if(computer_score == player_score)i
    {
        cout << "Game is a Tied" << endl;
    }
    else if (player_score > computer_score)
    {
        cout << player_name << " You Won! "  << endl;


        cout <<player_score <<player_score<<endl;

        cout<<"\ndo you want to repeat<y or n>?\n";






    }

    return 0;
}
