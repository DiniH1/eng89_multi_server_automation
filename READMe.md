<p align=center>
    <img src=jenkins_pipeline_diagram.PNG>
</p>

# Jenkins Pipeline setup
### ssh and GitHub setup
- Fork from the repo provided https://github.com/khanmaster/eng89_multi_server_automation
- Generate a new ssh key in your .ssh directory using `ssh-keygen -t rsa -b 4096 -C "name@example.com"`
- Copy the newly generated key and paste it in Settings >> Deploy Keys >> Add new deply key
## Creating a new item
- On the jenkins page create a new item 
- Name the new item with proper naming conventions
- Select freestyle project
- Select discard old builds with a max of keeping 3 builds
- Select execute shell as the build set up
- write a line of code as a test e.g. `uname -a`
- Save and apply all changes
- Select build now on the dropdown menu next to your item
- Check the console output which should return `Success`
## Creating a pipeline
- Create a new item with the steps above
- Go to the first item created and select configure
- Select Post build actions >> Build other projects and select the name of the new item created
- Build the first item and both should run successfully
## Setting up webhooks on GitHub
-
