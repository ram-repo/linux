# Linux Commands Reference

## 1. `ls`

The `ls` command lists the contents of a directory.
### 
```bash
ls [options] [directory]
```

* -l: Long listing format
* -a: Include hidden files
* -h: Human-readable file sizes
* -R: Recursively list subdirectories

## 2. `mkdir`

The `mkdir` command creates new directories.

```bash
mkdir [options] directory_name
```

* -p: Create parent directories as needed

```bash
mkdir new_directory
mkdir -p /path/to/new_directory
```

## 3. touch
The `touch` command creates empty files or updates the access and modification times of existing files.
 
```touch file_name```


```bash
touch newfile.txt
```

## 4. vi
The vi command opens the Vi text editor.
 
```bash
vi file_name
```
* Basic Commands in vi:
* i: Enter insert mode
* :w: Save the file
* :q: Quit vi
* :wq: Save and quit
* :q!: Quit without saving

```bash
vi example.txt
```

## 5. nano
The nano command opens the Nano text editor, which is more user-friendly than vi.

```bash
nano file_name
```

* Basic Commands in nano:
* Ctrl + O: Save the file
* Ctrl + X: Exit Nano
* Ctrl + K: Cut text
* Ctrl + U: Paste text

```bash
nano example.txt
```

## 6. echo
The echo command displays a line of text or a variable value.

```bash
echo [options] [string]
```

```bash
echo "Hello, World!"
echo $PATH
```

## 7. User Management
Adding a User:
The useradd command adds a new user.

```bash
sudo useradd [options] username
sudo useradd newuser
```

Changing a User's Password:
The passwd command changes a user's password.

```bash
sudo passwd username
```

```bash
sudo userdel -r username

```

## 8. Group Management
Adding a Group:
The groupadd command adds & Delete a new group.
```bash
sudo groupadd group_name
sudo groupadd newgroup
sudo groupdel GROUPNAME
sudo usermod -aG groupName user
sudo gpasswd -d user groupName
sudo deluser user groupName
```
Adding a User to a Group:
The usermod command modifies a user's account, including adding them to a group.
```bash
sudo usermod -aG group_name username
sudo usermod -aG newgroup newuser
```

## 9. ssh
The ssh command is used to connect to a remote machine securely.

```bash
ssh [user@]hostname [command]
ssh user@remotehost
```
Setting Permissions for SSH Keys:
Create a .ssh directory in the user's home directory if it doesn't exist:
```mkdir -p ~/.ssh ``` 
Set appropriate permissions:

```bash
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys
```
