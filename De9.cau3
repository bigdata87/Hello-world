# Aptech
Learning Github.com
#include <stdio.h>
#include <conio.h>
#include <process.h>

void menu(void)
{
    puts("1. Nhap mang N so thuc kieu double");
    puts("2. Tim so lon nhat va nho nhat");
    puts("3. Tinh tong cac so lon nhat va nho nhat");
    puts("4. Hien thi cac so lon nhat va nho nhat");
    puts("5. Ket thuc\n");
    puts("Nhap lua chon\n");
}

void nhap(double a[], int *n)
{
    int i;
    do
    {
	 printf("N = "); scanf("%d", n);
	 if (*n <= 0 || *n >= 100)
	      printf("Nhap lai\n");
    } while (*n <= 0 || *n >= 100);
    for (i=0; i<*n; i++)
    {
	 printf("a[%d] = ", i); 
	 scanf("%lf", a+i);
    }
}

void max_min(double a[], int n, double *max, double *min)
{
    int i;
    *max = a[0];
    *min = a[0];
    for (i=0; i<n; i++)
    {
	 if (*max < a[i])
	      *max = a[i];
	 if (*min > a[i])
	      *min = a[i];
    }
}

double tong(double max, double min)
{
    double tong;
    tong = max + min;
    return tong;
}

void in(double max, double min)
{
    printf("\nCac so lon nhat va nho nhat: %5g, %5g", max, min);
}

int main()
{
    double a[100], max, min, tg;
    int n=-1;
    char ch;
    do
    {
//	 clrscr();
	 menu();
	 ch=getch();
	 switch(ch)
	 {
	      case '1':
		    nhap(a, &n);
		    getch();
		    break;
	      case '2':
		    if (-1 == n)
			puts("File not found...");
		    else
		    {
			max_min(a, n, &max, &min);
			printf("\nSo lon nhat: %g", max);
			printf("\nSo nho nhat: %g\n", min);
		    }
		    getch();
		    break;
	      case '3':
		    if (-1 == n)
			puts("File not found...");
		    else
		    {
			tg = tong(max, min);
			printf("\ntong cac so lon nhat va nho nhat: %g\n", tg);
		    }
		    getch();
		    break;
	      case '4':
		    if (-1 == n)
			puts("File not found...");
		    else
			in(max, min);
		    getch();
		    break;
	      case '5':
		    exit(0);
	      default:
		    puts("Invalid ! Re-enter.....");
		    getch();
	 }
    } while(ch != '5');
    getch();
    return 0;
}
