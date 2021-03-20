# iotest
Script for testing of the first IOS project.

## Setup
Copy all the files into one folder with your tradelog script.

## Usage
To run the test, execute this command

```./iotest```

You can also include `-v` flag to print the output, if any test fails.

If you want to make your own test cases, you can just add it into `test-cases` folder. Every use case has its own folder with given command to run and correct output.
The command is stored in the `in.txt` file.
The reference output is stored in the `out.txt` file
After the test is run, `test_output.txt` is created. In it you can find the actual output of your program.
