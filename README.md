# Managing-Permissions-Using-Linux
In this project the Cybersecurity analyst was tasked with managing permissions of different groups of users thereby ensuring permissions and ensure they are aligned with the principle of least privilege.  

In Linux, permissions are represented with a 10-character string. Permissions include: "r","w","x". 
read: for files, this is the ability to read the file contents; for directories, this is the ability to read all contents in the directory including both files and subdirectories (r), write: for files, this is the ability to make modifications on the file contents; for directories, this is the ability to create new files in the directory(w), execute: for files, this is the ability to execute the file if it’s a program; for directories, this is the ability to enter the directory and access its files (x)

The 10-character string can be deconstructed to determine who is authorized to access the
file and their specific permissions. The characters and what they represent are as follows:
● 1st character: This character is either a d or hyphen (-) and indicates the file type. If it’s
a d, it’s a directory. If it’s a hyphen (-), it’s a regular file.

● 2nd-4th characters: These characters indicate the read (r), write (w), and execute (x)
permissions for the user. When one of these characters is a hyphen (-) instead, it
indicates that this permission is not granted to the user.
● 5th-7th characters: These characters indicate the read (r), write (w), and execute (x)
permissions for the group. When one of these characters is a hyphen (-) instead, it
indicates that this permission is not granted for the group.
● 8th-10th characters: These characters indicate the read (r), write (w), and execute (x)
permissions for other. This owner type consists of all other users on the system apart
from the user and the group. When one of these characters is a hyphen (-) instead,
that indicates that this permission is not granted for other.



First analyst was tasked with checking current permissions for users in the projects directory: 


![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/efb09933-5202-4c1f-808d-c405a8fa54a5)
![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/bfc1b636-4655-455b-8f51-1ca40ca8e2e2)
![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/ae1f8eff-da4f-4f1b-9e88-c4e8c79d6b2e)

Next reviewed if there were any hidden files located in the directory "projects":


![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/5597ae8e-c0f5-43d4-8d96-bd20e274cc7b)


Next with changing file permissions to determine whether any files have incorrect permissions in projects and then change the permissions as needed. This action will remove unauthorized access and strengthen security on the system:


Viewed permissions once again:

![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/f4cc8bec-0422-45bd-abb0-097cd58c039e)


Changed permissions so that the owner type of "other" wouldn't have write permissions in project_k.txt:

![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/f3637feb-6b2a-45cf-93ad-e7acb01f5b9e)


Checked that permissions had been updated :

![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/61a45dea-c28f-4075-9e08-76b9b86de8c4)


Next changed permissions of the project_m.txt file so that the group doesn’t have read or write permissions:

![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/b697e048-ad22-4dcc-b6f4-8a96dba8c97b)
![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/0686f464-4fae-4a14-b4e9-549906696a90)


Next changed file permissions on a hidden file. This action will further remove unauthorized access and strengthen security on the system: 

First reviwed current permissions in the hidden file: 

![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/8a3457a2-0fbc-4b14-937e-40b428d6ad69)


Then proceeded to change those user permission that were given incorrectly to users and group: 

![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/1360496d-90b3-41ca-9b9f-5dcf114c03e3)
![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/7fb78649-3865-4253-b33b-ac654ac9e517)


Finally tasked with changing directory permissions for group users: 

![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/67a52c9c-0213-4b69-8197-73f35dcff29e)
![image](https://github.com/MarcoSantibanez/Managing-Permissions-Using-Linux/assets/138132151/4e3bc054-cc83-4b50-a3c4-a2fae004cba0)


Summary:

I changed multiple permissions to match the level of authorization my organization wanted for
files and directories in the projects directory. The first step in this was using ls -la to
check the permissions for the directory. This informed my decisions in the following steps. I
then used the chmod command multiple times to change the permissions on files and
directories.














