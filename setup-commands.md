# EC2–1: Private Database EC2 (MariaDB Server)
sudo yum update -y
sudo dnf install mariadb105-server -y
sudo systemctl start mariadb
sudo systemctl enable mariadb
sudo systemctl status MariaDB
sudo mariadb
sudo mariadb

# EC2–2: Web/Application EC2 (Apache + PHP)
sudo yum update -y
sudo yum install git httpd php php-mysqli mariadb105 -y
sudo systemctl start httpd
sudo systemctl enable httpd
cd /var/www/html
git clone https://github.com/Utkarshs2905/simple-website.git
sudo systemctl restart httpd

# Access webapp at -- http://PUBLIC-EC2-IP/simple-website

