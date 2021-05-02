Credit Approval Data Set
Download: Data Folder, Data Set Description

Abstract: This data concerns credit card applications; good mix of attributes

Data Set Characteristics:  

Multivariate

Number of Instances:

690

Area:

Financial

Attribute Characteristics:

Categorical, Integer, Real

Number of Attributes:

15

Date Donated

N/A

Associated Tasks:

Classification

Missing Values?

Yes

Number of Web Hits:

490205


Source:

(confidential source)

Submitted by quinlan '@' cs.su.oz.au


Data Set Information:

This file concerns credit card applications. All attribute names and values have been changed to meaningless symbols to protect confidentiality of the data.

This dataset is interesting because there is a good mix of attributes -- continuous, nominal with small numbers of values, and nominal with larger numbers of values. There are also a few missing values.


Attribute Information:

A1: b, a.
A2: continuous.
A3: continuous.
A4: u, y, l, t.
A5: g, p, gg.
A6: c, d, cc, i, j, k, m, r, q, w, x, e, aa, ff.
A7: v, h, bb, j, n, z, dd, ff, o.
A8: continuous.
A9: t, f.
A10: t, f.
A11: continuous.
A12: t, f.
A13: g, p, s.
A14: continuous.
A15: continuous.
A16: +,- (class attribute)






README
 Files in the 'data/card' directory:
=========================================

This dataset is from the UCI machine learning database:
"credit-screening"

[Remark: some of the generated files may not exist in order to save disk space]

crx.names
  Original documentation for the dataset

crx.data
  Original data file

crx.raw
  Symbolic ling to crx.data

crx.cod
  crx.raw encoded (using raw2cod)

header
  Header lines used in .dt files

crx?.dt
  different permutations of the lines of cod file plus the header lines

raw2cod
  Perl script for format conversions:
  takes xx.raw as input and produces xx.cod as output according
  to the rules given in section 'design' below.

Makefile
  Makefile to call scripts and programs to create .dt files


 
 Encoding:
===========

This is credit card approval data. For confidentiality, all attributes
and values are unexplained in the original data set.

Class distribution:
 granted: 307 (44.5%)
 denied : 383 (55.5%)
 total  : 690

There are 15 input attributes of very different kinds.
For 7 of them, there are a few missing values (in 37 (=5%) of the records).
We encode all these misses explicitly (using 51 instead of 43 inputs).
Of attribute 14, the logarithm has to be used in order for the attribute
to be useful.

Resulting encoding:

0. binary, values: b, a, ?.   (12 missing)
  3  b="1 0 0", a="0 1 0", ?="0 0 1"
1. continuous, values 13.75...80.25     (12 missing)
  2
2. continuous, values 0...28
  1
3. nominal, values: u, y, l, t, ?.   (6 missing)
  5
4. nominal, values g, p, gg, ?.   (6 missing)
  4
5. nominal, values c, d, cc, i, j, k, m, r, q, w, x, e, aa, ff, ?. (9 missing)
 15
6. nominal, values v, h, bb, j, n, z, dd, ff, o, ?.   (9 missing)
 10
7. continuous, values 0...28.5
  1
8. binary, values t, f.
  1
9. binary, values t, f.
  1
10. continuous, values 0...67
  1
11. binary, values t, f.
  1
12. nominal, values g, p, s
  3
13. continuous, values 0...2000    (13 missing)
  2
14. continuous, values 0...100000 (must be log-transformed to be useful)
  1
-------
 51 inputs

15. binary, values: +, -
  2:  +="1 0", -="0 1"
--------
  2 outputs
