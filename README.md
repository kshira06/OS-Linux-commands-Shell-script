# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/user-attachments/assets/8029ac56-7e4d-43a7-9918-bc0b87f8fe44)





cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/a23101bc-968b-4abb-8fea-55ef8d41458e)



# Comparing Files
cmp file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/33514cdd-ddcd-4ef6-8dda-149c0ed87da1)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/410fdd16-1f43-4a5d-9526-db0fd3326d7e)


 
diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/9e57fd50-b4f9-4af8-ab7f-9e5f0adf0d39)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![image](https://github.com/user-attachments/assets/32da0433-5f19-48b6-aa72-c888dd8d1afd)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/bae9e5d3-8dd8-4630-8b41-099bfa12bab1)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/220838aa-a87c-410c-b83a-47ec63e29675)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/93e85e41-6482-496b-baa3-0da4c1f3ff97)



grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/97401607-9f8b-4960-aa47-857a83652aff)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/53cb71c2-f381-40a8-a384-2d19a7d52be4)


cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/0e443306-1902-4fd8-b7f1-95fc68466c9d)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/ede9acb2-5076-4da2-8715-7cdb51a2fb9c)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/bc50fc2d-79f4-4c52-a238-2a0b685b0690)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/7638ecfc-5363-4798-a21e-a877eb877e8f)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/c52199ff-5060-4890-943b-8820b7b6925c)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/96a2981e-471b-4577-8cc4-cae3e0ece3c6)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/bf8ea764-1454-420d-b840-a1be70002c80)



egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/0e4dabea-0bed-4883-af25-8f914a7ba353)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/3c0ece1e-32d3-4b74-a789-c6bc7ce7d353)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/0ca309ef-91c1-40a9-8d89-fe872470026e)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4599b623-7f25-4352-ab65-b2a47555fecf)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/66702da5-8561-480b-9f51-894e7372527d)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f7e3b399-3295-490a-9705-b8e7c89b754d)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/0c2e0a52-53b2-4212-a513-3ae5fca32c9c)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/3871088c-8e58-4920-8012-d5dca65e6ffd)


egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/839712c0-8866-4e6e-ad70-d4350affd5f9)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/118ff71a-c5be-41bb-b423-2cf1584e748a)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/b60a3812-a734-4847-83d9-ef398460f15f)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/db487fe1-00ad-437d-b472-56abc7964672)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/fec12e86-7b66-4929-802c-72105d23cc1c)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/8880b8f8-cac7-40f9-bc6a-caf76244839e)



sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/5e019337-6d5a-4c9f-b494-8a6d1f4f30d4)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/7ad10650-d502-4355-acf8-1d9e238b054b)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/4b9c1007-4d47-423e-9a1d-90861c6ecc4d)


seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/f7da28c4-c498-4441-acee-7899a0af0160)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/04af3201-e3d3-4c9a-a944-b75d6c1cfdfb)


seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/76038ca0-76b6-48ee-a783-f9876a1fca9e)



seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/8ebbcf19-0926-4ea9-8250-f97fe7db21d8)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/66dc5b06-716a-4d6d-beff-d569472da11e)

seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/2241bf16-7cec-4b42-b7e6-f8d123570255)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/76f017ef-3e0c-4ce4-ae73-79b0acdc9df1)


sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/user-attachments/assets/bbabe181-a9ee-414e-b869-4a5f0e393aa4)


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![image](https://github.com/user-attachments/assets/410d3f4c-6c39-45ae-8d3f-77c27203390e)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/da018c16-5e8c-467f-ae30-7095b5901456)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![image](https://github.com/user-attachments/assets/e617db96-fce1-436d-9fe0-41f35ed083cc)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/bcf83c13-33e3-48fb-90ed-7a55a7b75aa0)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/364aed51-0b83-4bf9-8fbb-55787296e496)


mkdir backupdir


mv backup.tar backupdir
![image](https://github.com/user-attachments/assets/24568343-494d-4e4d-802e-5132811c31ba)
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/036e4799-abdc-450b-88d7-5ddeb8f5f803)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/6ccb03c0-f3b9-4904-ad0b-8dffb2b14370)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/6181de5f-05bb-4725-8f80-608999f94138)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/719b3d0d-18fc-4ed7-9dc5-db698fc8bc0c)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/b1348641-2974-42a9-bf03-f3eb66ad7c4c)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/84742458-2423-4883-8125-fbdff9904663)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![image](https://github.com/user-attachments/assets/ed0d58ba-6d11-49ce-a525-e8ccd29fee64)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/5c9a1a29-9f59-4b3a-abba-c189e817d48c)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/accc7ac1-d2e6-4432-9f19-f564067ea229)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/user-attachments/assets/29ed365e-c001-46cf-86d9-9cb9d2e2b0d4)

abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/b612ffcf-c9bc-4067-8031-9a455df30894)

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT
![image](https://github.com/user-attachments/assets/d9bc106e-0791-4922-9bfd-5805cabfdf40)


chmod 755 strcomp.sh
 ![image](https://github.com/user-attachments/assets/44ac9255-b39a-410d-a7f1-d79020fd656a)

./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/22cecc8a-b0ce-461e-919d-30bd1eee22c8)


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/9e0840f0-393b-44ae-95a7-bff3bbb98824)

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/17dd1995-2421-42ac-b5e9-8d36ac5889b9)



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![image](https://github.com/user-attachments/assets/5d1d4c76-0e62-462f-aeca-f8856ce9bd2a)



# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/704a8138-da04-4e6d-9e7c-d57cebd03f12)

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/e320f6f7-1d8c-40a6-ae26-22e9bb492693)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 ![image](https://github.com/user-attachments/assets/e1e50e41-ca0d-46b4-9511-c19c6c948dfb)

cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 ![image](https://github.com/user-attachments/assets/8e9cfc14-5b7b-4a44-9a52-f602265a3b6b)

 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 ![image](https://github.com/user-attachments/assets/c6276731-bfc0-4923-9395-0174767314ea)

 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 ![image](https://github.com/user-attachments/assets/21495f41-b787-49c4-866b-c750cd004372)

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 ![image](https://github.com/user-attachments/assets/b110ca89-7bb4-40a2-ae7e-9e955cd5bb8a)

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 ![image](https://github.com/user-attachments/assets/441c7ce5-30db-40a2-9868-e06e977c8d21)

$ ./forin2.sh 
 
cat forin3.sh 
![image](https://github.com/user-attachments/assets/d13f1aa3-28f5-45c3-a9c6-0154630d7af7)

```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
![image](https://github.com/user-attachments/assets/da525d56-1aa8-4e9f-bfb8-bb75206511fc)

$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
![image](https://github.com/user-attachments/assets/2d6442e7-f0b8-4703-b39e-362a2cd2ca95)

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![image](https://github.com/user-attachments/assets/1a551ddf-899d-4b54-8cdd-9bca556fc323)


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/39f1b427-8058-4fa8-86bd-4938e6e93a0c)

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/7575775e-8de8-41e3-ac19-4f22ef794827)


cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![image](https://github.com/user-attachments/assets/e73bc102-01c6-447b-94ee-628c97afd6f9)


 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![image](https://github.com/user-attachments/assets/9c772da4-1d47-4e05-9d64-1f21e7366fb6)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 ![image](https://github.com/user-attachments/assets/ba08a53c-75f2-4d42-8200-b95e96202b60)

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/757cf856-8760-4cad-8015-8ac27cea4c56)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/user-attachments/assets/0d6a0e74-5611-4d24-b5d5-5ce22356c84e)



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 
![image](https://github.com/user-attachments/assets/82c45f2a-3a14-494a-b82e-64c5711578b2)

 
 ./funcex.sh 1 2
![image](https://github.com/user-attachments/assets/a2795737-fd0b-48f0-9f73-3e1a8f79451e)

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
![image](https://github.com/user-attachments/assets/8c1fadd2-03e3-4340-8ed4-e6fe845f5776)

$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/5a0ddfc4-b9fa-4d72-8d3e-99452643ed5a)

$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 ![image](https://github.com/user-attachments/assets/dcccd7d9-9525-4da4-86fc-eb10879c3e9f)

cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
![image](https://github.com/user-attachments/assets/dc8f5288-ef79-4ed1-9d80-62c354d4cd33)
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![image](https://github.com/user-attachments/assets/c2f94730-818a-4041-b143-a6606c643a94)


# RESULT:
The Commands are executed successfully.
