#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 100; i++) {
        if (i % 3 == 0 && i % 5 == 0) {
            cout << "FizzBuzz" << endl;
        } else if (i % 3 == 0) {
            cout << "Fizz" << endl;
        } else if (i % 5 == 0) {
            cout << "Buzz" << endl;
        } else {
            cout << i << endl;
        }
    }
    return 0;
}
 

2. Triangle Type Program

 
#include <iostream>
using namespace std;

int main() {
    float a, b, c;

   // Input sides of the triangle
    cout << "Enter the lengths of three sides of the triangle: ";
    cin >> a >> b >> c;

   // Check if a triangle can be formed
    if (a + b > c && a + c > b && b + c > a) {
        cout << "A triangle can be formed." << endl;

   // Check for type of triangle
        if (a == b && b == c) {
            cout << "The triangle is Equilateral." << endl;
        } 
        else if (a == b || b == c || a == c) {
            cout << "The triangle is Isosceles." << endl;
        } 
        else {
            cout << "The triangle is Scalene." << endl;
        }
    } else {
        cout << "A triangle cannot be formed." << endl;
    }

   return 0;
}
 

3. Largest Digit Program

 
#include <iostream>
using namespace std;

int main() {
    int number, largest_digit = 0;
    cout << "Enter a number: ";
    cin >> number;

   while (number > 0) {
        int digit = number % 10;
        if (digit > largest_digit) {
            largest_digit = digit;
        }
        number /= 10;
    }

   cout << "The largest digit is: " << largest_digit << endl;
    return 0;
}
 

4. Decimal to Binary and Octal Conversion

 
#include <iostream>
using namespace std;

int main() {
    int decimal;
    cout << "Enter a decimal number: ";
    cin >> decimal;

   // Binary conversion
    cout << "Binary: ";
    for (int i = 31; i >= 0; i--) {
        cout << ((decimal >> i) & 1);
    }
    cout << endl;

   // Octal conversion
   cout << "Octal: ";
    int octal = 0, place = 1;
   while (decimal) {
        octal += (decimal % 8) * place;
        decimal /= 8;
        place *= 10;
    }
    cout << octal << endl;

   return 0;
}
 

5. Perfect Number Check

 
#include <iostream>
using namespace std;

int main() {
    int number, sum = 0;
    cout << "Enter a number: ";
    cin >> number;

   for (int i = 1; i < number; i++) {
        if (number % i == 0) {
            sum += i;
        }
    }

   if (sum == number) {
        cout << number << " is a Perfect Number." << endl;
    } else {
        cout << number << " is not a Perfect Number." << endl;
    }

   return 0;
}
 

6. Pattern Program (n=3)

 
#include <iostream>
using namespace std;

int main() {
    int n = 3;
    for (int i = n; i >= 1; i--) {
        for (int j = 1; j <= i; j++) {
            cout << j;
        }
        cout << endl;
    }
    return 0;
}
 

7. Pattern Program (n=4)

 
#include <iostream>
using namespace std;

int main() {
    int n = 4;
    for (int i = 1; i <= n; i++) {
        for (int j = 1; j <= i; j++) {
            cout << j << "*";
        }
        cout << endl;
    }
    return 0;
}

8. Pattern Triangle type(n=4) 

#include <iostream>

int main() {
    int n = 4; // You can change this value for different sizes

   // Loop through rows
    for (int i = 1; i <= n; ++i) {
        // Print left side of the pattern
        for (int j = 1; j <= i; ++j) {
            std::cout << j;
        }
        
   // Print right side of the pattern
        if (i > 1) {
            for (int j = i; j >= 1; --j) {
                std::cout << j;
            }
        }

   // Move to the next line after each row
        std::cout << std::endl;
    }

   return 0;
}
