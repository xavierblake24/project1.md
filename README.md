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

#include <map> 

 

struct IngredientEntry { 

    std::string ingredient; 

    double quantity; 

    std::string date; 

}; 

 

std::map<std::string, double> categoryTotals; 

 

void saveIngredient(const IngredientEntry& entry) { 

    std::ofstream file("ingredient_data.txt", std::ios::app); 

 

    if (file.is_open()) { 

        file << entry.ingredient << " " << entry.quantity << " " << entry.date << std::endl; 

        file.close(); 

    } else { 

        std::cerr << "Error: Unable to save ingredient data." << std::endl; 

    } 

} 

 

void categorizeExpense(const IngredientEntry& entry) { 

    if (entry.quantity >= 50 && entry.quantity <= 200) { 

        categoryTotals[entry.ingredient] += entry.quantity; 

    } 

} 

 

void generateSummaryReport() { 

    std::cout << "\nSummary Report\n"; 

    std::cout << std::setw(15) << "Ingredient" << std::setw(15) << "Total Quantity\n"; 

    for (const auto& pair : categoryTotals) { 

        std::cout << std::setw(15) << pair.first << std::setw(15) << pair.second << std::endl; 

    } 

} 

 

int main() { 

    int choice; 

    IngredientEntry newEntry; 

 

    do { 

        std::cout << "\n1. Input new ingredient\n2. View summary report\n3. Exit\nEnter your choice: "; 

        std::cin >> choice; 

 

        switch (choice) { 

            case 1: 

                std::cout << "\nEnter ingredient name (name): "; 

                std::cin >> newEntry.ingredient; 

 

                std::cout << "Enter quantity ($50-$200): "; 

                std::cin >> newEntry.quantity; 

 

                std::cout << "Enter date (MM/DD/YYYY): "; 

                std::cin >> newEntry.date; 

 

                saveIngredient(newEntry); 

                categorizeExpense(newEntry); 

                break; 

 

            case 2: 

                generateSummaryReport(); 

                break; 

 

            case 3: 

                std::cout << "\nExiting program.\n"; 

                break; 

 

            default: 

                std::cerr << "\nError: Invalid choice. Please enter a valid option.\n"; 

        } 

    } while (choice != 3); 

 

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

References: 

Malik, D. S. (2017). C++ Programming: From Problem Analysis to Program Design (8th ed.). Cengage Learning. January 13, 2024, https://www.cengage.com/c/c-programming-8e-malik/9781337102087/ 

 

 
