# Fast-BigDouble

This source code is a fork of BreakInfinity that has been modified for idle games that use very large numbers.

## Why Fast?
While double.Parse and double.ToString are great for their versatility, they are very slow in special situations.

In games that use large numbers, such as idle games, you don't need to care as much about the accuracy of floating-point numbers, so it's a performance advantage to create your own algorithm to parse double.

## How to Use?
It is exactly the same as BigInfinity.cs, but it must follow these rules

Simple.
```cs
FastBigDouble _ = new BigDouble("1000");
FastBigDouble _ = new BigDouble("1.0A");
FastBigDouble _ = new BigDouble("999.9A");
FastBigDouble _ = new BigDouble("1000A"); // It's Error. Alphabet Number Allow -999.9~999.9 for performance.
FastBigDouble _ = new BigDouble("9.999e100"); // It's Very Fast!
FastBigDouble _ = new BigDouble("100e100"); // It's Error. If you want exponent style mantissa allow -9.99999999d~9.99999999d


new FastBigDouble(1e3).ToString() // Result = "1.0A"
```


