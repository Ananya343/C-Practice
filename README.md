#include<iostream>
#include<string.h>

using namespace std;

class bank
{
  int AccountNo;
	char H_name[100];
	float balance;
 public:
     bank(int Account_No,char*H_name,float A_balance)
	 {
	  AccountNo=Account_No;
		strcpy(H_name,name);
		balance=A_balance;
	 } 
	 void deposit();
	 void withdraw();
	 void display();
};
void bank::deposit()
{
   int depositAmt;
   cout<<"Enter deposit Amount = "endl;
   cin>>depositAmt;
   balance+=depositAmt; //add the value to variable
}
void bank::withdraw()
{  
   int withdrawAmt;
   cout<<"Enter withdraw Amount = "endl;
   cin>>withdrawAmt;
   if(withdraw > balance)
			cout<<"Insufficent funds = "endl;
   balance-=withdrawAmt;
}
void bank::display()
{
  cout<<"Account Number: :"<<AccountNo;
  cout<<"Name:"<<H_name;
  cout<<"Balance" "<<balance;
}

int main()
{
     int Account_No;
	   char name[150];
     float balance;
     cout<<"\n Enter the details:\n";
     cout<<"\n Account number";
     cin>>Account_No;
     cout<<"\n Name:";
     cin>>name;
     cout<<"\n Balance";
     cin>>balance;
  
    bank detail(Account_No,name,balance);
    detail.deposit();
    detail.withdraw();
    detail.display();
    return 0;
 }

  
