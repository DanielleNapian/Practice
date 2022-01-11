# Practice

    #include <iostream>
    #include <string>

    using namespace std;

    void choice(char reply)
    {


            switch (reply)
            {
            case 'y':
            case 'Y':
            {
                cout << "Enjoy";
                break;
            }
            case 'n':
            case 'N':
            {
                cout << "Cancelled";
                break;
            }
            default:
            {
                cout << "Invalid input";
            }
            }
        }


    int main()
    {
        int age;
        char reply;
       cout << "Enter your age\n";

       cin >> age;
       while (cin.fail())
       {
           cin.clear();
           cin.ignore(1000, '\n');
           cout << "Enter your age again\n";
           cin >> age;

       }

       if (age >= 16 && age <= 21)
       {
           cout << "Would you like to go to the mall: \n";


           string reply2;
           cin >> reply2;
           while (reply2.size() != 1)
           {
               cout << "You have entered more than one character: " << endl;
               cout << "Enter only one character answer" << endl;
               cin >> reply2;
           }
           reply = reply2.at(0);
           choice(reply);
       }
       else  if (age >= 22 && age <= 30)
       {
           cout << "Would you like to go to the Hawaii: \n";
           string reply2;
           cin >> reply2;
           while (reply2.size() != 1)
           {
               cout << "You have entered more than one character: " << endl;
               cout << "Enter only one character answer" << endl;
               cin >> reply2;
           }
           reply = reply2.at(0);
           choice(reply);
       }
       else
       {
           cout << "You're not eligible to participate \n";
       }


    }
    
 Practice 2 
 
     #include <iostream>
    #include <string>
    using namespace std;

    void fact(double num)
    {
        long double f = 1;
        for(int y = num; y > 0; y--)
        {
            f = y * f;
        }
        cout << "The factorial is: " << f << endl;
    }

    void table(double num)
    {
        int negative = 0;
        int positive = 0;
        for (int x = -5; x <= 10; x++)
        {
            cout << num << " x " << x << " = " << num*x << endl;
            if (num*x < 0)
            {
                negative++;
            }
            else {
                positive++;
                 }
        }
        cout << " The negative numbers in the table are: " << negative<< endl;
        cout << " The positive numbers in the table are: " << positive << endl;
    }


    int main()
    {
        string name;
        double num;
        cout << " Enter your full name " << endl;
        getline(cin, name);
        cout << " Enter any number range from 1 - 10 " << endl;
        cin >> num;
        while (num <= 0 || num >= 11 || cin.fail())
        {
            cin.clear();
            cin.ignore(31, '\n');
            cout << "Incorrect command, please try again: " << endl;
            cin >> num;
        }
        fact(num);
        table(num);


    }
