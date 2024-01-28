# **Testing C, C++ Compilers**

------

We will be moving forward assuming that you have already followed the manual on how to install Ubuntu and C, C++ compilers on Virtual Box.

- ## Step 1:  **How to create a File**

   Note that when its your first time creating a file, **by default,** when we **right-click** inside anywhere in the Ubuntu file manager, it will not give us the “New document” option. We must do the following steps to achieve this.

   To get this **missing** option, we need to run a command.

   1. Open **Ubuntu command** terminal.

   2. Run commands

     ```
     mkdir -p ~/Templates/Text
     cd ~/Templates/Text
     touch document
     ```

     ![documentOption](.\images\documentOption.png)

     

   3. Now, go to your **Linux File Manager** or **Desktop** and **right-click** where you want to **create a new file** and the option will be available.

   4. Select **New Document** and then **Text Document**.

     ![optionAvailable](.\images\optionAvailable.png)

     

   5. This will instantly create a new text file on your Linux OS.

     

- ## Step 2:  **Using C Language Compiler**

   1. **Create a new file** and rename it to **test.c**.

   ![rename](.\images\rename.png)

     
   
   2. **Double-click** to open the file.

   3. **Write a sample C language code** in the file. For example:

     ```
     #include<stdio.h>
     
     void main() 
     {
     	printf("Hello! This is my first C program with Ubuntu\n");
     	int a=3,b=7;
     	printf("%d is the sum of a and b", a+b);
     }
     ```

     ![exampleCode](.\images\exampleCode.png)

     

   4. Open the **Linux terminal**(**`Ctrl + Alt + T`**) and enter the following commands to compile and run this code (**You must first enter the directory where you have created the file** using the "**cd ~/**" command).

     **To Compile:**

     ```
     gcc -o obj test.c
     ```

     **To Run:**

     ```
     ./obj
     ```

     ![runProgram](.\images\runProgram.png)

     

- ## Step 3:  **Using C++ Language Compiler**

   1. **Repeat the same procedure as Step 2** with few changes.

   2. **Create a new file** and rename it to **test.cpp**.

     ![cppRename](.\images\cppRename.png)

     
   
   3. **Double-click** to open and **write a sample C++ language code** in the file. For example:

     ```
     #include<iostream>
     using namespace std;
     
     int main()
     {
         cout << “Testing G++ Compiler!!!!!!!” << endl;
         cout << “Yes, G++ Compiler working Perfectly!!!!!!!” << endl;
         int a=3,b=7;
         cout << a+b << " is the sum of a and b";
     
         return 0;
     }
     ```

   4. Open the **Linux terminal**(**`Ctrl + Alt + T`**) and enter the following commands to compile and run this code (**You must first enter the directory where you have created the file** using the "**cd ~/**" command).

     **To Compile:**

     ```
     g++ -o obj test.c
     ```

     **To Run:**

     ```
     ./obj
     ```

     ![runProgramC++](.\images\runProgramC++.png)

   ------

     We are now done with the **running** and **testing** of both the compilers and successfully executing **C and C++ programs**.

# **GitHub Repository Link**

------

**2022-CS-214	Muhammad Aanish Naveed	[https://github.com/7Reaper7/OS-Lab](https://github.com/7Reaper7/OS-Lab)**

