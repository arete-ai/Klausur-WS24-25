# Klausur-WS24-25

1. Cheat Sheet mit Syntaxelementen 
Schleifen:  

// For-Schleife  
for (int i = 0; i < n; i++) { /* Code */ }  

// While-Schleife  
while (bedingung) { /* Code */ }  

// Do-While-Schleife  
do { /* Code */ } while (bedingung);  


Bedingungen:  

// If-Else  
if (x > 0) { /* Code */ }  
else if (x == 0) { /* Code */ }  
else { /* Code */ }  

// Switch-Case  
switch (variable) {  
    case 1: /* Code */ break;  
    case 2: /* Code */ break;  
    default: /* Code */  
}  


Funktionen:  

// Definition  
Rückgabetyp funktionsname(Parameter) {  
    // Code  
    return wert;  
}  

// Beispiel: Summe  
int sum(int a, int b) { return a + b; }  













Arrays & Zeiger: 

int arr[5];                   // Statisches Array  
int* dynArr = new int[5];     // Dynamisches Array  
delete[] dynArr;              // Speicher freigeben  

int* ptr = &arr[0];           // Zeiger auf Array  
const int* constPtr = arr;    // Konstanter Zeiger  

Mehrdimensionale Arrays:

int arr[2][3] = {{1, 2, 3}, {4, 5, 6}}; 
for (int i = 0; i < 2; i++) { 
	for (int j = 0; j < 3; j++) { 
		cout << "arr[" << i << "][" << j << "] = " << arr[i][j] << endl; } 


`const` und `static`: 

const int MAX = 100;          // Konstante Variable  
static int counter = 0;       // Statische Variable (lebt über Funktionsaufrufe)  


---

2. Häufige Bibliotheksfunktionen  
Eingabe/Ausgabe (`<iostream>`):  

cout << "Text" << variable << endl;  // Ausgabe  
cin >> variable;                     // Eingabe  
cerr << "Fehler!";                   // Fehlerausgabe  


Mathematik (`<cmath>`):  

sqrt(x);      // Quadratwurzel  
pow(x, y);    // x^y  
abs(x);       // Betrag  
ceil(x);      // Aufrunden  
floor(x);     // Abrunden  


Strings (`<string>`):  

string s = "Hallo";  
s.length();             // Länge  
s.substr(start, len);   // Teilstring  
s.find("text");         // Suche (gibt Position zurück)  
```



Container (`<vector>`):  

vector<int> v;  
v.push_back(5);         // Element hinzufügen  
v.size();               // Anzahl der Elemente  
v.at(0);                // Zugriff mit Prüfung  


Algorithmen (`<algorithm>`):  

sort(v.begin(), v.end());          // Sortieren  
max_element(v.begin(), v.end());   // Größtes Element  
min_element(v.begin(), v.end());   // Kleinstes Element  


Zufallszahlen (`<cstdlib>`):  

srand(time(0));                   // Seed setzen  
int zufall = rand() % 100 + 1;    // Zufallszahl zwischen 1-100  


---

3. Code-Vorlagen für komplexe Algorithmen  
Rekursion:  

// Fakultät  
int fakultaet(int n) {  
    return (n <= 1) ? 1 : n * fakultaet(n - 1);  
}  

// Fibonacci  
int fib(int n) {  
    return (n <= 1) ? n : fib(n - 1) + fib(n - 2);  
}  


Sortieren:

// Bubble Sort  
for (int i = 0; i < n; i++) {  
    for (int j = 0; j < n - i - 1; j++) {  
        if (arr[j] > arr[j + 1]) swap(arr[j], arr[j + 1]);  
    }  
}  






Suchen: 

// Lineare Suche  
int linearSearch(int arr[], int size, int key) {  
    for (int i = 0; i < size; i++) {  
        if (arr[i] == key) return i;  
    }  
    return -1;  
}  



Dynamische Speicherverwaltung:  

int* createArray(int size) {  
    int* arr = new int[size];  
    return arr;  
}  
// Vergiss nicht: delete[] arr;  


Dateiverarbeitung (`<fstream>`):  

// Lesen  
ifstream input("datei.txt");  
string line;  
while (getline(input, line)) { /* Code */ }  

// Schreiben  
ofstream output("datei.txt");  
output << "Daten";  


Palindromprüfung:  

bool isPalindrom(const string& s) {  
    int left = 0, right = s.length() - 1;  
    while (left < right) {  
        if (s[left++] != s[right--]) return false;  
    }  
    return true;  
}  


---

Tipps für die Klausur: 
- Formatierung: Nutze `setw()`, `right`, und `fixed` für Tabellen.  
- Fehlerbehandlung: Prüfe immer auf `size <= 0`, `nullptr`, und Division durch Null.  
- Effizienz: Vermeide unnötige Kopien (z. B. mit `const&` bei Vektoren).
