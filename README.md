# Rikimuhamadikbal_1121031006_DLLC
#include <iostream>
#define MAX 5
//Riki muhamad ikbal//
//1121031006//
//MAIN : PROGRAM STACK MENGGUNAKAN BAHASA PEMROGRAMAN C++S
using namespace std;
//Deklarasi struct tumpukan
struct Stack {
    
	int top,Noel, data[MAX];
    
}Tumpukan;

void init(){
	Tumpukan.top = -1;
}

bool isEmpty() {
  return Tumpukan.top == -1;
}

bool isFull() {
	return Tumpukan.top == MAX-1;
}

void push() {
   if (isFull()) {
		cout << "\nTumpukan penuh"<<endl;
	}
	else {
    Tumpukan.top++;
    cout << "\nMasukkan data = "; cin >> Tumpukan.data[Tumpukan.top];
    cout << "Data " << Tumpukan.data[Tumpukan.top] << " masuk ke stack"<<endl;
	}
}

void pop() {
	if (isEmpty()) {
		cout << "\nData kosong\n"<<endl;
	}
	else {
    cout << "\nData "<<Tumpukan.data[Tumpukan.top]<<" sudah terambil"<<endl;
    Tumpukan.top--;
	}
}

void printStack() {
	if (isEmpty()) {
		cout << "Tumpukan kosong";
	}
	else {
    cout << "\nTumpukan : ";
		for (int i = Tumpukan.top; i >= 0; i--)
			cout << Tumpukan.data[i] << ((i == 0) ? "" : ",");
	}
}

int main() {
	int pilihan;
	init();
	do {
    printStack();
		cout <<"\n1. Create Stack Baru(CREATE)\n"
        << "2. Input (Push)\n"
        <<"3. Hapus (Pop)\n"
        <<"4. Keluar\n"
        <<"Masukkan Pilihan: ";
		cin >> pilihan;
		switch (pilihan)
		{
        case 1:
			init();
			break;
		case 2:
			push();
			break;
		case 3:
			pop();
			break;
		default:
      cout << "Pilihan tidak tersedia" << endl;
			break;
		}
	} while (pilihan!=4);
}
