
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
![Screenshot from 2025-03-04 14-06-15](https://github.com/user-attachments/assets/3a8efa18-928f-4f53-aba5-37b47f1bdcb3)




cat < file2
## OUTPUT
![Screenshot from 2025-03-04 14-02-52](https://github.com/user-attachments/assets/300bfbc3-c307-44d4-8afb-f39b5b543531)



# Comparing Files
cmp file1 file2
## OUTPUT
 
comm file1 file2
 ## OUTPUT
 ![Screenshot from 2025-03-04 14-09-08](https://github.com/user-attachments/assets/4a30d647-35f4-4902-a7ff-481b343fa080)



 
diff file1 file2
## OUTPUT
![Screenshot from 2025-03-04 14-10-50](https://github.com/user-attachments/assets/e5c4ea86-da78-467b-9f8f-0c76ae190bd8)



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
![Screenshot from 2025-03-04 14-13-09](https://github.com/user-attachments/assets/58de7d99-34fc-4a95-8cf9-9c72e3eaa2ac)





cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-03-04 14-14-02](https://github.com/user-attachments/assets/12f50400-e3ec-46d7-8885-e6c856896839)




cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-03-04 14-14-39](https://github.com/user-attachments/assets/8286775b-ee9b-4b96-9eaa-c32fd3a1075b)


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
![Screenshot from 2025-03-04 14-21-33](https://github.com/user-attachments/assets/43326a3d-2ac7-462c-aa70-14b10e72b988)




grep hello newfile 
## OUTPUT
![Screenshot from 2025-03-04 14-22-28](https://github.com/user-attachments/assets/d8494ec5-b4f9-4b6f-99f2-5c3e55e880ec)





grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-04 14-23-00](https://github.com/user-attachments/assets/6d3c754a-0a59-4006-9a55-81103350d6dc)




cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2025-03-04 14-23-41](https://github.com/user-attachments/assets/099acb82-3578-429c-a2e8-305efe33656a)





cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-03-04 14-24-26](https://github.com/user-attachments/assets/7ff50629-6a15-4a5e-a9f5-dbae1ec6b96e)






grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2025-03-04 14-25-59](https://github.com/user-attachments/assets/b3ff8446-6add-4ae1-ad9a-94415a9700be)




grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/872ac707-1893-47a6-a203-bb7c403ba6af)



cat > newfile 
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
![image](https://github.com/user-attachments/assets/9986492e-a1fa-475d-9893-36abcd56ec52)




egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a5ed2149-b859-4dbf-8852-2c55dfdd7b6c)




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/049bf802-7797-4ae0-8aa5-4d261f46bb0a)





egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/df283d9b-ae84-4f8c-b27e-29a40c08f247)




egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4366b97f-8d12-42c1-a0b8-6018f365438a)




egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/215be314-57cf-4011-9f7b-46a60b1ad287)



egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/5582433c-066b-41b5-91e8-f2fe3b25fb02)




egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/fddad321-ba48-416c-a85f-469f2f35a415)




egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/57b70f93-e9a7-428a-a053-7e53758d8f62)



egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/2e22e2fb-a294-470b-9e25-6ab514bbafa6)



egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/1f6d8cde-6b16-4b2a-b079-d6fc50a8efab)




egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/ebeba707-2572-4e49-9c49-94a527cf01ae)



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
![image](https://github.com/user-attachments/assets/a445e376-115a-4abd-8360-d34c2c7dfcf6)




sed -n -e '5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/96f6312d-81c2-469b-beb7-e96300c9266e)




sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/44c993aa-f0b4-4a3d-b640-30a2d6a52feb)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/ae4ab4b0-013c-489b-bce1-c4cc70a9e509)




sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/c71d1322-f5db-4222-86a1-f4b202bbf39c)




sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/1eb21f85-7870-43f2-b9ea-5817acb25a13)




sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/94e844a0-5485-4f03-b9bb-b773f6ffa3e1)





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/33d2d573-4901-46e8-a133-ff1f34266571)



seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/e61d13a7-5801-4e2c-96e1-bb0481d19ef6)




seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/f0544394-7d34-42da-87b1-a917065f395e)




seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/611a82ce-2c74-44f4-a635-b5651c27158c)




seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/6119e59d-31df-4372-842c-a139ac8519d5)




seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/43a94eb4-b5c8-4033-a32b-d331e0fa16c0)



seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/4608b0fb-c455-4259-85b0-4103f306cba6)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/99c73ba9-8e09-47da-8705-e2f17516e8b7)





sed -n '2,4{s/$/*/;p}' file23


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
![image](https://github.com/user-attachments/assets/243def38-9848-4575-816f-78aa9a038696)



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
![image](https://github.com/user-attachments/assets/3874bb79-ddfe-414d-904f-458320d9818c)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/c82a8521-5cbe-47f6-868c-8503a6d73aa6)


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
 ![image](https://github.com/user-attachments/assets/93901c25-c687-4313-bf3d-094eeb6752a3)



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/9fce0538-5fd1-4f87-b824-fc17d0eab5c1)




#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/bd9e91b8-f04c-4ae3-bf88-536407d238fa)



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/a0edd1f6-ae8d-4e93-9bb9-4fd79a2cc91f)



tar -xvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/7f794075-11e6-4045-81dd-ded38a0b3462)


gzip backup.tar

ls .gz
## OUTPUT

![image](https://github.com/user-attachments/assets/62e6ffcd-3a8d-442e-8d74-d878a8f75d88)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/098575e8-46e0-4852-b691-52594a4be7b4)



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

![image](https://github.com/user-attachments/assets/a6671a13-a9ac-4161-b943-00ef6c3c4756)


 
ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/416ebb36-2e25-4b28-ab74-dc0ea7c53f82)


echo $?
## OUTPUT 

![image](https://github.com/user-attachments/assets/6799b43e-d951-46bf-a4d6-d93276484399)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

![image](https://github.com/user-attachments/assets/9aaef22f-3414-45ad-8995-53cb8526737b)

 
abcd
 
echo $?
 ## OUTPUT


 ![image](https://github.com/user-attachments/assets/6ab2fb90-ae92-40d0-a9a4-0a4f74ac8f84)



 
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

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/4fadc5e6-c229-42de-8c7c-8a8e35a46c0f)



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

![image](https://github.com/user-attachments/assets/9d4757ed-2c5c-4c60-a6bd-41c09b54371c)


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

![image](https://github.com/user-attachments/assets/e6bb5869-a57d-4eb6-9a40-c18edd38b4c3)


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

## OUTPUT

![image](https://github.com/user-attachments/assets/2387f741-1662-4739-aee9-5a2d730329bc)


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

## OUTPUT
![image](https://github.com/user-attachments/assets/6c334646-1239-4db0-88e4-0d02f17de012)


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

![image](https://github.com/user-attachments/assets/1020d3bb-68ce-47f1-8a9c-8abec3a4cd6f)

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

![image](https://github.com/user-attachments/assets/d1c79bea-82f8-44a0-a578-4ff311e0ca28)


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
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
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

![image](https://github.com/user-attachments/assets/9edb20a4-3c2b-4dee-9cd1-68f525f77394)

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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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

 
 ./funcex.sh 1 2

 
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

![image](https://github.com/user-attachments/assets/0e2e6ba4-6116-42cb-8096-8e4f067979e4)

 
 
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

![image](https://github.com/user-attachments/assets/2f46bed6-9fbd-462d-8919-a6f5ccaa53bd)

 
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

![image](https://github.com/user-attachments/assets/3f07da4e-a733-4b18-9b15-0510320ee247)



# RESULT:
The Commands are executed successfully.
