# square-root
how to get the square root of the number 

#include using namespace std;

int main() { double number; cout << "Enter a number to find its square root: "; cin >> number;

if (number < 0) {
    cout << "Square root of negative number is not real." << endl;
    return 0;
}

double guess = number / 2.0; // Initial guess
double epsilon = 0.00001;   // Precision level

while ((guess * guess - number) > epsilon || (guess * guess - number) < -epsilon) {
    guess = (guess + number / guess) / 2.0; // Newton's formula
}

cout << "Square root of " << number << " is approximately " << guess << endl;

return 0;
}
