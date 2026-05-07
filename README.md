# BASIC-256
Basic programming using [BASIC-256](https://basic256.org/)

## First test of BASIC-256

Using the graphics output and measuring the execution time.

The code: [test256.kbs](test256.kbs)

The IDE of BASIC-256 with the program:

![test256_list.png](test256_list.png)

The output saved to PNG by the program:

![test256.png](test256.png)

## Julia Fractal

Drawing a Julia fractal. The code takes about 21s to complete. It calculates half of the fractal and plots the other half from the same data using symmetry.

The code: [julia.kbs](julia.kbs)

The output saved to PNG by the program:
![julia256.png](julia256.png)

## Minsky Circle Algorithm

Drawing a circle using only addition, subtraction and integer division.

The main loop:

    x=1024: y=0 # initial values
    do
        x = x - y\32 # using integer division
        y = y + x\16 # new value of x has to be used
	    x = x - y\32 # 3rd step to reduce phase error
		plot(x,y)
    until x=1024 and y=0 # until back to initial values

The integer division by powers of 2 could be done using bit shift to the right also.

Using info from: ["Drawing Circles · Hrvoje's Blog"](https://blog.hrvoje.org/2020/05/drawing-circles/)

The code: [minsky.kbs](minsky.kbs)

![minsky.png](minsky.png)


