---
title: pointer
layout: page
---
# pointer

1. サンプルプログラムを打ち込む
2. メモリマップを描く

<!-- 箱でイメージしてる人は今日からそのイメージ捨ててください -->
<!-- TODO 先生の作ったプログラムを自作に置き換える -->

```C

/*
 * List 10_2
 */
#include <stdio.h>

int main ( void ) {
    int n = 100;
    double x = 3.141592;
    int a[3] = { 1024, 2048, 4096 };
    int * n_ptr;
    
    printf( "\n" );
    printf( "n = %d : addr = %p (size:%u) \n",
            n, &n, sizeof(n));
    printf( "x = %f : addr = %p (size:%u) \n",
            x, &x, sizeof(x));
    
    printf( "\n" );
    printf( "a[0] = %d : addr = %p (size:%u) \n",
            a[0], &a[0], sizeof(a[0]) );
    printf( "a[1] = %d : addr = %p (size:%u) \n",
            a[1], &a[1], sizeof(a[1]) );
    printf( "a[2] = %d : addr = %p (size:%u) \n",
            a[2], &a[2], sizeof(a[2]) );
    printf( "array of int a: addr = %p (size:%u)\n",
            a, sizeof( a ) );
    
    n_prt = &n;
    printf( "n_ptr = %p : addr = %p (size:%u) \n",
            n_ptr, &n_ptr, sizeof(n_ptr));

    return 0;
}

```

```
n = 100 : addr = 0xbf86f798 (size:4)
x = 3.141592 : addr = 0xbf86f790 (size:8)

a[0] = 1024 : addr = 0xbf86f784 (size:4)
a[1] = 2048 : addr = 0xbf86f788 (size:4)
a[2] = 4096 : addr = 0xbf86f78c (size:4)
array of int a: addr = 0xbf86f784 (size:12)
n_ptr = 0xbf86f798 : addr = 0xbf86f79c (size:4)
```

| address  | value | size |
|:---------|------:|------|
|0xbf86f798|100|4|
|0xbf86f790|3.141592|8|
|0xbf86f784|1024|4|
|0xbf86f788|2048|4|
|0xbf86f78c|2048|4|
|0xbf86f79c|0xbf86f798|4|


