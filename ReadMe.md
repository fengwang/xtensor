# __XTENSOR__ in a single header file.


Putting <https://github.com/nlohmann/json>, <https://github.com/xtensor-stack/xsimd> and <https://github.com/xtensor-stack/xtl> together with <https://github.com/xtensor-stack/xtensor>, for easy of use. (dating 2020.08.03)

```bash
cat `nlohmann/json` `xtensor-stack/xsimd` `xtensor-stack/xtl` `xtensor-stack/xtensor` > `fengwang/xtensor`
```


## Dependency:
- [Intel TBB](https://github.com/oneapi-src/oneTBB)


## Example Code:

All `<xtensor-stack/xtensor>` code should work by simply copying the header file `xtensor.hpp` in this repo  and adding `#include "xtensor.hpp"` to your cpp source code:
```cpp
//test.cc
#include "xtensor.hpp"
#include <iostream>

int main()
{
    xt::xarray<double> arr1
    {
        {1.0, 2.0, 3.0},
        {2.0, 5.0, 7.0},
        {2.0, 5.0, 7.0}};
    xt::xarray<double> arr2
    {5.0, 6.0, 7.0};
    xt::xarray<double> res = xt::view( arr1, 1 ) + arr2;
    std::cout << res std::endl;;
    return 0;
}
```

## Simple Compilation Command:
```bash
g++ -o test test.cc -std=c++2a -O2 -Wall -ltbb
```
## Documentation

Refer to [xtensor-stack/xtensor](http://xtensor.readthedocs.io/)


