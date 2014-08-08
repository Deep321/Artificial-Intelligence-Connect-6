//Deep Prasad - #1000928240 - Connect 6 AI Algorithms
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
//int scorecpu(char ** board, int n, int *row, int *col, char colourcpu);
//int scorehuman(char ** board, int n, int *row, int *col, int lcurr, char temp);

void intial(char **board,int n)
{
    int i, j;

    for(i = 0; i < n; i++)
    {    for(j = 0; j < n; j++)
        {  board[i][j] = 'U';}
    }
}

void printBoard(char **board, int n)
{
    int i, j;

    for(i = 0; i < n; i++)
    {    for(j = 0; j < n; j++)
        {  printf("%c", board[i][j]);}
    printf("\n");
    }

}

/*int checkval(char *st)
{
    int ran = 1;
    char temp;

printf("Enter stone (B|W): ");
scanf(" %c", &temp);

    *st = temp;    

if (*st != 'B' && *st != 'W')
        { ran = 0; }
            //printf("ran and st is %d %c\n", ran, *st);
return ran;
} */

int checkrun(char**board, int n)
{

int i, j;

    int ran = 0;
    char temp;
    
        for(i = 0; i < n; i++)
        {    for(j = 0; j < n; j++)
            { if (board[i][j] == 'U')
                { ran = 1; }
                
            }
        }
    //printf("ran is %d\n", ran);
    //if (ran == '0')
    
return ran;
}            
                
int checkpos(int *row, int *col)
{    int row1, col1;
    int ran2 = 1;
printf("Enter an occupied position to check for contiguous stones (ROW COL): ");
scanf("%d %d", &row1, &col1);
    *row = row1;
    *col = col1;
//printf("row is %d col is %d\n", *row, *col);    
if (*row == - 1 && *col == -1)
{ 
ran2 = 0; 
}

return ran2;
}

int checkinput (char *p) 

{   char temp; 
 
    *p = temp; 
    if (*p == 'E') 
        return 0; 
    else 
        return 1; 
}

int findLongest(char **board, int n, int row, int col)
    {
        int i,j;
        char temp;
        int dlength = 1;
        int dlength2 = 1;
        int vlength = 1;;
        int hlength = 1;
        int longest = 1;
            
            temp = board[row][col];    
        
            //counting positive diagonal
            for (i = row - 1, j = col + 1; i >= 0 && i < n && j >= 0 && j < n; i--, j++)
            {
                    if (board[i][j] == temp)
                        { 
                            dlength++; 
                            //printf("%d\n",dlength); 
                        }
                        else 
                            break;    
            }
            
            //counting negative diagonal
            for (i = row + 1, j = col - 1; i >= 0 && i < n && j >= 0 && j < n; i++, j--)
            {
                if (board[i][j] == temp)
                        { 
                            dlength++; 
                            //printf("%d\n",dlength); 
                        }
                        else 
                            break;     
            }
            
            
            
            longest = dlength;
    
                                                            //counting positive diagonal2
                                                            for (i = row -1, j = col -1; i >= 0 && i < n && j >= 0 && j < n; i--, j--)
                                                            {
                                                                if (board[i][j] == temp)
                                                            { 
                                                                dlength2++; 
                                                                //printf("%d\n",dlength2); 
                                                            }
                                                            else 
                                                                break; 
                                                                    }
                                                        
                                            
                                                            //counting negative diagonal2
                                                            for (i = row + 1, j = col + 1; i >= 0 && i < n && j >= 0 && j < n; i++, j++)
                                                            {
                                                                if (board[i][j] == temp)
                                                            { 
                                                                dlength2++; 
                                                                //printf("%d\n",dlength2); 
                                                            }
                                                            else 
                                                                break; 
                                                            }            
                                                            
                                                            
                                                            if(dlength2>longest)
                                                            {
                                                                longest = dlength2;
                                                            }
            
                        
            //counting positive horizontal
            for (i = row, j = col + 1; i >= 0 && i < n && j >= 0 && j < n; j++)
            {
            
                        if (board[i][j] == temp)
                        { 
                            hlength++; 
                            //printf("%d\n",hlength); 
                        }
                        else 
                            break; 

            }
            //counting negative horizontal
            for (i = row, j = col - 1; i >= 0 && i < n && j >= 0 && j < n; j--)
            {            
                    if (board[i][j] == temp)
                        { 
                            hlength++; 
                            //printf("%d\n",hlength); 
                        }
                        else 
                            break; 
            }
            
            if(hlength>longest)
                longest = hlength;
            //printf("%d",longest);

                                                            
                                                                                                                                //counting positive vertical
                                                                                                                                for (i = row + 1, j = col; i >= 0 && i < n && j >= 0 && j < n; i++)
                                                                                                                                {        
                                                                                                                                        if (board[i][j] == temp)
                                                                                                                                        { 
                                                                                                                                            vlength++; 
                                                                                                                                            //printf("%d\n",vlength); 
                                                                                                                                        }
                                                                                                                                        else 
                                                                                                                                            break; 
                                                                                                                                }
                                                                                                                                //counting negative vertical
                                                                                                                                for (i = row - 1, j = col; i >= 0 && i < n && j >= 0 && j < n; i--)
                                                                                                                                {
                                                                                                                                        if (board[i][j] == temp)
                                                                                                                                        { 
                                                                                                                                            vlength++;
                                                                                                                                            //printf("%d\n",vlength); 
                                                                                                                                        }
                                                                                                                                        else 
                                                                                                                                            break; 
                                                                                                                                }
                                                                                                                                
                                                                                                                                if(vlength > longest)
                                                                                                                                    longest = vlength;
            
            
    //printf("findlongest %c\n", temp);
    //printf("%d\n", longest);
    return longest;            
}                                                                                


                                                                                                                    void findwinner(char **board, int n, int row, int col)
                                                                                                                    {
                                                                                                                        int length = 0;
                                                                                                                        int i, j;
                                                                                                                        char temp2='U';
                                                                                                                            
                                                                                                                        for(i = 0; i <= 6; i++)
                                                                                                                        {    
                                                                                                                            for(j = 0; j < n; j++)
                                                                                                                            { 
                                                                                                                                int templ = findLongest(board, n, i, j); 
                                                                                                                                if (templ >= 6)
                                                                                                                                { 
                                                                                                                                    length = templ; 
                                                                                                                                    //printf("temp2 %c i %d j %d\n", temp2, i, j);
                                                                                                                                    temp2 = board[i][j];
                                                                                                                                    
                                                                                                                                    if (temp2 == 'W')
                                                                                                                                        {printf("White wins.\n"); return;}
                                                                                                                                    else if (temp2 == 'B')
                                                                                                                                            {printf("Black wins.\n");return;}
                                                                                                                                }
                                                                                                                
                                                                                                                            }
                                                                                                                        }
                                                                                                                        
                                                                                                                        printf("No winner so far.\n");
                                                                                                                    }
                                                                                                                    
                                                                                                                    
                                                                                                                    int findwinnerres(char **board, int n)
                                                                                                                    {
                                                                                                                        int findtemplongest;
                                                                                                                        int i,j;
                                                                                                                    
                                                                                                                        for(i = 0; i < n; i++)
                                                                                                                            {    for(j = 0; j < n; j++)
                                                                                                                                { if (board[i][j] == 'B' || board[i][j] == 'W')
                                                                                                                                     {
                                                                                                                                        findtemplongest = findLongest(board, n, i, j);
                                                                                                                                        
                                                                                                                                        if (findtemplongest >= 6 )
                                                                                                                                        { 
                                                                                                                                          //printf("findtemplongest = %d\n", findtemplongest);
                                                                                                                                          char winner = board[i][j];
                                                                                                                                          
                                                                                                                                          if (winner == 'B')
                                                                                                                                          {printf("Black player wins.\n");}
                                                                                                                                          else if (winner == 'W')
                                                                                                                                          {printf("White player wins.\n");}
                                                                                                                        
                                                                                                                                          return 0; 
                                                                                                                                        }
                                                                                                                                    }
                                                                                                                                }
                                                                                                                            }
                                                                                                                            
                                                                                                                            return 1;
                                                                                                                     }
                                                                                                                            
                                                                                                                
char oppositecolour(char colour)
{ char newcolour;
if (colour == 'B')
{ newcolour = 'W'; }
else if (colour == 'W')
{ newcolour = 'B';}
return newcolour;
}                 
                                                                                                                        
int scorehuman(char ** board, int n, int lcurr, char colourcpu);                                                                                                                    
                                                                                                                    
//black goes first                                                                                                                    
int scorecpu(char ** board, int n, int *row, int *col, char colourcpu, int r, int *maxscore)
{    int lcurr;
    int lnext = 0;
    int i, j;
    int score = -6;
    int tempscore;
    int temprow, tempcol;
    
    if(r < n - 1)
    {
        scorecpu(board, n, row, col, colourcpu, r + 1, maxscore);
    }
        
    for(i = 0; i < n; i++)
    {    for(j = 0; j < n; j++)
        {  if (board[i][j] == 'U')
              { 
                     board[i][j] = colourcpu;               
               
                   lcurr = findLongest(board, n, i, j);
                   lnext = scorehuman(board, n, lcurr, colourcpu); 
                   
                   tempscore = (lcurr - lnext);
                      
                      if (tempscore > score)
                      {
                      score = tempscore;
                      *maxscore = tempscore;
                      *row = i;
                       *col = j;
                       
                       
                      } board[i][j] = 'U';
                      
               }    
         }
     }
return score;
}          
               
int scorehuman(char ** board, int n, int lcurr, char colourcpu)
{    int a, b;               
    //int tempcurr = findLongest(board, n, i, j);
    int tempscorehuman;
    int tempscore = -6;
    int templength;
    int tempnext;
             
                            
        for(a = 0; a < n; a++)
               {    for(b = 0; b < n; b++)
                       {     if (board[a][b] == 'U')
                           {    //int temprow = a;
                               //int tempcol = b;
                                   
                                   if (colourcpu == 'B')
                                   {board[a][b] = 'W';}
                                   else if (colourcpu == 'W')
                                   {board[a][b] = 'B';}
                                   
                                   
                               
                               
                               
                                   tempnext = findLongest(board, n, a, b);
                                 //tempscorehuman = lcurr - tempnext;
                                 
                                       if(tempnext > tempscore)
                                       {                                    
                                        tempscore = tempnext;
                                       
                                       } board[a][b] = 'U';
                               }
                           }
                       }
                   
                return tempscore;
}                     
            

int main(void)
{

int i, n;
char**board;

printf("Enter board dimensions (n): ");
scanf("%d", &n);

board = ((char**) malloc(n * sizeof(char*)));

for (i = 0; i < n; i++)
{board[i] = (char*) malloc(n * sizeof(char));}

intial(board, n);
printBoard(board, n);

char b,w;
int prow, pcol, row, col;
char st;
int pr;
char playerindicator;
char colourcpu, colourplayer;
printf("Computer playing B or W?: ");
scanf(" %c", &playerindicator);
char looper;
int maxscore;


if (playerindicator == 'B')
{ colourcpu = 'B';
  colourplayer = 'W';
}
else if (playerindicator == 'W')
{ colourcpu = 'W';
  colourplayer = 'B';
}

        if (colourplayer == 'B')
            {
                printf("Lay down a stone (ROW COL): ");
                scanf("%d %d", &row, &col); 
 
                board[row][col] = colourplayer; 
                printBoard(board,n);
            }
        while (checkrun(board,n) && findwinnerres(board, n))
        {     
 
            scorecpu(board, n, &row, &col, colourcpu, 0, &maxscore);
            printf("Computer lays a stone at ROW %d COL %d.\n", row, col);
            board[row][col]=colourcpu; 
            printBoard(board,n); 

            if(findwinnerres(board, n)==0)
            {
                break;
            }
            
            if(checkrun(board, n) ==0)
            {
                printf("Draw!");
                break;
                
            }

            printf("Lay down a stone (ROW COL): "); 
            scanf("%d %d", &row, &col); 
 
            if (board[row][col] == 'U') 
            {
            board[row][col] = colourplayer; 
            printBoard (board, n); 
            } 
            else 
            { 
                printf("That square is occupied.\n"); 
                do 
                { 
                     printf("Lay down a stone (ROW COL): "); 
                    scanf("%d %d", &row, &col); 
 
 
                    if (board[row][col] == 'U') 
                    { 
                    board[row][col] = colourplayer; 
                    printBoard (board, n); 
                    } 
 
                } while (board [row][col] == 'U'); 
            } 
 
        }
        
return 0;
}       
