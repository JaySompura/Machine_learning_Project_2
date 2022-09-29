# Machine_learning_Project_2
Creating conda environment 
```
conda create -p venv python==3.9 -y
```

Activate Anaconda Virtual environment
```
conda activate venv/ 
```
OR
```
conda activate venv
```

Create and Run requirements.txt with following command
```
conda -r requirements.txt
```

Push the newly created file - app and README and requirements.txt except venv(which will be inside) using following command
```
git add filename1,filename2 

```

To add all file from current directory
```
git add .
```

To check whether files are added to the git or not 
```
git status
```
To check all version maintained by git 
```
git log
```

To create version/commit all changes by git
```
git commit -m "message"
```

To send version/changes to the main branch of github
```
git push origin main
```

To check remote url (from where the data would be fetched or to the location where the data would be pushed)
```
git remote -v
```

To check the current branch
```
git branch 
``` 

Note: To ignore file or folder from git we can write name of file/folder in .gitignore file.

To setup CI/CD pipeline in heroku we need 3 information

1. HEROKU_EMAIL = sompura2019@gmail.com
2. HEROKU_API_KEY = 
3. HEROKU_APP_NAME = jay-ml-regression-app

BUILD DOCKER IMAGE 
```
docker build -t <image_name>:<tag_name> .
```
Note: The name of image in docker must be always in small letters. Generally tag_name = latest always.

FOR EXAMPLE HERE THE CODE WOULD BE FOLLOWING 
```
docker build -t ml-project:latest .
```

To list docker images 
```File
docker images
```

To run docker image -- Get IMAGE ID from previous command and write it whose image we wish to run  
```
docker run -p 5000:5000 -e PORT=5000 <IMAGE ID>
```

To check running container in docker 
```
docker ps
```

To stop docker container - Get CONTAINER ID from previous command (docker ps)
```
docker stop <CONTAINER ID>  for e.g. docker stop 18a80486e31a
```

To upload model on Heroku create a .github folder and then create a workflows folder in it. Then create a main.yaml file and which contains the given code. 

Commit changes to github with message = "Added github work for Heroku deployment" and add secrets of heroku key, email and app name as given in main.yaml file. Make sure that name of secret should same as given in main.yaml file.