# Self Assessment of Programming Skills for ECE-573 Applied Data Structures and Algorithms

For this course you must be able to write and debug C++ code.
Each question contains code in both C++ and Java. Pick the language you know and attempt to solve.
If you are not comfortable with this level of programming, please study C++ before attempting ECE-573. I am conducting a review first week, and will record it for future classes. If that's enough to get you going, great.

1. The following code should compute the sum 1 + 3 + ... + 51 but it is wrong. Fix the loop so it works, then rewrite it without an if statement so it is faster.

    You should not have to ask if your answer is correct. You can test with a smaller number if necessary. For example:
    1+3+5 = 9, so you can test with 5 instead of 51.

      ```c
      int sum = 0;
      for (int i = 0; i < 51; i++)
        if (i % 2 == 0)
          sum = i;
      cout << sum << '\n';
      ```

2. The following code crashes. Explain why.

    ```c
    int main() {
      int a[100];
      for (int i = 0; i < 10000; i++)
        cout << a[i] << '\n';
    }
    ```

3. Write a list class holding integers implementing the following
  C++

  ```c
    class MyList {
    private:
      int* data;         // pointer to a block of memory holding the data
      uint32_t len;      // the number of elements in the list
      uint32_t capacity; // the size of the block of memory allocated
      // complete whatever is needed so this class runs correctly
    };
    int main() {
      MyList a; // create an empty list (len=0, capacity = 1)
      MyList b(100) // create an empty list with capacity = 100
      a.addEnd(3); // put the number 3 at the end of the list and increase len by 1
      // write destructor to give back the memory
      MyList c = a; // copy a into c using the copy constructor
      MyList d(a); // alternate form of calling the copy constructor
      b.add(4);
      c = b; // destroy the memory in c, then copy b implementing the operator =
      cout << c << '\n'; // print the list
    }
  ```


## [&larr; Return and Finish](readme.md)
