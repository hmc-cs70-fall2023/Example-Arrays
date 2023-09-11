# CS 70 Array Example

Load the code into Visual Studio, look at the comments and follow the instructions. (Be sure to click “Reopen in Container” when it comes up so that it uses the CS 70 docker image.)

As a reminder, you can build and run the code by running:

    clang++ -std=c++17 -Wall -Wextra -pedantic -c arrays.cpp
    clang++ -o arrays arrays.o
    ./arrays


## Extra Bonus Fun for Lab

_**Note:** Only do this after you've done everything described in `arrays.cpp`._

Try running the code on a different processor architecture. Docker can simulate this, but you'll need to use a terminal rather than VS Code.

Open a Mac Terminal, and then run:

    cd whatever-directory-you-used/Example-Arrays
    docker run --platform linux/arm64 -v "$(pwd):/home/student/cs70/" -it 'harveymudd/cs70-student:spring2023-arm64' /bin/zsh

to start up an ARM64 docker image.

Then run:

    clang++ -std=c++17 -Wall -Wextra -pedantic -c arrays.cpp
    clang++ -o arrays arrays.o
    ./arrays

and compare the results against the ones you saw in VS Code.