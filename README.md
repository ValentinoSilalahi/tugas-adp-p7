#include <iostream>
#include <math.h>

using namespace std;

int main()
{
    cout << " Nama : Valentino Silalahi " << endl;
    cout << " Nim  : 2310431015 " << endl;
    cout << " Program Tabel Fungsi " << endl;

    char ulang ='Y' ;
    while ( ulang=='Y' || ulang=='y' ) {

    cout << endl << "==================================================" << endl;
    cout << "                  TABEL FUNGSI" << endl;
    cout << "==================================================" << endl;

    int n,i;

    cout << endl << " Masukkan banyak data : ";
    cin >> n;

    int x[n];
    float f[n],g[n],h[n];

    cout << endl << " Inputkan " << n << " buah data : " << endl;
    for ( i=0; i<n; i++ ) {
        cout << " Input nilai x ke-" << i+1 << " = ";
        cin >> x[i];

        if ( x[i] >= 0 ) { f[i] = (3*(x[i] *x[i])) + (7*x[i] ) - 2; }
        if ( x[i] < 0 ) { f[i] = (2*(x[i] *x[i] )) - (5*x[i] ) - 4; }
        g[i] = (f[i]*f[i]) - sqrt(f[i] );
        h[i] = f[i] * g[i] ;
    }

    cout << "\nNo \tx \tf(x) \t g(x) \t    h(x) \n";
    for ( i=0; i<n; i++ ) {
        cout << i+1 << "\t" << x[i] << "\t" << f[i] << "\t" << g[i] << "\t   " << h[i] <<endl;
    }

    cout << " Mau ulang lagi [Y/T] : ";
    cin >> ulang;
  }
}

