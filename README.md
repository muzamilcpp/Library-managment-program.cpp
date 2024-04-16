# Library-managment-program.cpp
it is a cpp program to manage libraryworks .
#include<iostream>
#include<string>
using namespace std;

struct Book {
	int count;
	int id;
	string title;
	string author;

};

void addbook(Book book[], int n) {
	for (int i = 0;i < n;i++) {
		cout << "Enter the book id: ";
		cin >> book[i].id;
		cin.ignore();
		cout << "Enter the book name: " ;
		getline(cin, book[i].title);
		cout << "Enter the author name:" ;
			getline(cin, book[i].author);
	book[i].count = i + 1;
		cout << "Total add books = " <<	book[i].count<<endl;
	}
}
int main() {
		 int n;
	 cout << "Enter how many books you want to enter: ";
	 cin >> n;
	 cin.ignore();
	 Book books[n];
	 addbook(books,n);
	 return 0;
  }
