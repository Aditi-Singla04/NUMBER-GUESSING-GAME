#include <bits/stdc++.h>
using namespace std;

int main()
{
    cout<<"\t\t\tWelcome to number guessing game!";
    cout<<"\n\nPlease choose from two levels:\n1.Easy\t\t2.Hard";
    cout<<"\nFor easy you have 10 chances and for hard you have 5 chances.";
    cout<<"\n\nType 1 for easy and 2 for hard:";
    int x;
    cin>>x;
    srand (time(0));
    int number=1+(rand()%100);
    int choice;
    if(x==1)
    {
        for(int i=1;i<=10;i++)
        {
            cout<<"\nPlease enter your chosen number:";
            cin>>choice;
            if(choice<number)
            {
                cout<<"\nYour chosen number "<<choice<<" ,is less than generated number.\nPlease choose increased number.";
                cout<<"\nYou have "<<10-i<<" chances left.\n";
            }
            
            if(choice>number)
            {
                cout<<"\nChosen number, "<<choice<<" ,is more than generated number.\nPlease choose decreased number.";
                cout<<"\nYou have"<<10-i<<" chances left.\n";
            }
            
            if(choice==number)
            {
                cout<<"Congratulations! You completed the game in "<<i<<" chances!";
                break;
            }
            
            if(i==10 && choice!=number)
            {
                cout<<"OOPS! You lost! You can try again if u want.";
                break;
            }
        }
    }    
        
    if(x==2)
    {
        for(int i=1;i<=5;i++)
        {
            cout<<"\nPlease enter your chosen number:";
            cin>>choice;
            if(choice<number)
            {
                cout<<"\nYour chosen number "<<choice<<" ,is less than generated number.\nPlease choose increased number.";
                cout<<"\nYou have "<<5-i<<" chances left.\n";
            }
            
            if(choice>number)
            {
                cout<<"\nChosen number, "<<choice<<" ,is more than generated number.\nPlease choose decreased number.";
                cout<<"\nYou have"<<5-i<<" chances left.\n";
            }
            
            if(choice==number)
            {
                cout<<"Congratulations! You completed the game in "<<i<<" chances!";
                break;
            }
            
            if(i==5 && choice!=number)
            {
                cout<<"OOPS! You lost! You can try again if u want.";
                break;
            }
        }
    }
}
