# Billing_Machine.
This code is a simple billing machine program for a tea store, written in c language.

Welcome Message: The software begins by presenting a welcome message to the user, signifying that they are in the tea store.

Display Menu: Following the welcome greeting, the application shows a menu of the many varieties of tea available for purchase, along with costs. The user is prompted to choose a decision.


User Input: The application waits for the user to enter their decision. The user picks a tea choice by providing the appropriate number.

Price determination: The application calculates the price of the tea based on the user's selection. Each tea selection has a predetermined price.

amount Input: After picking a tea, the user is asked to input the amount they wish to purchase.

Subtotal Calculation: The program determines the subtotal for the selected tea by multiplying the price by the amount given by the user.

overall Accumulation: The subtotal is added to the overall bill, accumulating the cost of all products selected by the user to date.


Item Added Feedback: The application alerts the user that the item has been added to their basket.

Repeat or Quit: The preceding stages (steps 2–8) are repeated until the user decides to quit. The user can resign by picking a specific option (such as 'resign') from the menu.

Total Bill: After the user decides to resign, the application calculates the total bill by adding the costs of all products selected by the user.

Farewell Message: Finally, the application shows the user the entire bill and says goodbye with a thank you message.

This explanation illustrates the step-by-step operation of a tea store's billing system without delving into the minutiae of the computer code.

WITH CODE EXPLANATION:--
step1:-
Include Libraries:
#include <stdio.h>
This line includes the standard input-output library, which provides functions like printf and scanf for input and output operations.

step2:-
Define displayMenu() Function:
float displayMenu() {
    // Displaying menu options
    printf("\nMenu:\n");
    printf("1. Black Tea - $3.00\n");
    printf("2. Green Tea - $4.00\n");
    printf("3. Masala Chai - $3.50\n");
    printf("4. Quit\n");

    // Variables declaration
    int choice;
    float price = 0;

    // Prompting user for choice
    printf("Enter your choice: ");
    scanf("%d", &choice);

    // Switch statement to determine price based on choice
    switch(choice) {
        case 1:
            price = 3.00;
            break;
        case 2:
            price = 4.00;
            break;
        case 3:
            price = 3.50;
            break;
        case 4:
            printf("Thank you for visiting!\n");
            break;
        default:
            printf("Invalid choice!\n");
            break;
    }

    // Returning the price of selected tea
    return price;
}

This function displayMenu() is responsible for presenting the menu choices to the user and obtaining their selection. It then returns the price of the chosen tea. Inside the function:

Menu options are shown.
The user is requested to enter an option.

A switch statement is used to set the pricing based on the user's selection.
The function returns the price of the specified tea.


step3:-
Define main() Function:
int main() {
    // Variables declaration
    int quantity;
    float total = 0;

    // Welcoming message
    printf("\nWelcome to the APNA--Tea Store!\n");

    // Loop for selecting tea and calculating total bill
    while (1) {
        // Calling displayMenu() function to select tea
        float price = displayMenu();

        // Exiting loop if user chooses to quit
        if (price == 0)
            break;

        // Prompting user for quantity
        printf("Enter quantity: ");
        scanf("%d", &quantity);

        // Calculating subtotal and updating total bill
        total += price * quantity;

        // Providing feedback that item has been added to cart
        printf("Item added to cart!\n");
    }

    // Printing total bill and farewell message
    printf("\n*******************************\n");
    printf("Total bill: $%.2f\n", total);
    printf("*******************************\n");
    printf("\n THANKYOU--->VISIT AGAIN  :)----!!");

    // Returning 0 to indicate successful completion of program
    return 0;
}

In the main function:

The variables for quantity and total bill are declared.
A welcome message is presented.

A loop is used to constantly execute the displayMenu() function, allowing the user to choose tea until they decide to exit.
Within the loop, the user is invited to enter the desired quantity of tea, and the sum is computed and added to the total bill.
It is shown that the item has been added to the cart.
When the loop ends (when the user decides to depart), the whole cost is printed, along with a farewell message.

final step:-
Upon execution, the software shows a welcome message and menu. The user may select the tea they desire by providing the appropriate number. They can also indicate a quantity. They have the option to resign after picking all of the products they desire. The application then calculates and shows the entire amount, along with a goodbye note.




