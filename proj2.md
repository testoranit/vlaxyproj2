![image](https://github.com/testoranit/vlaxyproj2/assets/124513439/08b4092e-c0d1-4d61-a1f8-7f3e55cef037)

GitHub URL for source code: https://github.com/ravdy/tweet-trend-new.git

Documentation: https://github.com/ravdy/devops-workshop.git

INstall VScode,terraform,git bash on ur local
clone the above workshop repo

install awscli and configure it(createIAM user,and security,cred)

create all terraform code in separate direcorty of the glit clone so that u can commit changes to it hub.
create_ec2_instance.tf file in ur local
and spin up an ec2 instance(for testing purpose)
destroy the instance and then push this file wit folder to github.
create .gitignore and include default files created by terraform check .gitignore

2)create ec2 with sg using terraform
since u already commited the test ec2 files above so u can delete these files from ur dir including the tfstate files.
now create an newfile ceate_ec2_with_sg.tf for testing

and commit to github

3)create 3 ec2 usin foreach with sg and vpc and subnets
and commit this file to github

SInce we need 3 ec2 1 jenkins master 1 jenkins slave and 1 ANsible server.

Jenkins slave should have maven since it is a build server.

take ansible server
1)install ansible
2)Add inventory
3)cpoy private key on to ansible
4)test connection

NOw, add Jenkins and Maven nodes as managed nodes to ansible.

create hosts file in /opt directory using root on as server

[jenkins-master]
10.1.1.145

[jenkins-master:vars]
ansible_user=ubuntu
ansible_ssh_private_key_file=/opt/18apr.pem

[jenkins-slave]
10.1.1.227

[jenkins-slave:vars]
ansible_user=ubuntu
ansible_ssh_private_key_file=/opt/18apr.pem


make sure u copy pem file in /opt dir
and give it 400 permissions
test connansible all  -i hosts -m ping

****************
Write ansible playbook to install jenkins
1)Add jenkins repo to system
2)add repo to system
3)install dependenceis
4)install jenkins

commit hosts file to github

#)write ansible playbook to install jenkins on MAster
ANsible folder on github jenkins-master-setup.yaml
execute the playbook 

run the above playbook

U know have jenkins installed on Master
login to Jenkis master using url:8080
install sugested plugins.
#)Now write ansible playbook to install maven server

1)update the system
2)install java
3)download maven packages
4)extract
5)add path to bash_profile

check githuhub ansible folder and execute v1-jenkins-slave-setup.yaml playbook


************
understand src code
eg:- tweet trent on ur github repo
this repo has app code to build and also have some test cases.

**************
Jenkins--Master slave config.

1)master where u configured dashboard
Managecred-->system-->global cred-->sshuser with private key
U now added slave system credentials to master

2)go to manage jenkins-->bild-in Node-->+new node add slave node details

create a sample job from js dashboard to test the connectivity

now,
clone the app code tweet to local
and cretae a jenkins file and push it to ithub
so that u can do a sample test job run

#)createmultie branch pieplien

3)enable github webhook.
*************
SonnarQube and SonarCube scanner
for static code analysis to check code quality
![sonarQube](https://github.com/testoranit/vlaxyproj2/assets/124513439/9fa2eb2e-e2d9-4184-93ef-1f9825b59195)


##########)Integrate Jfrog with jenkis
![Artifact integration](https://github.com/testoranit/vlaxyproj2/assets/124513439/2e55f8e8-0e9e-44a7-bece-001813b0f499)

****************************
U can install docker on maven server or sepearet docker host or on ansible server
here we are using maven server




