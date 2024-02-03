# **Operating System Lab 3**

------

**Note:** Remember to use the **sudo** **(super user do)** command if you are **denied permission**.

## <span style="font-size: 1.1em;">Create a New User:</span>

1. Add a new user **"mrtom"** and change its **password** using the following commands.

  ```
  sudo useradd user
  sudo passwd user
  ```

2. It is to be noted that the **useradd** command will not create the **default files** for the new user initially.

3. To achieve that, you must write the following commands:

  ```
  sudo mkdir home/user
  sudo cp -rT /etc/skel /home/user
  sudo chown -R user:user /home/user
  ```

4. The first command makes a **new home directory** for the created user.

5. The second line **copies the system files** to the that directory.
     - **`-r`**: **Recursively** copy directories and their contents.
     - **`-T`**: Treat the destination as a normal file and not a directory.

6. The third line **changes the ownership** of the the directory to the new user we created.![1](./images/1.png)

     

7. **Restart the machine** for the changes to take effect.![2](./images/2.png)

     

8. Now we have two users. **Login as the new user** with the password you had set before.![3](./images/3.png)

  

## <span style="font-size: 1.1em;">TASK 1 - Perform Basic Commands:</span>

1. Open the terminal.![4](./images/4.png) **Note:** By default when you create a new user using the above method it will not assign a shell to the terminal. to achieve that you can run the following command:

  ```
  chsh -s /bin/bash user
  ```

2. **Create** a new file named "**19f-XXXX.txt**" and **start editing** through the built in text editor using the **nano** command.

  ```
  nano file/path/name
  ```
![5](./images/5.png)

3. Add at least **10 lines of text**, for later testing also write your **roll number** in any one of them.

4. Press **`ctrl + s`** to **save** and **`ctrl + x`** to **exit**.![6](./images/6.png)

   

5. Create and edit another file named "**mrtom.txt**"  using the same procedure.

6. Also **add 10 lines**.![7](./images/7.png)![8](./images/8.png)

   

7. **Merge and print** the data from both files using the **cat** command.

  ```
  cat file1 file2
  ```

![9](./images/9.png)

8. Create another file.

9. **Redirect the data** on the screen into that file using the **`(>)`**  operator.![10](./images/10.png)

   

10. Print the **first two lines** of the first file using the **head** command.

    - **`-n`**: Represents the **number of lines to be shown** starting from the **head**.

  ```
  head -n file/path/name
  ```

![11](./images/11.png)

11. Print the **last two lines** of the second file using the **tail** command.
    - **`-n`**: Represents the **number of lines to be shown** starting from the **tail**.

   ```
   tail -n file/path/name
   ```

![12](./images/12.png)

12. Use the **grep** command to **find a line having a specified string** from a particular file, which in this case is your **roll number** and **the seventh line**.

   ```
   grep "string" file/path/name
   ```

![13](./images/13.png)

13. **Change the permission** of "**mrtom.txt**" to grant the groups the executable permission to the file using **chmod** command.

   ```
   chmod g+x file/path/name
   ```

14. Here:
       - **`g`**: means **group**.

       - **`+`**: **adds** the following permission(s).

       - **`x`**: means **executable**.


![14](./images/14.png)

15. **Change the permission** to **remove** the write permission from the **users**

   ```
   chmod u-w file/path/name
   ```

16. Here:
       - **`u`**: means **user**.
       - **`-`**: **removes** the following permission(s).
       - **`w`**: means **writeable**.

![15](./images/15.png)

17. Show the **current location** (in directories) using the **pwd** command.![16](./images/16.png)

18. Navigate to the **Desktop** using the **cd** command.

19. Use **ls** command to **show a list** of all directories and files in the Desktop directory.![17](./images/17.png)

    

20. You can make a **new directory** using **mkdir** to store your pictures and files.

   ```
   mkdir filename
   ```

![18](./images/18.png)

21. You can view the current **time and date** using the **date** command.![19](./images/19.png)

    

22. Display a "**Thank You**" message using the **echo** command.![20](./images/20.png)

   

## <span style="font-size: 1.1em;">TASK 2 - Perform Basic Commands 2:</span>

1. Create a new file named "**19f-XXXX_OS-lab_rules.txt**" using **touch** command.

  ```
  touch filename
  ```

![21](./images/21.png)

2. Open the **notepad editor** using **gedit** command and paste the Lab 1 rules.

  ```
  gedit filename
  ```

![22](./images/22.png)

3. Change the permissions as required using the **binary representation**, **`( rwx r-x r--)`** for the current case.
4. The steps are as following:
     - In the three character combination of permissions per user, put **1** in place of each **`(r,w,x)`**and put **0** in place of each dash **`(-)`**

     - For the above case the combinations will be: **`( 111 101 100 )`**.

     - Now convert the **binary numbers** to their **decimal** counterparts.

     - **111 = 7, 101 = 5 and 100 = 4.**

     - Using the following command:

```
chmod nnn filename
```

![23](./images/23.png)

5. You can **append** the results of **ls** command to the text file using the **double insertion operator** **`(>>)`**.

  ```
  ls -l filename >> filename
  ```

![24](./images/24.png)
