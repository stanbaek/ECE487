# ✔️ Preflight: Software Setup

## 📜 Agenda
- Create a Bitbucket repository.
- Configure git repository.
- Install and Configure PyCharm

:::{note}
Don’t worry if it doesn’t work right. If everything did, you’d be out of a job.
:::

## 💻 Procedure

### Create Bitbucket Repository

- Create a <a href="https://bitbucket.org/" target="_blank">Bitbucket</a> account if you don't have one.
- Log in <a href="https://bitbucket.org/" target="_blank">Bitbucket</a>.
- Browse to <a href="https://bitbucket.org/stanbaek2/ece487_wksp/src/master/" target="_blank">https://bitbucket.org/stanbaek2/ece487_wksp/src/master/</a>.
- Click on the three dots ($\cdots$) on the top of the right-hand navigation for more options. 
- Select `Fork this repository`. 
- Enter "ECE487" for `Project`.
- Name this new repository ECE487\_LastName\_FirstName.
- Ensure the access level is `Private repository`.
- Give your instructor (Dr. Baek) read access: Click `Invite` and then click `Add members`. Provide him **read access**. Dr. Baek's email address ![baek](https://img.shields.io/badge/stanley.baek@afafacademy.af.edu-red)    
- Note: The gif animation below has been adpated from ECE382. You must use ECE487 in place of ECE382.
<br>


```{image} ./figures/HW1_GitFork.gif
:width: 720
:align: center
```
<br>

```{important}
Please name your repository as ECE487_LastName_FirstName. This will help instructors find your repository easily.
```

- You may need to create a Bitbucket `app password` as follows.
- Click `Your Profile` on the top of the right-hand navigation and then click `Personal Settings`. 
- Click `App Passwords` and then click `Create app password`. 
- Write your preferred label and select permissions as needed.
- Click `Create`.
- Save the password as you cannot view it after you create it.

```{image} ./figures/BitBucketAppPassword.gif 
:width: 720
:align: center
```
<br>

### Install Git

- Browse to  <a href="https://git-scm.com/download/win" target="_blank">git-scm.com</a> to download `64-bit Git for Windows setup`
- Install Git with the default settings. Git is already installed on Mac. 
- Create a folder named `workspace` under your home folder, e.g., C:\Users\stanley.baek\workspace. 
- Right-click the `workspace` folder and select `Git Bash Here` as shown below.   
- From your repository in Bitbucket, click Clone and copy the command that begins with _git clone_ by clicking on the copy button as shown below.  
- Paste it within the Bash terminal (middle-click, right-click > Paste, or `Shift+Ins` to paste) and add a space followed by a **_period_** as shown below. The **_period_** at the end means that the destination is the **_current folder_**. Hit Enter.
- If it asks for a password, enter the app password you saved in the previous step.
- Notice that you have `(master)` at the end of the folder name. 

```{image} ./figures/GitClone.gif
:width: 720
:align: center
```
<br>

- The figure below shows an example of a local `workspace` folder on your computer.

```{image} ./figures/HW1_Workspace.png
:width: 580
:align: center
```

<br>

- Go back to Git Bash. If you have already closed it, right-click on an empty space inside the `workspace` folder and select `Git Bash Here`.
- Type `git remote -v`.  It will return two lines showing that `origin` is your remote repository at bitbucket.org for both fetch and push. 
- Type `git remote add upstream https://stanbaek2@bitbucket.org/stanbaek2/ece382_wksp.git` (or copy & paste) and hit `Enter`.
- Type `git remote -v`.  It will now return four lines showing that `upstream`
is the original instructor's repository that you forked from.

```{image} ./figures/GitAddUpstream.gif
:width: 640
:align: center
```
<br>

- Whenever there are any updates on the original code, you will be asked to run `git fetch upstream` to update your local files.  
- Your default push and pull repository is `origin`, which is your Bitbucket repository. 

```{image} ./figures/FetchUpstream.png
:width: 320
:align: center
```
<center>
Image is sourced from <a href="https://stackoverflow.com/questions/9257533/what-is-the-difference-between-origin-and-upstream-on-github/9257901#9257901" target="_blank">Stakeoverflow</a>
</center>

<br>



<br>


### Install and Configure PyCharm

- Download the latest version of [PyCharm Edu](https://www.jetbrains.com/edu-products/download/#section=pycharm-edu) and install it on your computer.
- Ensure you have the installation options checked as shown below. 


<br>

- Start PyCharm and create a new project.
- Ensure the project location is `PycharmProjects` under your home folder, e.g., C:\Users\stanley.baek\PycharmProjects.
- The location of virtual environment should be `env` under `PycharmProjects`, e.g., C:\Users\stanley.baek\PycharmProjects\env.


<br>

- Open `Settings` under the `File` menu and browse to `Project: PycharmProjects` > `Python Interpreter`.
- Click `+` 
- Search for `numpy` and click `Install Package`.
- Install the following packages
    - `matplotlib`
    - `spatialmath-python`
    - `sympy`
    - `roboticstoolbox-python`
    - `opencv-python`
    - `serial`
    

```{image} ./figures/InstallNumpy.gif
:width: 720
:align: center
```
<br>

- Go back to Git Bash. If you have already closed it, right click on an empty space inside the `PycharmProjects` folder and select `Git Bash Here`.
- Type `git add -A` or `git add -all` and hit `Enter`.
- Type `git commit -m "Initial commit."` and hit `Enter`.
- Type `git push` as shown below
- Enter your username and password if prompted.


- In the future you will repeat these three steps when committing your changes:
    - git add -A
    - git commit -m "Comment"
    - git push

- Refresh your Bitbucket repository to observe the new files as shown below


```{image} ./figures/BitBucketPushed.png
:width: 640
:align: center
```
<br>

```{Attention} 
It is your responsibility to check your files have been successfully pushed to your Bitbucket repository. Always visit your Bitbucket repository after you push your assignments to the repository.
```

## 🚚 Deliverables

Take screenshots of the following and submit them via Gradescope.  Use `Snip & Sketch` (Win+Shift+S) in Windows 10 or Shift+CMD+4 in Mac to take a screenshot. Save it in `png` or `jpg`.  

```{Warning}
Take a picture of your screen with a mobile device or digital camera and upload it in
Gradescope to show that you have no idea what sampling aliasing (you learned it in ECE215) is and
you are not qualified for bachelor's degree in ECE. You will lose 30 points every time you submit a picture of a computer screen taken by your phone or mobile device. Yes, I am serious..., and it takes more time if you do.
```

### Deliverable 1
- Provide a screenshot of your Bitbucket repository as shown below 

```{image} ./figures/BitBucketPushed.png
:width: 640
:align: center
```
<br>

### Deliverable 2

- Take a screenshot of your PyCharm settings as shown below

<br>







