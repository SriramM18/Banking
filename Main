#include <iostream>
using namespace std;

class bank
{
    int id = 1, a = 1;
    struct hello
    {
        string fname, lname, gender, accounttype;
        int tdeposit, pincode, accountnumber;
        long contactnumber;
    } arr[1000];

public:
    void switchcase();
    void createAccount();
    void balanceEnquiry();
    void deposit();
    void withdraw();
    void holderList();
    void CloseAccount();
    void modifyData();
    void accountDetails();
    void quit();
};
void bank::switchcase()
{
    int temp=1;
    while(temp==1){
        int ch;
    cout<<endl<<"***********************"<<endl;
    cout << "1.Open an account " << endl;
    cout << "2.Balane Enquiry" << endl;
    cout << "3.Deposit" << endl;
    cout << "4.Withdrawal" << endl;
    cout << "5.All holder List" << endl;
    cout << "6.Close an account" << endl;
    cout << "7.Modify an account " << endl;
    cout << "8.Account details" << endl;
    cout << "9.Quit \n" << endl;
    cout<<"***********************"<<endl;
    cout << "Enter you choice=";
    cin>>ch;
    switch (ch)
    {
    case 1:
        bank::createAccount();
        break;
    case 2:
        bank::balanceEnquiry();
        break;
    case 3:
        bank::deposit();
        break;
    case 4:
        bank::withdraw();
        break;
    case 5:
        bank::holderList();
        break;
    case 6:
        bank::CloseAccount();
        break;
    case 7:
        bank::modifyData();
        break;
    case 8:
        bank::accountDetails();
        break;
    case 9:
        bank::quit();
        temp=0;
        break;
    default:
        cout <<"INCORRECT option";
        break;
    }
    }
}
void bank::createAccount()
{
    int ideposit;
    cout << "First Name: ";
    cin >> arr[id].fname;
    cout << endl << "last name :";
    cin >> arr[id].lname;
    cout << endl << "initial deposit:";
    cin >> ideposit;
    cout << endl << "Gender <M/F/O>:";
    cin >> arr[id].gender;
    cout << endl << "accounttype<C/S>:";
    cin >> arr[id].accounttype;
    cout<< endl << "contact number:";
    cin>> arr[id].contactnumber;
    cout<<endl<<"***********************";
    int p=1;
    while(p!=0){
        cout << endl << "Please insert a pincode:";
        cin>>arr[id].pincode;
        cout<<"Re Enter your Pincode = ";
        int rpin;
        cin>>rpin;
        if(rpin!=arr[id].pincode){
        cout<<endl<<"Pincode does not match...re Enter";
        }
        else{
            cout<<endl<<"Pincode Created";
            p=0;
        }
    }
    cout<<endl;
    arr[id].tdeposit = ideposit;
    arr[id].accountnumber = a;
    cout<<endl<<"***********************";
    cout <<endl<<"Account Number= " << a<<endl;
    cout<<"Account Balance= "<<arr[id].tdeposit<<endl; ;
    cout<<"             ****DO NOT Share Your pincode****";
    cout << endl << "Pincode= " << arr[id].pincode;
    cout<<endl<<"***********************";
    a++;
    id++;
    system("cls");
}
void bank::balanceEnquiry() {
     int m, n,i,temp=0;
        cout << "Enter your Account Number=";
        cin >> m;
        cout << "Please enter yout pincode= ";
        cin >> n;
     for(i=1;i<=id;i++){
        if (arr[i].pincode == n && arr[i].accountnumber == m)
        {
        cout <<arr[i].accountnumber<<"   "<<arr[i].fname<<" "<<arr[i].lname<<endl;
        cout<< "Balance is: "<<arr[i].tdeposit<<endl;
            temp=1;
            break;
        }
    }
    if(temp==0)
            cout << "Incorrect input...Try again"<< endl;
}
void bank::holderList() {
    cout<<"**********HOLDER LIST***********"<<endl;
    cout<<"ACC No."<<"     "<<"ACC. Type"<<"     "<<"NAME"<<endl;
    for(int i=1; i<id ; i++ ){
        cout<<arr[i].accountnumber<<"     "<<arr[i].accounttype<<"     "<<arr[i].fname<<" "<<arr[i].lname<<endl;
        // cout<< "first name is :"<<arr[i].fname<<endl;
        // cout<< "last name is :"<<arr[i].lname<<endl;
        // cout<< "gender <M/F/O> :"<<arr[i].gender<<endl;
        // cout<< "Type of account <C/S> :"<<arr[i].accounttype<<endl;
        // cout<< "contact number is :"<<arr[i].contactnumber<<endl;
        // cout<< "Account number is:"<<arr[i].accountnumber<<endl;
        // cout<< "Total balance in the account is: "<<arr[i].tdeposit<<endl;
    }
}
void bank::deposit()
{
    int Acc_num, pcode, new_dep,i,temp=0;
        cout<<"**********KINDLY DEPOSIT THE MONEY***********"<<endl;
        cout << "Enter your Account Number=";
        cin >> Acc_num;
        cout << "Enter your pincode=";
        cin >> pcode;
    for(i=1;i<=id;i++){
        if (arr[i].pincode == pcode && arr[i].accountnumber == Acc_num)
        {
            cout << "enter the amount of new deposit=";
            cin >> new_dep;
            arr[i].tdeposit = arr[i].tdeposit + new_dep;
            cout << "the balance in your account is:" << arr[i].tdeposit;
            temp=1;
            break;
        }
       
    }
        if(temp==0)
            cout << "Incorrect pin ...Try again"<< endl;
}
void bank::withdraw()
{
    int m, n,i,temp=0;
    cout<<"**********KINDLY WITHDRAW THE MONEY***********"<<endl;
    cout << "Enter your Account Number=";
        cin >> m;
        cout << "Please enter yout pincode= ";
        cin >> n;
    for(i=1;i<=id;i++){
        if (arr[i].pincode == n && arr[i].accountnumber == m)
        {
            int q;
            cout << "Enter the amount= ";
            cin >> q;
            if (arr[i].tdeposit - q < 0) {
                cout << "Insufficient Balance.....";
                temp=1;
                break;
            }
            arr[i].tdeposit = arr[i].tdeposit - q;
            cout << "Account balance=" << arr[i].tdeposit;
            temp=1;
            break;
        }
    }
    if(temp==0)
            cout << "Incorrect input...Try again"<< endl;
}
void bank::modifyData(){
    int m, n;
    int d=1,i,temp=0;
        cout << "Enter your Account Number=";
        cin >> m;
        cout << "Please enter yout pincode= ";
        cin >> n;
        for(i=1;i<=id;i++){
             if (arr[i].pincode == n && arr[i].accountnumber == m)
                {
                    int x;
                    cout << "****************MODIFY DATA*************************";
                    cout << endl << "1 First Name";
                    cout << endl << "2 Last Name";
                    cout << endl << "3 Gender";
                    cout << endl << "4 Account type";
                    cout <<endl  << "5 contact number";
                    cout << endl << "6 pincode";
                    cout << endl << "choose option to modify";
                    cin >> x;
                    switch (x)
                    {
                    case 1:
                        cout << "Enter the First Name to be modify= ";
                        cin >>arr[i].fname;
                        break;
                    case 2:
                        cout<<"Enter the last Name to be modify= ";
                        cin >>arr[i].lname;
                        break;
                    case 3:
                        cout<<"Enter the Gender to be modify= ";
                        cin >>arr[i].gender;
                        break;
                    case 4:
                        cout<<"Enter the Account Type to be modify= ";
                        cin >>arr[i].accounttype;
                        break; 
                    case 5:
                        cout<<"Enter the contact Number to be modify= ";
                        cin >>arr[i].contactnumber;
                        break; 
                    case 6:
                        while(d!=0){
                        cout << endl << "Please insert a New pincode:";
                        cin>>arr[i].pincode;
                        cout<<"Re Enter your Pincode = ";
                        int rpin;
                        cin>>rpin;
                        if(rpin!=arr[i].pincode){
                        cout<<endl<<"Pincode does not match...re Enter";
                        }
                        else{
                                cout<<endl<<"New Pincode Created";
                                d=0;
                            }
                        }
                        break;       
                        default:
                        cout<<"Incorrect choice";
                        break;
                    }
                    break;
                    temp=1;
                }
    }
    if(temp==0)
     cout<<endl<<"Credential does not match";
}
void bank::CloseAccount() {
        int m, n,i,temp=0;
        cout<<"**********************************"<<endl;
        cout << "Enter your Account Number=";
        cin >> m;
        cout << "Please enter yout pincode= ";
        cin >> n;
        for(i=1;i<=id;i++){
        if (arr[i].pincode == n && arr[i].accountnumber == m){
            for( int j=i; j<=id; j++){
            arr[j].pincode=arr[j+1].pincode;
            arr[j].accountnumber=arr[j+1].accountnumber;
            arr[j].lname=arr[j+1].lname;
            arr[j].fname=arr[j+1].fname;
            arr[j].gender=arr[j+1].gender;
            arr[j].contactnumber=arr[j+1].contactnumber;  
            arr[j].tdeposit=arr[j+1].tdeposit;
            arr[j].accounttype=arr[j+1].accounttype;
            }
            temp=1;
            break;
        }
    }
            if(temp==0)
            cout << "Incorrect input...Try again"<<endl; 
    }
    
void bank::accountDetails(){
    int m, n,i,temp=0;
        cout << "Enter your Account Number=";
        cin >> m;
        cout << "Please enter yout pincode= ";
        cin >> n;
     for(i=1;i<id;i++){
        if (arr[i].pincode == n && arr[i].accountnumber == m)
        {
        cout << "Account Details of person "<<endl;
        cout<<" first name is :"<<arr[i].fname<<endl;
        cout<< "last name is :"<<arr[i].lname<<endl;
        cout<< "gender <M/F/O> :"<<arr[i].gender<<endl;
        cout<< "Type of account <C/S> :"<<arr[i].accounttype<<endl;
        cout<< "contact number is :"<<arr[i].contactnumber<<endl;
        cout<< "Account number is:"<<arr[i].accountnumber<<endl;
        cout<< "Total balance in the account is: "<<arr[i].tdeposit<<endl;
            temp=1;
            break;
        }
    }
    if(temp==0)
            cout << "Incorrect input...Try again"<< endl;
}

void bank::quit(){
    cout<<"Thankyou For Operating"<<endl;
    cout<<"*********************"<<endl;
}

int main()
{
    bank b;
    cout<<"*****************************"<<endl;
    cout<<"Welcome to Our  Banking System"<<endl;
    
    cout<<"*****************************"<<endl;
    b.switchcase();
    return 0;
}
