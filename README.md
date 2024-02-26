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

#include <string> 

#include <iomanip> 

#include <fstream> 

 

Using namespace std: 

 

Int main () 

{ 

      int flour, milk, eggs, sugar 

      double items, payment, totalCost: 

      const int flourcost= 10 , eggscost=15 milkcost=20 , sugarcost=25 : 

      ofstream outputFile ( “bakingitems.txt “ , ios : : ) ; 

  

     cout<<”How many bags of flour were purchased? “; 

     cin>>flour 

     cout<<”How many milk jugs were purchased? “; 

     cin>>milk 

     cout<<”How many cartons of eggs were purchased? “; 

     cin>> eggs 

     cout<<”How many bags of sugar were purchased? “; 

     cin>>sugar 

 

      totalCost=( eggs*eggscost) + ( milk*milkcost ) + ( sugar*sugarcost) + ( flour*flourcost) ; 

   

      cout<<”Total cost: $”<< ( eggs*eggscost) + ( milk*milkcost ) + ( sugar*sugarcost) + ( flour*flourcost)<< 

      cout<<”Enter payment: $” ; 

      cin>>Payment ; 

 

       if  (payment  !=  totalcost ) 

              cout<<”You still owe:  $”<<fixed<<setprecision(2)<<(payment-totalCost)<<endl 

        else 

              cout<<”Have a great day!”<<endl 

         

        outputFile<<”Baking Items”<<endl ; 

        outputFile<<”milk : “<<milk<<endl; 

        outputFile<<flour : “<<flour<<endl 

        outputFile<<eggs : “<<eggs<<endl 

        outputFile<<sugar : “sugar<<endl 

        outputFile<<”Total Cost :  $”<<totalCost<<endl 

        outputFile<<Payment : $”<<payment<<endl 

 

        outputFile.close () ; 

 

        return 0: 

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

 

 
