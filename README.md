# aws-assignment

This project demonstrates deployment of a Dockerized Flask web application on AWS using EC2, Application Load Balancer (ALB), and Auto Scaling Group (ASG).


---

#  Project Architecture

User → Application Load Balancer → Auto Scaling Group → EC2 → Docker → Flask App

---

# Tech Stack

- Python Flask
- Docker
- Docker Compose
- AWS EC2
- Application Load Balancer (ALB)
- Auto Scaling Group (ASG)
- GitHub

---

#  Project Structure

aws-devops-assignment/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
├── README.md
├── screenshots/

### Clone repo
git clone <your-repo-link>

cd aws-devops-assignment

### Run Container
docker compose up --build

### Open browser

http://localhost:5000

## Docker Implementation
- Created Dockerfile for Flask app
- Used docker-compose for multi-container management
- Exposed port 5000
- Container runs app successfully

### Commands 
docker compose up -d --build
docker ps

## AWS Setup
## EC2 Setup
- Launched Ubuntu t2.micro instance
- Installed Docker & Docker Compose
- Cloned GitHub repository
- Started containers using docker-compose

## Elastic IP
- Allocated and associated Elastic IP for permanent access

## Load Balancer (ALB)
- Created Application Load Balancer
- Created Target Group (port 5000)
- Configured health checks (/)
- Forwarded traffic from port 80 → 5000

## Auto Scaling
- Created Launch Template
- Attached Auto Scaling Group
- Configured CPU-based scaling policy
- Automatic instance creation during high load

---

### Application access through EC2
http://<Elastic-IP>:5000

### Through Load Balancer
http://<ALB-DNS> 





