<h1 align="center">
  <br>
  <a href="https://github.com/s0md3v/fonetic"><img src="https://i.ibb.co/KctQhzN/phonetic.png" alt="fonetic"></a>
  <br>
  Fonetic
  <br>
</h1>

<h4 align="center">Calculate pronounciblity of text</h4>

<p align="center">
  <a href="https://github.com/s0md3v/fonetic/releases">
    <img src="https://img.shields.io/github/release/s0md3v/fonetic.svg">
  </a>
  <a href="https://github.com/s0md3v/fonetic/issues?q=is%3Aissue+is%3Aclosed">
      <img src="https://img.shields.io/github/issues-closed-raw/s0md3v/fonetic.svg">
  </a>
</p>


### Introduction
Fonetic is a python library to caculate assess pronounceablility of a given text based on an algorithm . It may be used in:

- Detecting randomly generated strings
- Heuristic checking for spell checkers
- Improving made-up word generators
- Optimizing brute-force attacks


Open an [issue](https://github.com/s0md3v/fonetic/issues) to extend this list.

**fonetic** has only 33 lines of executable code which is optimized to the boolean level.
It has no external imports and it can be used with any Python version and operating system.

### Installation
The recommended method to install **fonetic** is using `pip`, as follows:

```
pip install fonetic
```

### Documentation

fonetic is minimal and can be implemented in just 2 lines of code as follows:

```python
>>> from fonetic import count
>>> count('christmxs')
(8, 6, 2)
```

The output is a tuple containing values of total bigrams, pronounceable bigrams and unpronounceable bigrams respectively.

### Benchmarking
The python script and related files used for benchmarking can be downloaded from [here](https://github.com/s0md3v/MyPapers/blob/master/A%20Phonetic%20Approach%20to%20Calculate%20Linguistic%20Information%20in%20Text/phonetic-flow-chart.png)

The result below was produced by parsing a 4.3 MB text file containing the entire oxford dictionary with a 3GB RAM and a 4th Gen intel i3 processor.

```
~> python benchmark.py /root/oxford.txt

---Result---
- Text length: 4478566 bytes
- English text length: 3262241 bytes
- Total valid bigrams: 2566359
- Pronounceable bigrams: 2533266
- Unpronounceable bigrams: 33105
- Meaningful text: 98%

---Benchmark---
- Parsing started: 1577194614
- Parsing ended: 1577194616
- Time taken: 2 seconds
```

The error of 2% in Oxford dictionary was unexpected but manual checking revealed that it was caused by abbreviations and words from other languages. Such an entry is given below:

```
zygote  n. biol. cel
. biol. cell formed by the union of two
two gametes. [greek zugotos yoked: relat
tes. [greek zugotos yoked: related to *z
yoked: related to *zeugma]
```
