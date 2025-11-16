# Valorantapi
api for valorant-api.com site for getting info about Valorant game
# main
```cpp
#include "Valorantapi.h"
#include <iostream>

int main() {
   Valorantapi api;
    auto version = api.get_version().then([](json::value result) {
        std::cout << "Search results: " << result.serialize() << std::endl;
    });
    version.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
