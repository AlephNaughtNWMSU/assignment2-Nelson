# Sam Nelson
I always feel awkward when I am tasked to provide interesting facts about myself (one of my facts). I am tall but bad at basketball. I have a sizable coin collection. I am doing this assignment the morning that it's due. I enjoy looking at maps. I figure that six sentences qualifies as a pargagraph. 

![Image of park](image.gif)

--- 

### Table of Recommendations

These are four food and drink items that I recommend that someone should try. I think these food and drink items are ones that most people are familiar with but are still worthwhile to imbibe.

| Food/Drink Item | At | Cost |
| --- | --- | ---: |
| Kemps Vanilla Ice Cream| Maryville Walmart | $3.50 |
| Sonic Chocolate Milk Shake | Maryville Sonic | $4.00 |
| Reese's Peanut Butter Cup | Maryville Hyvee | $0.75 |
| Ali's Bakery Donut | Maryville (6th & Main) | $1.00 |

--- 

### Quotes

> I know not what course others may take; but
as for me, give me liberty or give me death!
*Patrick Henry*

> Father, forgive them; for they know not what they do (Luke 23:34)
*Jesus the Christ*

---

### Code Fencing - Algorithm
##### Sqrt Decomposition
> Sqrt (or Square Root) Decomposition Technique is one of the most common query optimization technique used by competitive programmers. This technique helps us to reduce Time Complexity by a factor of sqrt(n). *GeeksForGeeks.org*
[Source](https://www.geeksforgeeks.org/sqrt-square-root-decomposition-technique-set-1-introduction/)

~~~
// input data
int n;
vector<int> a (n);

// preprocessing
int len = (int) sqrt (n + .0) + 1; // size of the block and the number of blocks
vector<int> b (len);
for (int i=0; i<n; ++i)
    b[i / len] += a[i];

// answering the queries
for (;;) {
    int l, r;
  // read input data for the next query
    int sum = 0;
    for (int i=l; i<=r; )
        if (i % len == 0 && i + len - 1 <= r) {
            // if the whole block starting at i belongs to [l, r]
            sum += b[i / len];
            i += len;
        }
        else {
            sum += a[i];
            ++i;
        }
}
~~~
[Source Code](https://cp-algorithms.com/data_structures/sqrt_decomposition.html)
