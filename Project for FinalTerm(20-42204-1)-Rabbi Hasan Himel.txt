#include <iostream>//2.Contact Management System
using namespace std;
class contact {
protected:
    int a,n;
    int c=0;
    string nu[15]={""};
    string na[30]={""};
    string fa[30]={""};
public:
virtual void display(){
cout<<"*** CONTACT MANAGEMENT SYSTEM ***";
cout<< "\n1. Instruction";
cout<<"\n2. Create a New Contact";
cout<<" \n3. Delete a Contact\n>";
}
};
class sim : public contact{
public:
void newWindow(){
    int choice;
        cin>> choice;
switch(choice){
        case 1:
        inst();
            break;
        case 2:
             virFunt();
            break;
        case 3:
        deleteCon();
            break;
        default:
            cout<<"\nInvalid Input.. "<<endl;
            break;
        }}
       void inst()
    {
        cout<<"\nRead the following Instructions to Store a Contact.";
        cout<<"\n\n-Firstly,Enter First Name.";
        cout<<"\n-Secondly,Enter Last Name.";
        cout<<"\n-Thirdly,Enter Phone Number.";
        cout<<"\n-Lastly,After Reading Run the Program again."<<endl;
    }

void deleteCon()
    {
        cout<<"\nEnter First Name: ";
        cin>>fa[30];
        cout<<"Enter Last Name: ";
        cin>>na[30];
        cout<<"Enter phone number you want to delete: ";
        cin>>nu[15];
        cout<<"*Contact Successfully deleted*"<<endl<<endl;
    }
void virFunt(){
cout << "\nHow many Contact do want to store? : ";
cin>> n;
cout << "\n------Contact List------"<<endl;
for (a=0;a<n;a=a+1){
       c=c+a;
cout << "\nContact's First Name: ";
cin>>fa[30];
cout << "Contact's Last Name: ";
cin>>na[30];
cout << "Contact Number(With Country Code): ";
cin>>nu[15];
}
}
};
int main()
{
contact *p;
sim ob1;
p = &ob1;
p -> display();
ob1.newWindow();
}
