#include <stdio.h>

void displayMenu();
float UsdToInr(float amount);
float InrToUsd(float amount);
float UsdToGbp(float amount);
float InrToGbp(float amount);
float GbpToInr(float amount);
float GbpToUsd(float amount);

int main() {
	int choice;
	float amount;

	do {
		displayMenu();

		printf("Enter your choice (1-7): ");
		scanf("%d", &choice);

		if(choice >=1 && choice <= 6) {
			printf("Enter amount to convert: ");
			scanf("%f", &amount);
		}

		switch(choice) {
		case 1:
			printf("%.2f USD is %.2f INR\n", amount, UsdToInr(amount));
			break;
		case 2:
			printf("%.2f INR is %.2f USD\n", amount, InrToUsd(amount));
			break;
		case 3:
			printf("%.2f USD is %.2f GBP\n", amount, UsdToGbp(amount));
			break;
		case 4:
			printf("%.2f INR is %.2f GBP\n", amount, InrToGbp(amount));
			break;
		case 5:
			printf("%.2f GBP is %.2f INR\n", amount, GbpToInr(amount));
			break;
		case 6:
			printf("%.2f GBP is %.2f USD\n", amount, GbpToUsd(amount));
			break;
		case 7:
			printf("Exiting the program. Goodbye!\n");
			break;
		default:
			printf("Invalid choice. Please choose from the above statements!\n");
			break;
		}
	} while (choice != 7);

	return 0;

}

void displayMenu() {
	printf("\nCurrency Converter Menu:\n");
	printf("1. USD TO INR\n");
	printf("2. INR TO USD\n");
	printf("3. USD TO GBP\n");
	printf("4. INR TO GBP\n");
	printf("5. GBP TO INR\n");
	printf("6. GBP TO USD\n");
	printf("7. Exit\n");
}

float UsdToInr(float amount) {
	return amount * 84.10;
}

float InrToUsd(float amount) {
	return amount / 84.10;
}

float UsdToGbp(float amount) {
	return amount * 0.75;
}

float InrToGbp(float amount) {
	return amount / 100;
}

float GbpToInr(float amount) {
    return amount * 100;
}

float GbpToUsd(float amount){
    return amount / 1.30;
}





