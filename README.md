# Docker-Java-Kubernetes Project

## Overview
This project demonstrates deploying Java applications with Docker and Kubernetes. We'll be using Maven to build the JAR file for this project. The build process will be performed on a local machine (Mac), and then we'll proceed to build a Docker image and push it to Docker Hub.

## Prerequisites
Before getting started, ensure you have the following prerequisites installed on your system:
- Java Development Kit (JDK)
- Homebrew (for macOS package management)
- Docker Desktop
- Kubernetes (kubectl) - Optional for local Kubernetes deployment
- Docker Hub Account (for pushing Docker images)

## Installing Maven with Homebrew
1. Open Terminal.
2. Run the following command to update Homebrew:

brew update

3. Install Maven using Homebrew:

brew install maven


## Setting Up Environment Variables
To use Maven and other Java-related tools efficiently, it's recommended to set up the `JAVA_HOME` and `M2_HOME` environment variables.
1. Open Terminal.
2. Edit the `.bash_profile` or `.zshrc` file in your home directory. You can use any text editor of your choice, for example:

nano ~/.bash_profile

export JAVA_HOME=$(/usr/libexec/java_home)
export M2_HOME=/usr/local/Cellar/maven/<your_maven_version>/libexec
export PATH=$PATH:$M2_HOME/bin


## Project Structure
The project is structured as follows:
- `src/`: Contains the source code of the Java application.
- `pom.xml`: Maven project configuration file.
- `Dockerfile`: Dockerfile for building the Docker image.
- Other project-related files and directories.

## Building the Project
1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Run Maven to build the JAR file:


Sure! I'll add steps for installing Maven using Homebrew and also include a section for setting up environment variables.

markdown
Copy code
# Docker-Java-Kubernetes Project

## Overview
This project demonstrates deploying Java applications with Docker and Kubernetes. We'll be using Maven to build the JAR file for this project. The build process will be performed on a local machine (Mac), and then we'll proceed to build a Docker image and push it to Docker Hub.

## Prerequisites
Before getting started, ensure you have the following prerequisites installed on your system:
- Java Development Kit (JDK)
- Homebrew (for macOS package management)
- Docker Desktop
- Kubernetes (kubectl) - Optional for local Kubernetes deployment
- Docker Hub Account (for pushing Docker images)

## Installing Maven with Homebrew
1. Open Terminal.
2. Run the following command to update Homebrew:
brew update

arduino
Copy code
3. Install Maven using Homebrew:
brew install maven

arduino
Copy code
4. After the installation completes, verify the Maven installation by running:
mvn -version

markdown
Copy code

## Setting Up Environment Variables
To use Maven and other Java-related tools efficiently, it's recommended to set up the `JAVA_HOME` and `M2_HOME` environment variables.
1. Open Terminal.
2. Edit the `.bash_profile` or `.zshrc` file in your home directory. You can use any text editor of your choice, for example:
nano ~/.bash_profile

vbnet
Copy code
3. Add the following lines to the file to set up environment variables:
export JAVA_HOME=$(/usr/libexec/java_home)
export M2_HOME=/usr/local/Cellar/maven/<your_maven_version>/libexec
export PATH=$PATH:$M2_HOME/bin

vbnet
Copy code
Replace `<your_maven_version>` with the version of Maven installed by Homebrew. You can find the version by running `brew info maven`.
4. Save the file and exit the text editor.
5. To apply the changes, either restart Terminal or run:
source ~/.bash_profile

Copy code
or
source ~/.zshrc

## Project Structure
The project is structured as follows:
- `src/`: Contains the source code of the Java application.
- `pom.xml`: Maven project configuration file.
- `Dockerfile`: Dockerfile for building the Docker image.
- Other project-related files and directories.

## Building the Project
1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Run Maven to build the JAR file:

mvn clean package

4. Once the build is successful, a JAR file will be created in the `target/` directory.

## Building Docker Image
To build the Docker image, follow these steps:
1. Ensure Docker Desktop is running on your local machine.
2. Navigate to the project directory.
3. Build the Docker image using the provided Dockerfile:

docker build -t <image_name>:<tag> .

docker push <dockerhub_username>/<repository_name>:<tag>


Credit: https://github.com/danielbryantuk/oreilly-docker-java-shopping/
