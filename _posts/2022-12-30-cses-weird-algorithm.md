---
layout: post
title:  "CSES Weird Algorithm"
date:   2022-12-30 03:33:07 +0530
categories: programming
tags: ["CP", "CompetitiveProgramming", "Programming", "cpp"]
---

#### Problem: [CSES Weird Algorithm](https://cses.fi/problemset/task/1068/)

#### Description: 
* As the problem statement mentions, if n is even, we divide it by 2 otherwise we multiply by 3 and add 1.
* We need to take care that the data type for N is 64 bits long. Some test cases fail if we use an int which is 32 bits.

#### Solution:

{% highlight cpp %}
#include <iostream>

using namespace std;

int main() {
    int64_t n;
    cin >> n;

    while(n != 1) {
        cout << n << " ";
        if(n % 2 == 0) {
            n /= 2;
        } else {
            n = ((n*3) + 1);
        }
    }
    cout << 1 << "\n";
}
{% endhighlight %}