#include <cmath>
#include <iostream>

using namespace std;

auto asalMi(int sayi) -> bool
{
    if (sayi < 2)
        return false;
    if (sayi == 2)
        return true;
    if (sayi % 2 == 0)
        return false;

    for (int i = 3; i <= sqrt(sayi); i += 2) {
        if (sayi % i == 0)
            return false;
    }

    return true;
}

auto girilenSayiGecerliMi(int girilenSayi) -> bool
{
    if (girilenSayi <= 2 || girilenSayi % 2 != 0) {
        return false;
    } else
        return true;
}

int main()
{
    int girilenSayi;
    int x;

    cout << "Goldbach hipotezi kontrolu icin 2'den buyuk bir cift sayi giriniz: ";
    cin >> girilenSayi;

    if (!girilenSayiGecerliMi(girilenSayi)) {
        cout << "Hata: Gecersiz sayi. Lutfen 2'den buyuk bir cift sayi giriniz." << endl;
        return 0;
    }

    for (int i = 0; i < int(girilenSayi / 2) + 1; i++) {
        x = girilenSayi - i;

        if (asalMi(x) && asalMi(i)) {
            cout << i << " + " << x << endl;
        }
    }
}
