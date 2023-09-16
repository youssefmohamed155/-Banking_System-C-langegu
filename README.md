//  main.c
//  Banking System
//
//  Created by Youssef on 10/09/2023.
//
//  ( printf - scanf - fgets) -  if - loop - function )
//   iit's my first project :) ;
//                                                                                              " بسم الله الرحمن الرحيم "    

#include <stdio.h>
#include <ctype.h>


int Create_Account (void);
char Deposit (void);
int  Withdraw (void);

int main(void) {
    char name [100];
    int choice ;
    //
    int Create_Account (void);
    char Deposit (void);
    int  Withdraw (void);
    //
    int i;
    int letterCount = 0;
    int u = 0;
    int totle;
    
    printf("Please Enter Your Name : ");
    
    fgets(name, sizeof(name), stdin);

    while (name[u] != '\0')
    {
        if (isalpha(name[u]))
        {
            
            letterCount++;
        }
        u++;
    }
     
    totle = letterCount + 12 ;
     
    for (i = 0; i < totle; i++)
    {
        printf("=");
    }
     
    printf("\n Welcame %s",name);

    for (i = 0; i < totle; i++)
    {
        printf("=");
    }
    

    while (1) {
        printf("\n==========================\n");
        printf("===== Banking System =====\n");
        printf("==========================\n");
        printf("[1] Create Account\n");
        printf("[2] Deposit\n");
        printf("[3] Withdraw\n");
        printf("[4] Exit\n");
        printf("Choose an option: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                Create_Account();
                break;
            case 2:
                Deposit();
                break;
            case 3:
                Withdraw();
                break;
            case 4:
                printf("\n==>> Are you sure you want to exit?...\n\n");
                return 0;
            default:
                printf("Invalid choice! Please try again.\n");
                break;
        }
    }

    return 0;
}

///                        ======================================================================== function ========================================================================

int Create_Account (void)
{
    printf("\n==========================\n");
    printf("\n===== Create Account =====\n");
    printf("\n==========================\n");
    

    char First_Name[20];
    char Mide_Name [20];
    char Last_Name [20];
    char User_Name [30];
    //
    int phone ;
    int National_Number;
    int Pwd;
    int co_pwd;
    
    
    printf("\nPlease enter all the required data correctly..\n\n");
    
    printf("First Name : \n");
    scanf("%s",First_Name);
    printf("Mide Name  : \n");
    scanf("%s",Mide_Name);
    printf("Last Name  : \n");
    scanf("%s",Last_Name);
    ///
    printf("Your Phone : \n");
    scanf("%d",&phone);
    ///
    printf("National Number : \n");
    scanf("%d",&National_Number);
    ///
    printf("User Name : \n");
    scanf("%s",User_Name);
    //
    printf("Password : \n");
    scanf("%d",&Pwd);
    printf("Confirm Password : \n");
    scanf("%d",&co_pwd);
    
    
    if (Pwd != co_pwd)
    {
        printf("The password does not match..\n");
        
    }
    
    
    printf("Thank You For Using The Service....\n");
    
    return(1) ;
    
}
///                     ================================================================================= function =====================================================================================
 char Deposit (void)
{
     char User [100] ;
     int pwd;
     int card [10];
     int cach;

     printf("\n===================\n");
     printf("\n===== Deposit =====\n");
     printf("\n===================\n");
     
     printf("-------------------------------------------------\n");
     printf("   Please enter all the required data correctly..\n");
     printf("-------------------------------------------------\n");
     
     printf("\nInter Your User name : ");
     scanf("%s",User);
     printf("Password : \n");
     scanf("%d",&pwd);
     
     printf("Enter the card number\n");
     scanf("%d",card);
     
     printf("Enter The Cach :\n");
     scanf("%d",&cach);
     printf("                Done             \n");
     
     printf("---------------------------------\n");
     printf("   You Enter In Cach [%d.00] E.G   \n",cach);
     printf("---------------------------------\n");
     
     printf("======================================\n");
     printf(" Thank You For Using The Service....\n");
     printf("======================================\n");
     
     
     return(2) ;
     
}

///                     ================================================================================= function =====================================================================================

int  Withdraw (void)
{
    printf("\n====================\n");
    printf("\n===== Withdraw =====\n");
    printf("\n====================\n");
    char User [100] ;
    int pwd;
    int card ;
    int cach;
    
   printf("\nPlease enter all the required data correctly..\n");

    printf("Inter Your User name : \n");
    scanf("%s",User);
    printf("Password : \n");
    scanf("%d",&pwd);
    
    printf("Enter the card number\n");
    scanf("%d",&card);
    
    printf(" Withdraw The Cach :\n");
    scanf("%d",&cach);
    printf("Done\n");
    printf("---------------------------------\n");
    printf("    You Enter In Cach [%d.00] E.G \n",cach);
    printf("---------------------------------\n");
    printf("======================================\n");
    printf("  Thank You For Using The Service....\n");
    printf("======================================\n");
    
    return (3);
}
