# C++ struct example
# include <iostream>
# include <string>
# include <iomanip>
using namespace std;
struct Payroll
{
int empId;
string name;
float no_of_hours;
float hourlypay;
float grosspay;
};
Payroll p;
void inputfunction()
{
    cout<<endl<<setw(45)<<setfill('*');
    cout<<"\n Enter the Employee ID: ";
    cin>> p.empId;
    cin.ignore();
    cout<<"\n Enter the Employee Name: ";
    getline(cin, p.name);
    cout<<"\n Enter the Number of hours worked: ";
    cin>> p.no_of_hours;
    cout<<"\n Enter the Hourly Pay: ";
    cin>> p.hourlypay;
    p.grosspay= (p.no_of_hours * p.hourlypay);
    cout<<"The gross pay is $ "<<p.grosspay;
}
int main()
{
    int range,condition=0;
    cout<<"Input Fuction is calling \n";
    cout<<"Enter numbers of records....";
    cin>>range;
    while(condition<range)
    {
        inputfunction();
        condition++;
    }
    cout<<"\n Program is terminated . . .";
    return 0;
}
