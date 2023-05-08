# File-Permissions-In-Linux
# This Project was done in my Google Cybersecurity training

<b>Project description</b>

Using the chmod command in the terminal, I modified the permissions of the identified files and directories to the correct level of authorization.

<b>Check file and directory details</b>

From the output of the command, it is clear that there are one directory named drafts, one hidden file called .project_x.txt, and five other project files. Additionally, the first column of the output, which is a 10-character string, indicates the permissions granted on each file or directory.

![image](https://user-images.githubusercontent.com/131769679/236787219-71f2289c-0846-4ab9-8c08-a52c7f0dd15a.png)

<b>Describe the permissions string</b>

The 10-character string contains information that can be used to determine file access authorization and specific permissions. It can be broken down into the following components:

The first character indicates the file type and is either a d for directory or a hyphen (-) for a regular file.

The second to fourth characters indicate the read (r), write (w), and execute (x) permissions for the user. If a hyphen (-) appears instead of one of these characters, it means that the user is not granted that permission.

The fifth to seventh characters indicate the read (r), write (w), and execute (x) permissions for the group. Similarly, a hyphen (-) indicates that the group does not have that permission.

The eighth to tenth characters indicate the read (r), write (w), and execute (x) permissions for all other users on the system, apart from the user and group. Again, a hyphen (-) indicates that these users do not have that permission.

<b>Change file permissions</b>

In order to adhere to the organization's security policy, it was decided that 'other' users should not have write access to any files. After reviewing the file permissions I previously retrieved, I determined that the 'other' owner type had write access to the file named project_k.txt, which needed to be removed.

To accomplish this, I utilized the chmod command to modify the file permissions of project_k.txt, specifically removing the write permission for the 'other' owner type. The following code demonstrates the specific commands used to achieve this:

![image](https://user-images.githubusercontent.com/131769679/236787263-5c4b688e-81c3-471f-ae00-643818e892d3.png)

<b>Change file permissions on a hidden file</b>

I modified the permissions of project_x.txt to restrict write access to all users except for the owner and the group, but allow read access. The following code showcases the Linux commands that I used to make these changes:

![image](https://user-images.githubusercontent.com/131769679/236787296-5844c3cb-731d-48e1-b812-7e9a68f31d51.png)

<b>Change directory permissions</b>

To restrict access to the drafts directory and its contents, I modified the permissions using the following Linux commands:

![image](https://user-images.githubusercontent.com/131769679/236787374-a02bc71b-5c10-4986-9c81-a355f20b7c54.png)

<b>Summary</b>

In order to match the desired level of authorization for files and directories in the projects directory, I made multiple changes to permissions. Firstly, I checked the directory's permissions using ls -la which helped me make informed decisions in the following steps. I then used the chmod command multiple times to modify permissions on files and directories.
