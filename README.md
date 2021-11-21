# Lecture-12-Arrays

SLIDE 9, Example initialisation (longhand)

    #include <iostream>
    using namespace std;

    int main()
    {
      int ages[5];

      ages[0] = 19;
      ages[1] = 23;
      ages[2] = 22;
      ages[3] = 30;
      ages[4] = 18;
    }
    
SLIDE 10, Example initialisation (shorthand)

    #include <iostream>
    using namespace std;
    
    int main()
    {
      int array[5] = {19, 23, 22, 30, 18};
      
      or
      
      int array [] = {19, 23, 22, 30, 18};
    }
    
SLIDE 11, Months of the Year

    #include <iostream>
    using namespace std;
    
    int main()
    {
    //initialisation:
    string month[12] = {"January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"};
    
    }
    
SLIDE 12, Accessing array values
    
    #include <iostream>
    using namespace std;
    
    int main()
    {
    int heartRates[8] = { 54, 60, 71, 59, 62, 63, 60, 58 };

    cout << heartRates[3] << endl;
    cout << heartRates[6] << endl;
    }
    
SLIDE 13, Iterating through an array

    #include <iostream>
    using namespace std;
    
    int main()
    {
    	int heartRates[8] = { 54, 60, 71, 59, 62, 63, 50, 68 };

    	for (int i = 0; i < 8; i++) {
		cout << heartRates[i] << endl;
    	}
    }
    
SLIDE 14, Time Travel

    #include <iostream>
    using namespace std;
    
    int main()
    {
    	string month[12] = { "January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December" };
    
    	for (int i = 0; i < 12; i++) {
        	cout << month[i] << endl;
    	}
    }
    
SLIDE 15, Marks

    #include <iostream>
    using namespace std;
    
    int main()
    {
    	float sum = 0.0, avg;

    	int mark[5];
    	for (int i = 0; i < 5; i++) {
		cout << "Enter the mark for subject " << (i + 1) << " (0-100):" << endl;
        	cin >> mark[i];
        	while (cin.fail() || mark[i] > 100 || mark[i] < 0) { //error handling
            	cout << "\nInvalid command. Enter the marks again.\n";
            	cin.clear(); //clears the error flag on cin
            	cin.ignore(); //used to ignore or clear one or more characters from the input
            	cin >> mark[i];
        	}
    	}
    	cout << "\nThese are the values that you have entered for the marks" << endl;
    	for (int j = 0; j < 5; j++) {
        	cout << mark[j] << endl;
        	sum = sum + mark[j]; //formula for sum
    	}
    	cout << "\nSum = " << sum << endl;
    	avg = sum / 5; //formula for average
    	cout << "Average = " << avg;

    	return 0;
}
    

