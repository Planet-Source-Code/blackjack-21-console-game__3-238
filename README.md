<div align="center">

## blackjack 21: console game


</div>

### Description

BLACKJACK VS THE COMP, My code probably isn't that great, but it works...
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[N/A](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/empty.md)
**Level**          |Intermediate
**User Rating**    |4.5 (9 globes from 2 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Games](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/games__3-13.md)
**World**          |[C / C++](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/blackjack-21-console-game__3-238/archive/master.zip)





### Source Code

```
//This game simulates a simplified version of the card game 21
#include <iostream.h>//include neccesary libraries
#include <stdlib.h>
#include <time.h>
int you1,you2,you3, c1, c2, c3,ans,you,comp,ans2,youpoint,comppoint,drawpoint;
//you1,2,3 are random #'s for player, C1,2,3 are random #'s for computer
// ans is # of cards, you and comp are total scores, youpoint compoint and drawpoint are total points for each
char yesno;//used to loop program
int main()
{
yesno='y';
comppoint=0;
youpoint=0;
drawpoint=0;//declares variable starting point
cout << "Ryan Fogarty" << endl << "Lab 21 Game" <<endl<<"Nov, 11, 1999"<<endl<<"This Program Simlulates the Card Game 21\n";
while ((yesno=='y')||(yesno=='Y'))// loop
{
	cout <<"How many cards do you want?\n";
	cin >> ans;
	srand (time(NULL));// generates random #'s for comp and player
	you1 =(rand()%(10)) +1; //from 1 to 10
	you2 =(rand()%(10)) +1; //from 1 to 10
	you3 =(rand()%(10)) +1; //from 1 to 10
	c1 =(rand()%(10)) +1; //from 1 to 10
	c2 =(rand()%(10)) +1; //from 1 to 10
	c3=(rand()%(10)) +1; //from 1 to 10
	if (ans==1)
		{
		cout <<"You: "<< you1 <<endl;
		cout <<"Computer: "<<c1<<" "<<c2<<" "<<c3<<endl;
		you = you1 ;
		comp = c1 + c2 + c3;
		}
	else if (ans==2)
		{
		cout <<"You: "<< you1 <<" "<<you2<<endl;
		cout <<"Computer: "<<c1<<" "<<c2<<" "<<c3<<endl;
		you = you1 + you2;
		comp = c1 + c2 + c3;
		}
	else if (ans==3)
		{
		cout <<"You: "<< you1 <<" "<<you2<<" "<<you3<<endl;
		cout <<"Computer: "<<c1<<" "<<c2<<" "<<c3<<endl;
		you = you1 + you2 +you3;
		comp = c1 + c2 + c3;
		}//if statement used to tell how many cards were chosen
		if ((you > comp)&&(you<=21)||(comp>21))
			{
			cout <<"I have " <<comp<<" and you have "<<you<<" so you win."<<endl;
			youpoint++;
			}
		else if ((comp > you)&&(comp<=21)||(you>21))
			{
			cout <<"I have " <<comp<<" and you have "<<you<<" so I win."<<endl;
			comppoint++;
			}
		else if ((comp == you))
			{
			cout <<"I have " <<comp<<" and you have "<<you<<" so we draw."<<endl;
			drawpoint++;
			}// statement tells who won and adds on total points
		cout <<"Would you like to play again? (Y/N)?";//to restart loop or not
		cin >> yesno;
		cout << endl;
	}
	cout << "\nComputer Wins = "<<comppoint<<endl;
	cout << "Your Wins = "<< youpoint<<endl;
	cout << "Draws = "<< drawpoint<< endl;// shows total amount of points
	return 0;
}
```

