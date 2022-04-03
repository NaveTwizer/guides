# Deploying a Node.JS app (or a web app) on a VPS

## 1. SSH into your VPS
You can SSH into your vps with the following command. This command will allow you to access the terminal of your vps on your computer.

Run this command on your terminal (Unix based OS users can use this directly in their terminal (All Linux Distributions and MacOS), Windows users can use Git Bash (If you do not have Git Bash installed, I recommend installing it to use unix like terminal in windows.))


```bash
ssh <username>@<ip>
```
Replace \<username\> and \<ip\> with your vps username and ip.

Example
```bash
ssh root@127.0.0.1
```

Then you will be prompted for your password (This is the root password of your vps (assuming you are having a linux based vps))

Once you enter your root password, You will be on ssh of your vps.

Any command you enter here will be run on your vps, if you are logged in as root, Type every command here with caution since every command will be like sudo.

All commands after this are expected to be run on SSH

## 2. Uploading your code to VPS
There are several ways to do so, I recommed using git so that's how we will do it.

- Upload your code to GitHub or any other repo hosting service.
- Mark the name of the repository and login to git using your terminal (you can do this in the next step too.)
- Clone your repository on VPS with the following command.
```bash
git clone https://github.com/<username_or_orgname>/<reponame>
```

If the above command fails with an exception like command "git" not found, install git on your vps.

Replace \<username\_or\_orgname> with your GitHub/Repository Hosting service username or organization name.

Replace \<reponame\> with the name of the repository you created in the step prior to this one.

This command will prompt you for username and password if you haven't logged in already.

Enter your username and password (Note: Support for password authentication was removed on August 13, 2021, You need to use a PAT (Personal Access Token) instead of password to sign in.)


## 3. Setting up Node.JS and Running it as a process

This assumes you have Node.JS and npm installed on your VPS, If not install them.

- Go to the folder and run the following command to install all your dependencies
```bash
npm install
```

This will create a node\_modules directory with all your dependencies

- Run your app like you would normally to test if it is working. If it is a web app, Go to the ip in your browser and the port (You can use port 80 for http and port 443 for https and then omit adding port)

Example:
```bash
node app.js
```

- If there is a process already using the port, And if you do not wish that process to run on that port, you can kill it (Example: Apache, kill using `apachectl -k stop`)

- Now try to rerun your app if the port was busy last time when you ran.

- If it works as expected proceed to next step, If not please review whether your code is correct and that you have followed all steps correctly

- Now if you close the terminal you are using SSH from the node instance will stop. To keep the node app running in background, Use a process manager, I recommend pm2.

- Install pm2 on your VPS

```bash
npm install -g pm2
```

- Initialize pm2
```
pm2 init
```

- Make sure you are in your app folder and run
```
pm2 start <args>
```

These \<args\> with your args that come after node.

For example, `node app.js` becomes `pm2 start app.js`

- To check console logs of your app, run pm2 logs this will show you last 15 lines of console log and error log and a live preview of any new logs as they come

## 4. Updating your code on VPS
If you want to change your code on VPS, and are using git it is very simple to do so.

- Update your code on github using git add, commit, push

- Update your code on VPS by pulling it.

```bash
git pull
```

- To restart your process, you can do either one of these:

1. Restart the app normally using pm2
```bash
pm2 restart 0
```

2. Kill and Start your app
```bash
pm2 kill
```

After running this start your app using pm2 (mentioned above)

# Congrats!!
Congrats your Node.JS app has been deployed on a VPS!!
