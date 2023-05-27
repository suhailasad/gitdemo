## Jenkins Installation


### Master node configuration

#### Step 1
```
sudo yum install wget -y
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
sudo yum install java-11-openjdk -y
sudo yum install jenkins -y
sudo systemctl daemon-reload
sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
```

### Slave node configuration

#### Step 2
```
sudo yum install java-11-openjdk -y
useradd -m -d /home/jenkins -g jenkins jenkins
id jenkins  # confirming
su jenkins
cd ~
mkdir jenkins-agent 
cd jenkins-agent
```

#### Go to jenkins dashboard
click on Manage Jenkins -> Manage Nodes and Clouds -> click on New node
<img width="1440" alt="image" src="https://github.com/suhailasad/gitdemo/assets/63904274/6f7fffc3-5e03-4d7b-8fbc-bb9c3d5e2689">


