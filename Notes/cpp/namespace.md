позволяет создавать "пространство имён"
``` cpp
namespace First {
	int a = 1;
	namespace Second {
		int a = 2;
	}
}
```

Эти пространства можно использовать вот так:
``` cpp
#include<iostream>
using namespace std;
cout << "теперь не надо писать std::";

using namespace First;
cout << a << " " << Second::a; // 1 2

using namespace Second;
cout << a; // 2
```