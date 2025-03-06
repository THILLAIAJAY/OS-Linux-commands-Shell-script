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
cat > thiru
```
chanchal singhvi
c.k.bindh
kavi
sumit
^d
```
cat > thiru1
```
chanchal singhvi
c.k.bindh
ajay
jai
^d
```
### Display the content of the files
cat < thiru
## OUTPUT

![Screenshot from 2025-03-06 13-31-37](https://github.com/user-attachments/assets/283b7183-d5a3-4dc3-8aaa-9f336da80af4)

cat < thiru1
## OUTPUT

![Screenshot from 2025-03-06 13-32-38](https://github.com/user-attachments/assets/803e651a-54e2-40a2-b015-0166fc5c4562)


# Comparing Files
cmp thiru thiru1
## OUTPUT

![Screenshot from 2025-03-06 13-33-49](https://github.com/user-attachments/assets/8a7b6933-02f7-4600-ac1c-59b01df32c88)
 
comm thiru thiru1
 ## OUTPUT
 
![Screenshot from 2025-03-06 13-34-33](https://github.com/user-attachments/assets/d7b8f479-9238-42c8-88b3-4d3e5458837e)

 
diff thiru thiru1
## OUTPUT

![Screenshot from 2025-03-06 13-38-02](https://github.com/user-attachments/assets/6c50b153-cb0d-47c8-95f6-cc8e59f1483b)

#Filters

### Create the following files file11, file22 as follows:

cat > thiru11
```
Hello world
This is my world
^d
```
cat > thiru22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 thiru11
## OUTPUT

![Screenshot from 2025-03-06 13-49-52](https://github.com/user-attachments/assets/9ac4b128-cad6-4d3a-a23a-84ef8825ceca)



cut -d "|" -f 1 thiru22
## OUTPUT

![Screenshot from 2025-03-06 13-51-07](https://github.com/user-attachments/assets/2cc662b6-8d6c-49e4-87f3-2af63561c415)


cut -d "|" -f 2 thiru22
## OUTPUT

![Screenshot from 2025-03-06 13-51-59](https://github.com/user-attachments/assets/ae21c7fe-689e-44b7-aba7-599c1f7653e5)

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

![Screenshot from 2025-03-06 14-00-07](https://github.com/user-attachments/assets/0b73c152-29bb-474a-a064-18fb4e5627f4)


grep hello newfile 
## OUTPUT

![Screenshot from 2025-03-06 14-00-52](https://github.com/user-attachments/assets/8b1127b7-4a64-4415-985f-bc68653514c2)



grep -v hello newfile 
## OUTPUT

![Screenshot from 2025-03-06 14-02-30](https://github.com/user-attachments/assets/c88dcfef-02e4-4620-a6c4-dc82ce6f2d54)


cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-03-06 14-04-38](https://github.com/user-attachments/assets/4ce72d51-4933-40f4-bd88-17b143e5677a)



cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2025-03-06 14-05-41](https://github.com/user-attachments/assets/35ad3f58-4375-4cf1-be26-6265eb87307f)



grep -R ubuntu /etc
## OUTPUT

![Screenshot from 2025-03-06 14-16-12](https://github.com/user-attachments/assets/351aef4e-0f05-41b0-b1cd-46dbe2086c89)


grep -w -n world newfile   
## OUTPUT

![Screenshot from 2025-03-06 14-18-49](https://github.com/user-attachments/assets/aeb8253e-176d-4b79-b834-008449412eeb)


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

![Screenshot from 2025-03-06 14-26-05](https://github.com/user-attachments/assets/ac56ba52-4538-41f0-8982-1a2bc6c4b9d5)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2025-03-06 14-28-10](https://github.com/user-attachments/assets/99bd0f53-de6e-4d14-a210-5089b79cbdfb)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2025-03-06 14-29-15](https://github.com/user-attachments/assets/73a27150-ac27-4825-9ec2-ba2fd06c822e)



egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2025-03-06 14-30-54](https://github.com/user-attachments/assets/c6d05779-5c19-447d-b4c5-f27605917c28)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2025-03-06 14-32-48](https://github.com/user-attachments/assets/1a3fc253-44d8-4d5a-a2d8-dd9d05b112ee)


egrep '(World$)' newfile 
## OUTPUT

![Screenshot from 2025-03-06 14-34-06](https://github.com/user-attachments/assets/0b92fcff-9a0f-4a05-b882-1d5c03bd5a92)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2025-03-06 14-38-30](https://github.com/user-attachments/assets/e89e8227-504b-4faf-aa9a-22252d86fb81)


egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2025-03-06 14-39-13](https://github.com/user-attachments/assets/7d49c79d-0d6c-4d75-8ce5-6c70329b5e72)


egrep 'Linux.*world' newfile 
## OUTPUT

![Screenshot from 2025-03-06 14-40-19](https://github.com/user-attachments/assets/9424e3f0-5bf6-4bbf-bce3-b004ab7820c0)

egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot from 2025-03-06 14-42-50](https://github.com/user-attachments/assets/1063eb4d-2b32-43ef-b89f-01c8d8a5660e)

egrep l{2} newfile
## OUTPUT

![Screenshot from 2025-03-06 14-45-04](https://github.com/user-attachments/assets/e5e63ccd-d6c0-43c4-952d-acf7b6bde2b7)


egrep 's{1,2}' newfile
## OUTPUT 

![Screenshot from 2025-03-06 14-46-06](https://github.com/user-attachments/assets/0224dfc0-4246-47ae-8489-d8740ce1aa0a)

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

![Screenshot from 2025-03-06 14-51-43](https://github.com/user-attachments/assets/eaad177c-16ba-493b-8470-89e3ebc9bd39)


sed -n -e '$p' file23
## OUTPUT

![Screenshot from 2025-03-06 14-53-10](https://github.com/user-attachments/assets/47438610-1cd7-4718-a48a-51e64ce43b24)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-03-06 22-03-51](https://github.com/user-attachments/assets/ce3672a1-9a7c-4f94-86b6-3b60877098d2)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-03-06 22-15-53](https://github.com/user-attachments/assets/bd1225fd-3f05-40c5-8e30-a6955fc5aa55)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-03-06 22-18-51](https://github.com/user-attachments/assets/51e85db6-ef58-493f-9df5-7153db40616b)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-03-06 22-20-08](https://github.com/user-attachments/assets/b2e8ec91-4732-4cd7-a1c4-0b43a9519398)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-03-06 22-22-51](https://github.com/user-attachments/assets/82622cad-113a-4bfd-9999-0026e3dd178d)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-03-06 22-26-16](https://github.com/user-attachments/assets/97ee75b3-0a1c-41b2-8227-da79a1ce74f4)


seq 10 
## OUTPUT

![Screenshot from 2025-03-06 22-28-24](https://github.com/user-attachments/assets/534a93d0-b706-4b1e-aff7-7604cb2961a8)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-03-06 22-29-36](https://github.com/user-attachments/assets/c7ec22e3-d74c-4271-ae52-3050fee55ad1)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2025-03-06 22-30-41](https://github.com/user-attachments/assets/a3de6eed-6154-42e5-988e-fcc790d425c7)


seq 3 | sed '2a hello'
## OUTPUT

![Screenshot from 2025-03-06 22-32-24](https://github.com/user-attachments/assets/62f3fc97-602a-470d-a0b1-0479499109c2)


seq 2 | sed '2i hello'
## OUTPUT

![Screenshot from 2025-03-06 22-33-19](https://github.com/user-attachments/assets/245b70ee-6efc-4cb9-bcd8-7cb670471d81)

seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot from 2025-03-06 22-34-13](https://github.com/user-attachments/assets/49919092-734e-49ec-9496-8a9c4030aa0e)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2025-03-06 22-35-56](https://github.com/user-attachments/assets/faa1776f-2b95-46fe-bc9b-5204835edc80)


sed -n '2,4{s/$/*/;p}' file23

![Screenshot from 2025-03-06 22-37-08](https://github.com/user-attachments/assets/ea32d9e7-7bc0-4e3b-973f-0954845d9854)

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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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
 ./argshift.sh 1 2 3
 
 
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


# RESULT:
The Commands are executed successfully.
