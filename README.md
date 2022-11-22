PROJECT 5

CLIENT-SERVER ARCHITECTURE WITH MYSQL

Client/Server Architecture Using MySQL Relational Database Management System 

STEP 1
- I created two instances in AWS with a free tier option for this project and named them 'mysql server' and 'mysql client' respectively. 

STEP 2
- On Mysql Linux Server, i installed MYSQL SERVER Software
- To do that, i simply ran the commands below;
- sudo apt update -y
- sudo apt install mysql-server -y
- sudo systemctl enable mysql
<img width="716" alt="Screenshot 2022-11-22 at 1 29 08 PM" src="https://user-images.githubusercontent.com/115854902/203402856-cc1ad1a8-dcbd-470d-a361-17b26c0344ba.png">
<img width="716" alt="Screenshot 2022-11-22 at 1 31 18 PM" src="https://user-images.githubusercontent.com/115854902/203402964-1b6e8a87-3a7f-4a84-aa58-336b7acdbaad.png">
<img width="716" alt="Screenshot 2022-11-22 at 1 32 48 PM" src="https://user-images.githubusercontent.com/115854902/203403201-8e2384f6-e54e-4fd3-8d88-38b05fd5db16.png">

STEP 3
- I also installed MYSQL CLIENT Software on Mysql Linux Client using the commands below
- sudo apt update -y
- sudo apt install mysql-client -y
<img width="723" alt="Screenshot 2022-11-22 at 1 36 29 PM" src="https://user-images.githubusercontent.com/115854902/203405236-47f3580b-1589-4a4e-8ff3-e267340c4af5.png">
<img width="723" alt="Screenshot 2022-11-22 at 1 38 16 PM" src="https://user-images.githubusercontent.com/115854902/203405309-bfd4e8cc-6613-4335-8b0d-57a173d7eb01.png">

STEP 4
- On Mysql Server Instance, i added a new security group rule 'MYSQL/AURORA TCP Port 3306'
- For extra security reasons, i allowed access only to the 'private IP address' of 'mysql client'
<img width="1440" alt="Screenshot 2022-11-22 at 8 45 45 PM" src="https://user-images.githubusercontent.com/115854902/203407372-a6ec6e9b-e827-484c-a641-50833e1514e7.png">

STEP 5
- Configure Mysql Server to allow connections from remote hosts.
- To configure mysql server instance, i ran the command ' sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf'
- Inside this file, i replaced the bind address from 127.0.0.1 to 0.0.0.0
<img width="718" alt="Screenshot 2022-11-22 at 1 55 58 PM" src="https://user-images.githubusercontent.com/115854902/203409348-545ed557-3e48-477c-b4ab-0724514a731b.png">

I CREATED A NEW USER IN MYSQL SERVER INSTANCE IN ORDER TO BE ABLE TO CONNECT TO MYSQL SERVER FROM MYSQL CLIENT.
- To do this, i ran the command "sudo mysql" and then went ahead to input this commands below inside mysql as shown by the images below;
<img width="721" alt="Screenshot 2022-11-22 at 5 16 38 PM" src="https://user-images.githubusercontent.com/115854902/203412322-6d305427-ea39-4280-a360-8e3d0caad1cf.png">

STEP 6
- CONNECTING TO MYSQL SERVER FROM MYSQL CLIENT
- I used the details of the user I created in mysql server instance to connect to mysql client instance.
- I ran this command to connect on my mysql client instance "mysql -u chigozie -h (private IP address of mysql server) -p"

STEP 7
- To check that i have successfully connected to a remote mysql server and i can perform SQL Queries, i ran  the command "Show databases";
- i got a confirmatory output that showed that i have successfully completed the project and I have deployed a fully functional MYSQL Client-Server set up.
<img width="721" alt="Screenshot 2022-11-22 at 6 33 36 PM" src="https://user-images.githubusercontent.com/115854902/203416823-c1e5815c-ae5e-4d71-a649-d845ed11c52f.png">









