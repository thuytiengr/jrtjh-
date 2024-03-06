# jrtjh-oán tháp Hà Nội: Cần chuyển n tầng tháp từ vị trí A sang vị trí B dùng vị trí C làm trung gian. Yêu cầu: Mỗi lần chỉ chuyển 1 tầng, chỉ được dùng các vị trí A, B, C để đặt các tầng tháp, không được đặt tầng lớn lên trên tầng nhỏ. Hàm main sử dụng hàm này và có thể chạy nhiều lần để tính cho nhiều số n khác nhau nhập từ bàn phím.

Code mẫu:
#include <conio.h>
#include <stdio.h>
#include <iostream.h>

int d;
void chuyen(int, char, char, char);
void main()
{
	int n;
	char c;
	do {
		clrscr();
		d = 0;
		do { 	cout << "Nhap so tang thap ( < 10), n=";
			cin >> n;
		} while ((n < 1) || (n > 9));
  
	if (n == 1) cout << "\nLan chuyen " << ++d << " : Tu " << a << " sang " << b;
	else
	{
		chuyen(n - 1, a, c, b);
		chuyen(1, a, b, c);
		chuyen(n - 1, c, b, a);
	}
}#include <conio.h>
#include <stdio.h>
#include <iostream.h>

int d;
void chuyen(int, char, char, char);
void main()
{
	int n;
	char c;
	do {
		clrscr();
		d = 0;
		do { 	cout << "Nhap so tang thap ( < 10), n=";
			cin >> n;
		} while ((n < 1) || (n > 9));
		chuyen(n, 'A', 'B', 'C');
		cout << "\nTong so lan chuyen=" << d;
		fflush(stdin);
		cout << "\nTiep tuc ? (c/k):";
		cin >> c;
	} while ((c == 'c') || (c == 'C'));
}

void chuyen(int n, char a, char b, char c)
{
	if (n == 1) cout << "\nLan chuyen " << ++d << " : Tu " << a << " sang " << b;
	else
	{
		chuyen(n - 1, a, c, b);
		chuyen(1, a, b, c);
		chuyen(n - 1, c, b, a);
	}
}
