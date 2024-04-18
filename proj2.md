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








