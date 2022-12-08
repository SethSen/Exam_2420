# Exam_2420

## Part 1

sudo apt update && sudo apt upgrade

## Part 2

### Keybinds used

r - replace 1 with 0 in line 1
a - add h in echo in line 2
o - add a new line
:wq - save and quit the file

### Images

![Part 2!](images/1)

## Part 3

Running `man journalctl`

![Part 3!](images/2)

1. Ran `/current boot` in man page

![Part 3!](images/3)

2. Ran `/priority` in man page

![Part 3!](images/4)

3. Ran `/output` in man page

![Part 3!](images/5)

5. Ran `/json` in man page

![Part 3!](images/6)

### output

![Part 3!](images/7)


## Part 4

adding two new users

![Part 4!](images/8)

Writing script

![Part 4!](images/9)

![Part 4!](images/10)

Changing file to executable

![Part 4!](images/11)

Running the file

![Part 4!](images/12)

updated script with motd

```
#!/bin/bash

# Find regular users and logged in users

echo "Regular users on the system are:" >> /etc/motd
awk -F: '$3 >= 1000 && $3 <= 5000 {print $1 " " $3 " " $7}' /etc/passwd >> /etc/motd

echo "Users currently logged in are:" >> /etc/motd
w -h | awk '{print $1}' >> /etc/motd

# Or, using who:
# who | awk '{print $1}' >> /etc/motd

```

moving files

![Part 4!](images/13)
