# mswitch
C++ multiple-test switch synthax

## Usage example
```C++
#include <mswitch> /* mswitch, mcase */
#include <iostream> /* std::cout */

int main(void)
{
    int a = 42;
    int b = a/2;
    double f = 1.618;
    double pi = 3.1416;

    mswitch(a > b, f > pi)
    {
    mcase(true, true):
        std::cout << "a > b, f > pi" << std::endl;
        break;
    mcase(true, false):
        std::cout << "a > b, f <= pi" << std::endl;
        break;
    mcase(false, true):
	      std::cout << "a <= b, f > pi" << std::endl;
        break;
    mcase(false, false):
	      std::cout << "a <= b, f <= pi" << std::endl;
        break;
    }
    return 0;
}
```
