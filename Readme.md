# Dockerized 2048 Game

## Description
This project involves creating a Dockerfile to containerize a 2048 game clone from the [Govindsinghsodhi/2048](https://github.com/Govindsinghsodhi/2048) repository. The game is served using Nginx within a Docker container.

## Key Features
- **Base Image:** `ubuntu:22.04`
- **Installed Packages:** `nginx`, `unzip`, `curl`
- **Automated Setup:** Downloads, extracts, and configures the 2048 game
- **Exposed Port:** 80 for Nginx

## Setup and Deployment
1. **Dockerfile**: The Dockerfile used for this setup can be found [here](https://github.com/Govindsinghsodhi/2048/blob/master/Dockerfile).
2. **AWS EC2 Instance**: The Dockerized game is hosted on an AWS EC2 instance. The instance is configured to run the Docker container and make the game publicly accessible.

## Running the Project
1. **Launch an AWS EC2 Instance**:
   - Set up an EC2 instance using Ubuntu 22.04.
   - Ensure that port 80 is open in the security group settings.
 
  
2. **Install Docker on the EC2 Instance**:
   ```bash
   sudo apt-get update
   sudo apt-get install -y docker.io
   ```

3. **Build and Run the Docker Container**:
   ```bash
   docker build -t 2048-game .
   docker run -d -p 80:80 2048-game
   ```

4. **Access the Game**:
   - Open a web browser and navigate to the public IP address of the EC2 instance to play the game.

## License
This project is licensed under the MIT License.

## Contact
For any questions or issues, please contact my eamil-(govindsinghsodhi18@gmail.com).

