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
click on Manage Jenkins -> Global Security -> scroll down to Agent, click on fixed and enter below port
<img width="1403" alt="image" src="https://github.com/suhailasad/gitdemo/assets/63904274/ba95fb6b-5224-4204-bcc3-0ccab70c8cbd">

click on Manage Jenkins -> Manage Nodes and Clouds -> click on New node
<img width="1440" alt="image" src="https://github.com/suhailasad/gitdemo/assets/63904274/6f7fffc3-5e03-4d7b-8fbc-bb9c3d5e2689">

enter nodename and select permanent agent then click on create

<img width="1309" alt="image" src="https://github.com/suhailasad/gitdemo/assets/63904274/0292d887-1cfc-460c-9f9c-3b2f53bb1585">


enter description if you want.

<img width="1348" alt="image" src="https://github.com/suhailasad/gitdemo/assets/63904274/2fb9430d-cd84-4fde-8c8f-05e204888cdc">
Enter executors as 2

<img width="1204" alt="image" src="https://github.com/suhailasad/gitdemo/assets/63904274/0fe9dc40-6f47-4c9d-b9c8-f96d110de9a1">
enter label and select options which is shown in image

scroll down and click on save
<img width="1357" alt="image" src="https://github.com/suhailasad/gitdemo/assets/63904274/183d613d-c038-4058-aff1-d47de17f44c1">

click on the newslave node

<img width="1411" alt="image" src="https://github.com/suhailasad/gitdemo/assets/63904274/6fef38fe-3c0d-4225-a338-6acc866260d0">

Run the shown command in slave node for connection -> note: command url will change when you build jenkins, you need to run commands shown to you when you configure node not from below image
<img width="1430" alt="image" src="https://github.com/suhailasad/gitdemo/assets/63904274/16f23154-9f4d-4d98-b088-0c7c4bac34fd">

After we ran the commands on slave, we will get connected message 
<img width="1124" alt="image" src="https://github.com/suhailasad/gitdemo/assets/63904274/818177b4-4a83-4fe7-a802-92ce369070ef">

Also we will get connected message on Dashboard
<img width="1328" alt="image" src="https://github.com/suhailasad/gitdemo/assets/63904274/e01d6ed9-00c3-42e2-bff3-f1e7477e2078">



