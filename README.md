# Library-management-system-
A Library Management System is a software application used to manage and organize library operations efficiently. It helps in maintaining records of books, users, issue and return transactions. The system reduces manual work, saves time, improves accuracy, and allows easy searching, tracking, and management of library resources





#include <stdio.h>
#include <string.h>

struct Book {
char name[50];
int quantity;
};

int main() {
struct Book library[100];
int n, i;
int totalQuantity = 0;

printf("Enter number of different books in library: ");
scanf("%d", &n);

for (i = 0; i < n; i++) {
printf("\nEnter name of book %d: ", i + 1);
scanf(" %[^\n]", library[i].name);

printf("Enter quantity of book %d: ", i + 1);    
scanf("%d", &library[i].quantity);    

totalQuantity += library[i].quantity;

}

printf("\n--- Library Book Details ---\n");
for (i = 0; i < n; i++) {
printf("Book Name: %s | Quantity: %d\n",
library[i].name, library[i].quantity);
}

printf("\nTotal number of different books: %d\n", n);
printf("Total quantity of all books in library: %d\n", totalQuantity);

return 0;

}.
