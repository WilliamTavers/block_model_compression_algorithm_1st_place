# BLOCK-UG11-SEP-2024 -> Block Model Compression Algorithms
<br> 


## Table of Contents

- **[Compilation](#compilation)**
  - [Install](#install)
  - [Pre-Compiled Headers](#pre-compiled-headers)
  - [Compilation Steps (Not Including The Fast One)](#compilation-steps-not-including-the-fast-one)
  - [Compilation Steps for The Fast One](#compilation-steps-for-the-fast-one)

---

- **[The Intro One and The Real One Competitions](#the-intro-one-and-the-real-one-competitions)**
  - [Top Performers (Compression)](#top-performers-compression)
  - [Top Performers (Speed)](#top-performers-speed)
  - [Download Options](#download-options)

---

- **[The Fast One Competition](#the-fast-one-competition)**
  - [Top Performers (Compression)](#top-performers-compression-1)
  - [Top Performers (Speed)](#top-performers-speed-1)
  - [Download Options](#download-options-1)

---

- **[The Streaming One Competition](#the-streaming-one-competition)**
  - [Top Performers (Compression)](#top-performers-compression-2)
  - [Top Performers (Speed)](#top-performers-speed-2)
  - [Download Options](#download-options-2)



<br> 

---

## Compilation 

### Install

``` 
sudo apt-get install mingw-w64
```

### Pre-Compiled Headers

```
x86_64-w64-mingw32-g++ -x c++-header -o pch.h.gch pch.h
```

### Compilation Steps (Not Including The Fast One)

```
x86_64-w64-mingw32-g++ -O2 -static -msse4.2 -c CHOSEN_COMPRESSION.cpp -o CHOSEN_COMPRESSION.o

x86_64-w64-mingw32-g++ -O2 -static -msse4.2 -c main.cpp -o main.o    

x86_64-w64-mingw32-g++ -static -msse4.2 -o CHOSEN_EXE_NAME.exe CHOSEN_COMPRESSION.o main.o
```


### Compilation Steps for The Fast One

First we run the python script to get the solution in a txt file, for example pyout.txt:

```
python3 comp.py < the_fast_one.csv > pyOut.txt
```

Then we create a header file of the txt file:

```
xxd -i pyOut.txt > pyOut_txt.h
```

Then general compilation: 

```
x86_64-w64-mingw32-g++ -O2 -static -msse4.2 -c fastOne.cpp -o fastOne.o

x86_64-w64-mingw32-g++ -static -msse4.2 -o CHOSEN_EXE_NAME.exe fastOne.o
```



### Compilation Steps for System Speed Exploit for The Intro One

This program runs off of a MakeFile, move the Main.cpp and the pre-compiled headers into the same directory and then run:

```
Make
```

<br>

---

## The Intro One and The Real One Competitions

### Top Performers (Compression) 

**The Intro One** 

3D Run-Length Encoding with SIMD: 93.7958% (Comp), 184.4684% (speed) 

**The Real One** 

3D Run-Length Encoding with SIMD: 99.1690% (Comp), 720.1795% (Speed)

### Top Performers (Speed) 

**The Intro One** 

System Speed Exploit with Run-Length Encoding: 5,680,984.5485% (Speed), 72.1008% (Compression)

**The Real One** 

Run-Length Encoding with SIMD: 4,396.1663% (Speed), 92.4948% (Comp)

### Download Options 
[Download 3D Run-Length Encoding with SIMD exe](executables/b.exe) 🏆

[Download 3D Run-Length Encoding exe](executables/g.exe)

[Download 2D Run-Length Encoding exe](executables/c.exe)

[Download Run-Length Encoding in x and y direction exe](executables/i.exe)

[Download Run-Length Encoding with SIMD exe](executables/a.exe) 🏆

[Download Run-Length Encoding exe](executables/d.exe)

[Download No Compression exe](executables/j.exe)

<br>

---

## The Fast One Competition

### Top Performers (Compression) 
Memo 2x2x2 and intermediate compression: 72.0729% (Comp), 1,831.9386% (Speed)

### Top Performers (Speed) 
Memo 2x2x2 and intermediate compression: 1,831.9386% (Speed), 72.0729% (Comp)

### Download Options 
[Download memo 2x2x2 and intermediate compression for The Fast One exe](executables/h.exe) 🏆

[Download No Compression exe](executables/j.exe)

<br>

---

## The Streaming One Competition

### Top Performers (Compression) 
Run-Length Encoding for Streams Simple I/O: 	69.0494% (Comp), 426420.9067 (Speed) 

### Top Performers (Speed) 
Run-Length Encoding for Streams Simple I/O: 454382.9333 (Speed), 67.5550% (Comp),

### Download Options 
[Download Run-Length Encoding for Stream Processor Using StringStreams exe](executables/e.exe)

[Download Run-Length Encoding for Streams Simple I/O exe](executables/k.exe) 🏆

[Download No Compression for Stream Processor exe](executables/f.exe)
