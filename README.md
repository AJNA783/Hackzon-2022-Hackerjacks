# Hackzon-2022-Hackerjacks
INTRODUCTION  TO  VOTING  SYSTEM
This project is developed for threat free and user oriented Online Voting System. The Online Voting system is made for the people of the country residing around the world and wants to vote for their representative. The election can be conducted in two ways: the paper ballot elections and the automated ballot elections. 
 
SCOPE OF  VOTING SYSTEM
This is a menu driven program based on the automated ballot elections also called electronic voting. Three services have been provided here namely casting the vote, finding the vote count and finding the candidate with the most number of votes. In casting the vote, voters can vote for the political party of their choice among BJP, In Congress, AAP and JDS. We can also find the total vote count of the individual political parties with this system with the help of C coding. Additionally, we also have a feature to find the candidate with maximum number of votes. We get to know the final result of the elections within fraction of seconds with electronic voting.
FEATURES OF VOTING SYSTEM
This is a menu driven program based on voting system. It is a basic project which can be used to elect candidates from the given list and shows the output. This C project consists of collecting votes, showing the results of each vote for each candidate, displaying the leading candidate, and exiting by giving a key value.
In "Cast the vote" section print all the candidate name and choice option to cast the vote.
In "Find Vote Count" section we will get the total number of vote casted in every candidate. If anyone casts a vote to "None of these" Then this vote consider as an invalid vote.
And using "Find Leading Candidate" we get the result as to who is in the leading position. If any two candidates have the same highest vote then we get an error "Warning!!! No-win situation".

SOURCE CODE

#include<stdio.h>

#define CONTENDER_COUNT
#define CONTENDER1 "All India Hindustan Congress Party"
#define CONTENDER2 "Bharatiya Janata Party"
#define CONTENDER3 "Janata Dal (Secular)"
#define CONTENDER4 "Communist Party of India"

int votesCount1=0, votesCount2=0, votesCount3=0, votesCount4=0, invalidvotes=0;

void castVote(){
int choice;    
printf("\n\n ### Cast your vote for the candidate of your preference : ####\n\n");
printf("\n 1. %s", CONTENDER1);
printf("\n 2. %s", CONTENDER2);
printf("\n 3. %s", CONTENDER3);
printf("\n 4. %s", CONTENDER4);
printf("\n 5. %s", "None of These");

printf("\n\n Input your choice (1 - 5) : ");
scanf("%d",&choice);

switch(choice){
    case 1: votesCount1++; break;
    case 2: votesCount2++; break;
    case 3: votesCount3++; break;
    case 4: votesCount4++; break;
    case 5: invalidvotes++; break;
    default: printf("\n Error: Wrong Choice !! Please retry by selecting one of the 5 choices. ");
             //hold the screen
             getchar();
}
printf("\n Thank you for voting !!");
}

void votesCount(){
printf("\n\n ##### Voting Statics ####");
printf("\n %s - %d ", CONTENDER1, votesCount1);
printf("\n %s - %d ", CONTENDER2, votesCount2);
printf("\n %s - %d ", CONTENDER3, votesCount3);
printf("\n %s - %d ", CONTENDER4, votesCount4);
printf("\n %s - %d ", "Invalid Votes", invalidvotes); 
}

void getLeadingCandidate(){
    printf("\n\n  #### Leading Candiate ####\n\n");
    if(votesCount1>votesCount2 && votesCount1>votesCount3 && votesCount1 >votesCount4)
    printf("[%s]",CONTENDER1);
    else if (votesCount2>votesCount3 && votesCount2>votesCount4 && votesCount2 >votesCount1)
    printf("[%s]",CONTENDER2);
    else if(votesCount3>votesCount4 && votesCount3>votesCount2 && votesCount3 >votesCount1)
    printf("[%s]",CONTENDER3);
    else if(votesCount4>votesCount1 && votesCount4>votesCount2 && votesCount4 >votesCount3)
    printf("[%s]",CONTENDER4);
    else
    printf("----- Warning !!! No-win situation----");    
    
    
    
}

int main()
{
int i;
int choice;

do{
printf("\n\n ###### Welcome to Election/Voting 2019 #####");
printf("\n\n 1. Cast the Vote");
printf("\n 2. Find Vote Count");
printf("\n 3. Find leading Contender");
printf("\n 0. Exit");

printf("\n\n Please enter what you would wish to do : ");
scanf("%d", &choice);

switch(choice)
{
case 1: castVote();break;
case 2: votesCount();break;
case 3: getLeadingCandidate();break;
default: printf("\n You have chosen to exit");
}
}while(choice!=0);

//hold the screen
getchar();

return 0;
}

OUTPUT SCREENSHOTS
 
 




CONCLUSION
Crucial points about the Online Voting System:
i.	Provision of improved voting services to the voters to the voters through fats, timely and convenient voting.
ii.	Requires less number of staff during the election.
iii.	This system is a lot easier to independently moderate the elections and subsequently reinforce its transparency and fairness.
iv.	Less capital, less labour intensive.
v.	Increased number of voters as this system is more convenient and easier to vote, especially those abroad.













