# Updating Motion Eye Deployed
This implementation contains 2 places for updates, the packages contained and the overall project.

### Updating the packages
Updating the packages is simple, the built-in packages get regular updates supplied by the maintainers. As described in the main directory the project is built on the back of docker, to update you will just need to grab the latest version.

#### 1. Navigate to the projects running files
The Project is stored in the srv directory to navigate to the srv directory use the following;
```bash
cd /srv/motion_eye_deployed
```

#### 2. Pull the latest updates
Once navigated we will utilise docker-compose which is a companion package to docker in which this is built on. Docker Compose manages the current containers based on what is described in the docker-compose.yml in the projects root.

To pull the updates run the following;
```bash
docker-compose pull
```

### 3. Install the updates
This part is straight forward we will again use the docker-compose companion to restart the containers currently running. Be aware this will mean there will be a short amount of down-time. Run the following:
```bash
docker-compose down; docker-compose up
```

### Updating the whole package
To make life simple I am storing all the files to this project in source control using Github, when in the future I make a change to the repo I ensured it should be straight forward process.

#### 1. Navigate to the projects running files
Much like above you will need to navigate to the project. The Project is stored in the srv directory to navigate to the srv directory use the following;
```bash
cd /srv/motion_eye_deployed
```

### 2. Pull the changes
As stated the changes are stored in source control. I have added to the Nuc a token in which will allow the it to regularly pull changes where necessary. Simply run the following;
```bash
git pull
```

### 3. Restart and Install the updates
Installing the updates will be really easy.
```bash
docker-compose down; docker-compose up --build
```