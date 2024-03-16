# project1.md
Project 1  

 

Statement of Independent Effort: 

[XAVIER BLAKE, hereby certify that this is my original work completed with the assistance of [BLAKE]/the resources listed in the reference. I used these resources in the following areas: [Pseudocode, Flowchart, Test Cases, and Code]. 

 

 

 

Analysis of Specifications: 

Input 

Process 

Output 

Ingredient 

Clarify Ingredient 

Ingredient name, quantity, date 

Summary 

Data from file 

Error/Display report 

Exit 

Ends program 

End 

 

 

 

 

 

Pseudocode: 
#include <iostream>
#include <fstream>
#include <iomanip>

using namespace std;

// Function to input quantities of baking items
void inputQuantities(int& flour, int& milk, int& eggs, int& sugar) {
    cout << "How many bags of flour were purchased? ";
    cin >> flour;
    cout << "How many milk jugs were purchased? ";
    cin >> milk;
    cout << "How many cartons of eggs were purchased? ";
    cin >> eggs;
    cout << "How many bags of sugar were purchased? ";
    cin >> sugar;
}

// Function to calculate total cost
double calculateTotalCost(int flour, int milk, int eggs, int sugar) {
    const int flourcost = 10, eggscost = 15, milkcost = 20, sugarcost = 25;
    return (eggs * eggscost) + (milk * milkcost) + (sugar * sugarcost) + (flour * flourcost);
}

// Function to handle payment
void handlePayment(double totalCost) {
    double payment;
    cout << "Total cost: $" << totalCost << endl;
    cout << "Enter payment: $";
    cin >> payment;

    if (payment != totalCost)
        cout << "You still owe: $" << fixed << setprecision(2) << (totalCost - payment) << endl;
    else
        cout << "Have a great day!" << endl;
}

// Function to write to file
void writeToFile(int flour, int milk, int eggs, int sugar, double totalCost, double payment) {
    ofstream outputFile("bakingitems.txt", ios::out);
    outputFile << "Baking Items" << endl;
    outputFile << "Milk: " << milk << endl;
    outputFile << "Flour: " << flour << endl;
    outputFile << "Eggs: " << eggs << endl;
    outputFile << "Sugar: " << sugar << endl;
    outputFile << "Total Cost: $" << totalCost << endl;
    outputFile << "Payment: $" << payment << endl;
    outputFile.close();
}

int main() {
    int choice;
    int flour, milk, eggs, sugar;
    double totalCost, payment;

    do {
        cout << "Menu:\n";
        cout << "1. Input quantities of baking items\n";
        cout << "2. Calculate total cost\n";
        cout << "3. Handle payment\n";
        cout << "4. Write to file\n";
        cout << "5. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;

        switch(choice) {
            case 1:
                inputQuantities(flour, milk, eggs, sugar);
                break;
            case 2:
                totalCost = calculateTotalCost(flour, milk, eggs, sugar);
                cout << "Total cost: $" << totalCost << endl;
                break;
            case 3:
                handlePayment(totalCost);
                break;
            case 4:
                writeToFile(flour, milk, eggs, sugar, totalCost, payment);
                cout << "Data written to file.\n";
                break;
            case 5:
                cout << "Exiting program.\n";
                break;
            default:
                cout << "Invalid choice. Please try again.\n";
        }
    } while (choice != 5);

    return 0;
}




 


 

 

}Flowchart: 
https://famu-my.sharepoint.com/:w:/g/personal/xavier1_blake_famu_edu/EZxrHKdxCoBFtRoln9-vh90BkaE74JBHWO7_VIycTJl6rA?e=pWzlWW
 

Test Cases: 

Case # 

Case Description 

Input 

Condition 

Output 

1 

Item should be approved 

Price $100 

False 

Approved 

2 

Item should be approved(edge case) 

Price $200 

False 

Approved 

3 

Item shouldn’t be approved 

Price $300 

True 

Not approved 

Code: 

https://codio.com/xblake/sandbox 

User Manual: 
https://github.com/xavierblake24/GUIDE.md/blob/main/README.md
References: 

Malik, D. S. (2017). C++ Programming: From Problem Analysis to Program Design (8th ed.). Cengage Learning. January 13, 2024, https://www.cengage.com/c/c-programming-8e-malik/9781337102087/ 

 

 
