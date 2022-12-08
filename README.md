# Exam_2420
Part 1 \
sudo apt upgrade is used to update most of the software on your Ubuntu OS \

NOTE: You can check what to update by using sudo apt update

Part 2 
1. Create a directory in VM using mkdir final \
2. Create a file in the directory using touch part2 \
3. Open vim editor to edit vim part2
4. Paste the code in it \
5. Pressing "I" and edit the text file just like normal word documents
![](Part2.png)

Part 3 \
journalctl \
1. To print logs for the current boot use command journalctl
2. ![](Part3%20boot.png)
3. To print a log that should have a priority of warning or more important use journalctl -p "warning"
4. ![](Part3%20priority.png)
5. ![](Part3%20pretty%20json.png)

Part 4 \
1. Add a user by using the command: useradd -ms /bin/bash USER_NAME 
2. Add the user to the sudo group by using the command: usermod -aG sudo USER_NAME 
3. Modify ownership by using the command:rsync --archive --chown=USER_NAME:USER_NAME ~/.ssh /home/USER_NAME 
4. Create a bash script using touch part4.sh 
5. Write a bash script 
```
#!/bin/bash

if grep -i -q. "$1" ;then
  if 1000 <= "$id -u" <= 5000
  echo "Regular users on the system are" 
  fi
 else
  echo "No Users"
fi

echo "Users currently logged in are:" "$whoami"
```
6. Give the script permission to excute by using chmod +x part4.sh 
7. Excute the scipt by using ./part4.sh 

Part 5
1. Create a bash script using touch part5.sh 
2. Write a bash script 
```
#!/bin/bash

echo "hi Bob" > /home/vagranthi-bob
```
3. Start the service by using sudo systemctl enable application.service
4. To check status sudo systemctl status backup.service
