# CS 70 Array-Bounds Example

You need to work with this code in Visual Studio Code. Do the following:

* On GitHub, click the white “Code” button and copy the URL (note it's *not* the green “Template” button but the one to the left of it).
* Start Docker Desktop (all CS 70 tools are in the folder at the top left of the screen)
    * You don't need to double click it more than once!
* In VS Code, either 
    * Click the “Clone Repository” button on the start screen, paste in the URL, and click “Clone”, or
    * Press Command+Shift+P to open the Command Palette and type “Git: Clone” as the command, paste in the URL, and press Enter.
* VS code will ask you where to put the repository. Choose a good place (like the Documents folder), and then ask you if you want to open it. Click “Open”.
* VS Code will ask you if you trust the authors of the code. Say yes.
* VS Code will ask you if you want to open the repository in a container. Click “Reopen in Container”.
* VS Code will then spin for a while as the container is downloaded, but eventually it will open up the code.
* Select `arrays.cpp` in the file list on the left to see the code.
    * There are instructions in the comments in the code. Follow them to see what happens when you run the code in different scenarios.
    * When you need a Terminal in VS code, either select Terminal -> New Terminal from the menu bar, or press Command+Shift+` (that's the backtick, not a single quote). You can then type commands in the terminal.

As a reminder (and for easy copy-and-pasting), once you have the code open in VS code, you can build and run the code by running:

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