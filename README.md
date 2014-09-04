_stats_ is a Unix console utility which gives you a quick analysis of a set of numbers.  It is not only as simple as possible, it is even simpler: it reads data from standard input -- only -- and there are no
options or command line arguments.

## Input

A list of numbers separated by carriage returns, passed to the program by stdin.

Lines beginning with '#' are considered comments and are skipped.

## Output
* maximum (the largest item)
* mean
* median
* minimum (the smallest item)
* standard deviation
* item count
* sum (of all items)
* a [histogram](https://en.wikipedia.org/wiki/Histogram)


## Example
   If there is a file named "numbers.dat", for example, and each line of the file is a number, you would invoke stats as follows:

      cat numbers.dat | stats

   If the file "numbers.dat" contains the following items:

      1
      2
      2
      3

   Usage would look like this:

````
      bash-2.05b$ cat numbers.dat | stats
             maximum: 3
              median: 2
             minimum: 1

             average: 2
  standard deviation: 0.816496580927726
                 sum: 8
          item count: 4

           histogram:
                      |  .
                      | . .
                      |_____
````

## Graph

Explanation of the graph:

* X axis represents a unique value
* Y axis represents how many times the element occurred

In other words, it's a histogram.

For this particular set of inputs the graph shows that element counts rise from 0 to 2, then fall.

## Installation

* Download the latest version.
* Make it executable by doing "chmod 755 stats".
* Copy it to a directory in your path, e.g. /usr/local/bin.
* If perl is not installed in /usr/bin/perl on your system, you will need to change the first line of the the script from
         #!/usr/bin/perl
     to
         #!/usr/local/bin/perl
   or wherever your perl is installed.

# Contact
   <a href="mailto:lucas@gonze.com">lucas@gonze.com</a>
