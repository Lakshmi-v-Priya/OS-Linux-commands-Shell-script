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
![312823451-0119401d-8e53-42c4-ab54-ce749dc6a03e](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/f2303091-4e9f-4c44-a28b-23ca83a69122)
cat < file2
## OUTPUT
![312823636-9d6b43a7-9146-4ad3-bd12-6124400fb4d7](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/08944f66-70a4-4db5-a933-feebaa01af78)
# Comparing Files
cmp file1 file2
## OUTPUT
 ![312824286-ec7146a1-7dcf-4519-b2bd-bb074874a9f6](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/1b4f8f77-5a16-417f-9666-f1570e157355)
comm file1 file2
 ## OUTPUT
![312824209-2b388c18-8716-471f-86a5-104b81593a8b](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/220be64a-effd-4244-bbaf-03b258b6f6e9) 
diff file1 file2
## OUTPUT
![312824501-bdc3e442-d591-40aa-b92a-121299adbb65](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/edef6c07-3a90-4bd5-9162-f01cf01307bf)
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
![312824664-141e89e4-c3d8-4296-b12d-a2e6bb80f2df](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/b77622d3-a823-482e-9c8d-ca4339837656)
cut -d "|" -f 1 file22
## OUTPUT
![312824777-b1f5d32d-f1a3-4a66-9c0e-10d02548f316](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/407d1f3f-7d6a-4345-9ea0-dcbfec7ac6ca)
cut -d "|" -f 2 file22
## OUTPUT
![312824982-336fe232-b5b0-424a-88fe-5ca75d10039f](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/10531e7e-a9ed-4915-822b-9a1363f28b50)
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
![312823117-fc26c416-54b1-4b9c-b839-1e6a77c2ff12](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/04f534a4-ea83-4a23-b77e-b371a5482c9b)
grep hello newfile 
## OUTPUT
![312825332-3cfe2166-0ee0-46f4-9b7c-44512aeae4cd](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/2420fa72-141a-4081-948a-e4cabe1d0d65)
grep -v hello newfile 
## OUTPUT
cat newfile | grep -i "hello"
## OUTPUT
![312825594-d6dd2db3-b402-47b5-84f7-35e3b2038e37](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/4772fc5b-ccd6-43fc-9a0a-8f2aedd49938)
cat newfile | grep -i -c "hello"
## OUTPUT
![312826006-eb5b87a0-bb58-4854-a95f-1063a74d1320](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/c0aae82e-d776-4370-89bc-af678289efc0)
grep -R ubuntu /etc
## OUTPUT
![312826766-3c2aa26a-270d-42cf-9f04-ce10dc341942](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/d91f9569-966a-4e9c-bb4c-563b0309f1d5)
grep -w -n world newfile   
## OUTPUT
![312827082-04c00dca-5051-48a8-9333-c20a7bfd9328](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/9642725e-55b5-45fb-abb7-03bb7a626e22)
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
![312830227-2e1abf54-ea02-4eb8-b1f6-fff5fef677e0](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/87d9eaf7-52ab-4c3d-8a17-7a8dcbff9da1)
egrep -w '(H|h)ello' newfile 
## OUTPUT
![312830407-618c12f7-7069-417f-8616-481edb3859ad](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/4e75c7d8-0876-4a31-b57d-e518dea77c74)
egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT:
![312831660-25ac512f-2dfb-4038-925f-0b2818d8a912](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/cff1721f-ef9d-4017-b09f-5819d38f9f09)
egrep '[1-9]' newfile 
## OUTPUT
![312831851-27139ca7-cf2a-4851-8047-cd30f39b3da4](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/b524a716-44eb-440f-8a0c-54e3946a21e8)
egrep 'Linux.*world' newfile 
## OUTPUT
![312832122-65f9c469-4f04-4490-b7b8-75268e22fbce](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/39520a0a-4e56-4eb4-a9fb-f423009f82b0)
egrep 'Linux.*World' newfile 
## OUTPUT
![312832282-82dd6efa-a158-4a99-b1d3-60ec8d16d18c](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/02e2b2e1-1275-43ca-8401-75fb456c9224)
egrep l{2} newfile
## OUTPUT
![312832569-7878b983-dcc0-4fad-96df-0eabfaff7a9c](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/85d5c86f-8e96-4bce-a6eb-0c1e1df2e45c)
egrep 's{1,2}' newfile
## OUTPUT 
![312833039-5743baa7-5209-46b3-89ff-1398ce18f46d](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/37903004-546c-456c-9a5e-df9d6adbe2c1)
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
![312890522-6ea57d36-ce6c-4daf-8d42-39476d4518a4](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/959ca950-4e78-4b55-948c-248a9b3d85bd)
sed -n -e '$p' file23
## OUTPUT
![312890691-ecf7119f-656f-4dfe-89fa-6e49e0f9104c](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/f77a6e2f-c50c-492d-95b1-a51123417379)
sed  -e 's/Ram/Sita/' file23
## OUTPUT
![312891134-b00debdd-71b6-4595-8af4-8dd502d1e9d1](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/6e317d40-d2eb-4def-a72e-8af579f3d07c)
sed  '/tom/s/5000/6000/' file23
## OUTPUT
![312891653-a57f600b-bf98-4ccf-8ea3-c966a7e7097c](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/9b285f86-75f9-489f-84a3-d4e2c9a966ff)
sed -n -e '2,/Joe/p' file23
## OUTPUT
![312892738-65246582-bd0f-490b-8352-01ff92960b8f](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/38f165e3-3226-4484-b9d4-64cc6406d6a5)
sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![312891961-ca015e97-51d3-46b3-a4b2-883386487e96](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/440b3393-95ce-4592-a8bf-df6aee7bc518)

seq 10 
## OUTPUT
![312892165-d89684e2-6e84-4c92-b8f7-05a1c425b8f6](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/6dad107f-bde5-4150-bc59-62e066672f97)
seq 10 | sed -n '4,6p'
## OUTPUT
![312893738-cc2be9dc-529d-48a8-8006-8d9658906ac7](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/fd0d8d9f-8be4-4975-9917-9e8fcc696c8c)
seq 10 | sed '2,9c hello'
## OUTPUT
![312894013-1ff68b19-cd1a-4152-930d-191cdf0a400a](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/d5724181-c328-42b7-bcbc-24b6ad8b2226)
sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
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
## OUTPU
![312894885-4082ae2d-91db-4998-95a9-336e7a63e3e4](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/4846567c-430d-4ace-b230-fbb4f8e55c5e)
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
![312897587-94e1fa19-3646-4f72-97c8-eff4a0e11279](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/a378b0b6-5dda-4caf-83d6-e695dc24a1dc)
#Using tr command
![312897917-b286bcd8-f51d-4f2b-a6ae-c06dd89621f6](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/2f15f738-d171-4e4d-9890-085a826f367d)

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
![312898870-de7ce8af-1855-4dec-99f3-734859a20a00](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/486cde49-4d9b-4619-b033-6836d9a278ce) 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![312899242-255942df-5e83-4d32-b128-ee2fe540cebe](https://github.com/Lakshmi-v-Priya/OS-Linux-commands-Shell-script/assets/151720706/23f6f1f4-f73e-42b8-85a2-30ce416eb1ae)
#Backup commands
tar -cvf backup.tar *

# RESULT:
The Commands are executed successfully.
