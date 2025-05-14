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

![319428818-b7f546fa-4358-4013-a104-97fd773bdf04](https://github.com/user-attachments/assets/aae1ad03-777a-4a42-a23c-b205e0bf2b79)


cat < file2
## OUTPUT
![319428860-4fba90d4-0fb0-49ce-95d0-e3f3251fd076](https://github.com/user-attachments/assets/20b20ae5-48f3-47b4-a40d-67376f3cc87b)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![319428880-dd3c9ace-6547-43db-9376-092b9d7ce36c](https://github.com/user-attachments/assets/1bff3db8-a363-45ee-b3de-9667a9c5befd)

comm file1 file2
 ## OUTPUT

 ![319428910-3bf10b6b-72c4-473a-b260-dfea58416ad1](https://github.com/user-attachments/assets/6e456b1c-8d27-428a-997a-15a25fce7fde)

diff file1 file2
## OUTPUT
![319428948-3cfa2e65-8cab-4fdd-a12a-098c79a58e90](https://github.com/user-attachments/assets/8327ec7d-6c12-42ee-974e-ebd85afb51c4)


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


![319429023-c573c7f6-9f5a-4854-8606-073f45491398](https://github.com/user-attachments/assets/ffd7c5d1-5eb6-49f2-8d7f-a6e293629642)


cut -d "|" -f 1 file22
## OUTPUT

![319429034-c4770f82-6188-41ac-a0aa-386a31d0210f](https://github.com/user-attachments/assets/81070732-9a26-406b-9779-92f1faf5266e)


cut -d "|" -f 2 file22
## OUTPUT

![319429078-9fee0b94-a3a0-4615-99c3-c1c6df894b85](https://github.com/user-attachments/assets/2e83d315-c793-4b90-8b12-7537c56ce94c)

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

![319429098-a12d1c94-407e-4081-9550-681d1f459a8b](https://github.com/user-attachments/assets/2a710280-4570-42a1-8d75-1a5c855eb128)


grep hello newfile 
## OUTPUT


![319429107-b6e084b5-5db6-4a6f-8c2f-71410c86f1bb](https://github.com/user-attachments/assets/ff9f5df6-c561-421d-9d0b-302c876ccb79)


grep -v hello newfile 
## OUTPUT


![319429118-9753ef93-0103-4f2f-b6c6-7eeca5a50894](https://github.com/user-attachments/assets/98b75fa0-d2b2-4c0d-b7c0-c4dda5c8f433)

cat newfile | grep -i "hello"
## OUTPUT

![319429140-713cd60f-e7f6-49f2-b237-f86c7c5d0f4e](https://github.com/user-attachments/assets/41fbe998-c41b-4910-9a0c-d7f576ec2ebe)



cat newfile | grep -i -c "hello"
## OUTPUT


![319429153-32035f00-2cbe-4b3d-ba9f-ba76408fac1b](https://github.com/user-attachments/assets/35bcca85-4b97-49d2-971a-0553a7c8ef68)


grep -R ubuntu /etc
## OUTPUT
![319429180-f1f4063b-872c-4ef5-b564-4f6f71258a70](https://github.com/user-attachments/assets/4ba3bfa4-0eab-49ca-b85e-83f7ec7cb072)


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

![319429480-b1b1806d-7e8c-4be2-bf6d-ae6f68f8c16d](https://github.com/user-attachments/assets/8768455a-ee31-43b4-891e-eb57c1ff9d38)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![319429497-45807eb4-1895-42df-a17d-29b5be91f3d5](https://github.com/user-attachments/assets/edb007ef-99cf-44c3-a24e-7ac04981067c)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![319429524-d8b21ec4-5e48-4417-9b5d-0c2ca8c23467](https://github.com/user-attachments/assets/3436a462-a6f3-4328-a7b1-6d994ac11d91)


egrep '(^hello)' newfile 
## OUTPUT

![319429544-8ce4f7f0-dfcf-4e0c-8073-14aaaa1199c1](https://github.com/user-attachments/assets/4a17191b-1991-483c-8938-b4158e18e6ac)


egrep '(world$)' newfile 
## OUTPUT

![319429558-33f03fe5-06b8-4015-aa52-8c20c4f9234d](https://github.com/user-attachments/assets/ad77ff51-fa16-4ed2-b6a3-4ba6cf79685b)


egrep '(World$)' newfile 
## OUTPUT

![319429568-1bb819a5-ab9f-4d04-bc47-06c9e5e27653](https://github.com/user-attachments/assets/001df498-08cf-48c7-8d8c-4e52b8fb1583)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![319429597-5f118111-b698-4aff-86c6-7f51a18ab6de](https://github.com/user-attachments/assets/0444163c-83cc-4681-8e5b-1237a8b3ac01)


egrep '[1-9]' newfile 
## OUTPUT

![319429612-1ae7fa24-8a53-4911-821d-e1665720e38e](https://github.com/user-attachments/assets/56a071d6-c864-4750-9d30-0076f53b7343)


egrep 'Linux.*world' newfile 
## OUTPUT

![319429631-f5207be6-4e7b-4ad0-a08b-6cccdee0b727](https://github.com/user-attachments/assets/34abb7cd-3501-406b-a31e-56ab5082802d)

egrep 'Linux.*World' newfile 
## OUTPUT
![319429660-1aa5ee2c-b200-4135-9d70-fe0c077570b4](https://github.com/user-attachments/assets/c33bf44a-7c80-4368-809f-96a09cee4b9c)


egrep l{2} newfile
## OUTPUT
![319429689-4d9b341a-e6a1-4293-8626-db2670e57542](https://github.com/user-attachments/assets/6d6f8dfb-d007-452d-a98e-7812726972f5)



egrep 's{1,2}' newfile
## OUTPUT 

![319429713-4b872336-a8db-4739-a832-c704bdc290ba](https://github.com/user-attachments/assets/d46f029b-8787-4821-a8df-fef6c9cc9cd5)

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
![319429740-44a01fbe-422e-485a-a22f-3c2a500d6932](https://github.com/user-attachments/assets/9958645c-e850-4952-b396-53fee930e42d)



sed -n -e '$p' file23
## OUTPUT

![319429846-709af281-77ce-4c2d-8838-3e70457475a4](https://github.com/user-attachments/assets/fb1399c8-20c2-4a58-8e53-82af04017b2f)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![319429914-0e2004aa-11a2-425a-8ab3-f5cd99442e5a](https://github.com/user-attachments/assets/fee5ae1f-76b7-480c-a007-5a1c864c28aa)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![319430010-6b17f715-e898-445c-9dcf-8e931c010e3b](https://github.com/user-attachments/assets/b6014e51-71e3-4053-b9fb-d3ef213cda8d)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![319430032-7d74c34e-c552-4843-a075-63f9067aca24](https://github.com/user-attachments/assets/d412ce46-9754-4a7c-9149-bbbc224921b1)


sed -n -e '1,5p' file23
## OUTPUT
![319430061-1ab92a40-ea52-4d36-a46f-420f361d58ac](https://github.com/user-attachments/assets/c3cc4379-af00-45f6-90c6-a6a0aeb7909d)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![319430073-2be25544-97f8-4630-b406-9f4776ee958b](https://github.com/user-attachments/assets/9e0bd5d9-49eb-41c6-9714-1febb7b6ad53)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![319430132-2268f0e7-579a-4a55-8fe1-67bb74cd3ed1](https://github.com/user-attachments/assets/2d3eee97-98a7-476d-8316-cd7e8a235761)



seq 10 
## OUTPUT
![319430254-44a7ea47-2616-4d0a-bae9-17da9e779169](https://github.com/user-attachments/assets/19fa0831-7f7b-4b9c-87b9-0978d0d500e6)



seq 10 | sed -n '4,6p'
## OUTPUT

![319430262-04dc11f3-6be0-4c27-a1bc-5be21f7278e1](https://github.com/user-attachments/assets/a5be3d75-e71b-474a-b07a-b87879463b25)


seq 10 | sed -n '2,~4p'
## OUTPUT



seq 3 | sed '2a hello'
## OUTPUT
![319430303-d234abfa-cda4-4fb2-8165-0dbfbbb9b26f](https://github.com/user-attachments/assets/abef0cbb-6908-41ea-abc5-3ef5b371c668)



seq 2 | sed '2i hello'
## OUTPUT
![319430323-f5ec0595-dc0c-4d27-a7d2-7f5815ec056c](https://github.com/user-attachments/assets/c6a5a4b2-db1a-40cf-8d53-4ec6c43d31d4)


seq 10 | sed '2,9c hello'
## OUTPUT
![319430340-586c40eb-e2a0-4ec0-86de-736a7cb32bf1](https://github.com/user-attachments/assets/cb5532fa-e4e3-4e4a-a754-cf7113403df4)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![319430353-2bf29007-b112-461a-bfa0-fd4332cfa0be](https://github.com/user-attachments/assets/2007e804-9369-4ac2-977f-6048de47da71)


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
![319430425-8d0bf1fe-9dce-4202-bf35-ac135b7778a2](https://github.com/user-attachments/assets/de5230d9-a36f-41b9-bfc0-622c37b15749)


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

![319430447-67cd139d-f8ea-433a-b959-13b9e8cbcc8a](https://github.com/user-attachments/assets/996e5503-ebb9-4611-9d6f-87727d88cbde)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![319430477-2c88ffa0-ff83-400a-83fd-51a1822881f4](https://github.com/user-attachments/assets/95d54a1d-c396-40e2-832e-57f802798ca8)

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

![319430503-ccf8d42b-87c2-4a5a-8faf-c24a53024da5](https://github.com/user-attachments/assets/01f881e4-407c-4577-8a65-83cad986d257)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![319430558-073c27b4-adb7-4e3a-b901-d3828a715dbe](https://github.com/user-attachments/assets/e1a57867-21af-4ef0-85cc-9e2986dfe2d0)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![319430645-e12aad28-de23-40ee-9f2b-85d989c8e24c](https://github.com/user-attachments/assets/d80a6adb-210b-4fca-b2f1-d80d4a7cc772)

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

![319430766-d2ad8a74-7544-4c51-b368-f846976d49ef](https://github.com/user-attachments/assets/0b7a18dc-0c97-4275-8b2e-646c5ec910aa)

tar -xvf backup.tar
## OUTPUT
![319430795-0449668b-ab2f-4bdd-aee6-19fd5ae8ff0e](https://github.com/user-attachments/assets/cb00426a-f007-4f57-a338-a8032b5b8c28)

gzip backup.tar

ls .gz
## OUTPUT
 ![319430873-5a66b934-9a7b-4ea5-885d-9bd736a46d1f](https://github.com/user-attachments/assets/9f133ddc-4d5e-40fb-8440-72f5caae7c06)

gunzip backup.tar.gz
## OUTPUT

 ![319431041-18762b5d-f682-4bbb-8db6-f5010444fc09](https://github.com/user-attachments/assets/cc3d50ba-4cda-4ba1-afa4-148dd3002139)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![319431069-daa97438-0c15-4018-ad8e-f3e00efb84f7](https://github.com/user-attachments/assets/b68a84e6-fe0d-4f26-b3fd-ef5f6d1944ad)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![319431153-588ed472-4e89-471d-a11e-de8d15296821](https://github.com/user-attachments/assets/371f80a7-e844-41c4-a3f9-6c573146a4ab)


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

 ![319431226-0c14a3e5-23c1-4da7-9813-6e123505567e](https://github.com/user-attachments/assets/5541f9aa-300d-4d01-a960-aee9768faff1)

ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![319431402-f7dd3dc5-e458-40c5-b65c-f155aa31dc17](https://github.com/user-attachments/assets/27737d3e-988e-4525-8abb-92d8cd346651)

abcd
 
echo $?
 ## OUTPUT

![319431412-c842ce43-7d54-4ba3-b7ec-50da158c51ee](https://github.com/user-attachments/assets/1fc81144-f6a1-4fba-bd58-3a163abef9ac)

 
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

![319431442-8dba7800-b309-4d0c-99fc-dbc7d1651e60](https://github.com/user-attachments/assets/0309000b-023c-4932-9507-ad2271e44f9d)

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
![319431716-0c65c410-0709-44dc-bb09-5121ba7c0020](https://github.com/user-attachments/assets/e665cb5b-1e8d-4c3b-b4da-1e76a2a0f7ce)
![319431777-314d1e38-aa8a-4463-898d-533444575494](https://github.com/user-attachments/assets/788f2237-13d6-4eaa-9ab1-9e5d9753a0d2)


# RESULT:
The Commands are executed successfully.
