# Massivke_esep
Palindrom_sandardy_anyqtau

    #include <iostream>
    using namespace std;

    int main()
    {
    bagdarlama_basy:
    int n, c;
    cout << "Massivke olshem beriniz: n=";
    cin >> n;
    int a[100];
    for (int i = 0; i < n; i++) {
        cout << "a[" << i << "]=";
        cin >> a[i];
    }
    for (int i = 0; i < n; i++) {
        int p = 0;
        c = a[i];
        while (a[i] > 0) {
            int k = a[i] % 10;
            p = p * 10 + k;
            a[i] /= 10;
            if (p == c)cout << "Palindrom san " << p << endl;

            else {
                cout << "Palindrom sandar joq, sandardy janadan engiziniz; " << endl; \
                    goto bagdarlama_basy;
            }
        }
    }
    }
