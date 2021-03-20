# iotest
Script for testing of the first IOS project.

## Setup
Copy all the files into one folder with your tradelog script.

## Usage
To run the test, execute this command

```
$ ./iotest
✓ test-cases/01: cat stock-2.log | head -n 5 | ./tradelog
✓ test-cases/02: ./tradelog -t TSLA -t V stock-2.log
✓ test-cases/03: ./tradelog -t CVX stock-4.log.gz | head -n 3
✓ test-cases/04: ./tradelog list-tick stock-2.log
✓ test-cases/05: ./tradelog profit stock-2.log
✓ test-cases/06: ./tradelog -t TSM -t PYPL profit stock-2.log
✓ test-cases/07: ./tradelog pos stock-2.log
✓ test-cases/08: ./tradelog -t TSM -t PYPL -t AAPL pos stock-2.log
✓ test-cases/09: ./tradelog last-price stock-2.log
✓ test-cases/10: ./tradelog hist-ord stock-2.log
✗ test-cases/11: ./tradelog -w 100 graph-pos stock-6.log
✗ test-cases/12: ./tradelog -w 10 -t FB -t JNJ -t WMT graph-pos stock-6.log
✓ test-cases/13: cat /dev/null | ./tradelog profit
Some tests failed. Run with -v to see their output.
You can also check the test case folder to see the actual and expected output files.
```

You can also include `-v` flag to print the output, if any test fails.

## Test cases
Test cases 01-13 are copied from project specification.
Cases 14 and up are custom, but they should still conform to the spec.

If you want to make your own test cases, you can just add it into `test-cases` folder. Every use case has its own folder with given command to run and correct output.
The command is stored in the `in.txt` file.
The reference output is stored in the `out.txt` file
After the test is run, `test_output.txt` is created. In it you can find the actual output of your program.
