# Git Bash

During my studies, I explored and applied different Bash commands for working with files, directories, and processes. Here are some of them:

#### Files and directories commands
```bash
~                                     # Home directory 
pwd                                   # Determine the name of the current directory
mkdir test1                           # Create a directory named test1 inside the current directory
cd test1                              # Navigate to the test1 directory 
touch 1 2 3                           # Create files 1, 2, and 3 inside the test1 directory
ls                                    # Check the contents of the test1 directory
cd ..                                 # Navigate to the home directory
mkdir test2                           # Create a folder named test2 inside the home directory
rmdir test2                           # Delete the test2 directory
cd test1                              # Delete file 2 from the test1 directory
    rm 2                              
cd ..                                 # Create a folder named test3 in the home directory and add two files into it
    mkdir test3
   cd test3
    touch 1 2
cd ..                                 # Delete the test3 directory
    rm -rf test3
mkdir test4                           # Create a folder named test4 in the home directory
mv test1/1 test4                      # Move files 1 and 3 from the test1 directory to the test4 directory
mv test1/3 test4
cd test4                              # Add three lines with the word line into file 1
    echo line > 1
    echo line >> 1
    echo line >> 1
 cat 1                                # View the contents of file 1
 echo line > 3                        # Add three lines with the word line into file 3
   echo line >> 3
   echo line >> 3
cat 1 3                               # View the contents of both files (1 and 3) at the same time
nano 1                                # Using one of the text editors, replace all lines in file 1
    ^\ Replace
      Search (to replace): line
      Replace with: kitten
      Replace this instance? All
   ^X Exit
      Save modified buffer? Y Yes
      File Name to Write: 1
```
#### Search, proccesses and curl commands
```bash
~                                          # Home directory
pwd                                        # Determine the name of the current directory
mkdir test3                                # Create a folder named test3
cd test3                                   # Add three files (4, 5, and 6) to the test3 folder, each containing four lines: row1, row2, row3, row4.
  touch 4 5 6
   echo row1 > 4
   echo row2 >> 4
   echo row3 >> 4
   echo row4 >> 4

   echo row1 > 5
   echo row2 >> 5
   echo row3 >> 5
   echo row4 >> 5

   echo row1 > 6
   echo row2 >> 6
   echo row3 >> 6
   echo row4 >> 6
 grep row2 5                               # Find the line row2 in file 5
 grep -r "row" .                           # Find the line row in the test3 folder
   or grep -rw "row" . (if "row" is a standalone word)
grep -c "row" 6                            # Count how many lines contain row in file 6
find -name 5                               # Find file 5 inside the test3 folder
find -name 5 -delete                       # Delete file 5 using the find command 
echo test > 4                              # Using the echo command, add the word test into file 4 without keeping its previous content
echo fail > 4                              # Replace the word test with fail in file 4
echo test >> 4                             # Append the word test to file 4 while keeping its existing contentecho test >> 4
 echo test >> 4
ps aux or tasklist (for windows)           # Display all processes for all users, not just the processes in the console
kill 14480                                 # Kill any process in the console  
ping rusau.net                             # Check the availability of the resource rusau.net using ping 
ping -n 5 rusau.net (-n for windows)       # Send 5 ping packets to rusau.net
curl https://petstore.swagger.io/v2/       # Using GET and curl, retrieve information about registered pets with any status from https://petstore.swagger.io/
 pet/findByStatus?status=available,pending,sold
curl -X POST "https://petstore.swagger.io   # Using POST and curl, create a new user on https://petstore.swagger.io/ 
  /v2/user" \
   -H "Content-Type: application/json" \  
   -d '{
     "id": 876505,
     "username": "Annnnna123",
     "firstName": "Anna",
     "lastName": "Zuuuuu",
     "email": "ryry888e@gmail.com",
     "password": "qwerty123",
     "phone": "876876860",
     "userStatus": 1
    }'
  {"code":200,"type":"unknown","message":"876505"}

```
