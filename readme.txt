Config for ctf :
---------------------
npm install -g juice-shop-ctf-cli
juice-shop-ctf


Install CTFd on Docker
----------------------------
Clone the CTFd repository with git clone https://github.com/CTFd/CTFd.git
Modify the docker-compose.yml file from the repository to specify a SECRET_KEY environment for the CTFd service.

  environment:
    - SECRET_KEY=MySuperSecretKey
    - UPLOAD_FOLDER=/var/uploads
    - LOG_FOLDER=/var/log/CTFd
    - DATABASE_URL=mysql+pymysql://root:ctfd@db/ctfd
    - REDIS_URL=redis://cache:6379
    - WORKERS=4

Run docker-compose up 
Go to the section Admin > Config > Backup and choose Import
Select the juice-shop-ctf degenerated .zip file and make sure only the Challenges box is ticket. Press Import.