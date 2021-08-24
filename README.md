# คู่มือ Jenkins automated
## ในการทดลองนี้ได้ทำการสร้าง ubuntu vm ขึ้นมา2เครื่อง ให้เครื่อง 1. เป็น Jenkins ip192.268.23.129 2. เป็น web server 192.168.23.130 ติดตั้ง Node.js และอัพเดท npm ในทั้ง2เครื่องเพื่อให้ทำงานร่วมกันได้ จากนั้นทำให้ Jenkins เข้าถึง project บน github ได้ต้องทำการชี้ url และผูก user ก่อนจึงจะทำงานร่วมกันได้ดังวิธีในคู่มือ จากนั้นเมื่อมีการ push code new version ขึ้นไปที่ project การทำงานจะเริ่มต้น Jenkins จะทำการ -pull -build -sent to production sussecc
## ขั้นแรก (เพื่อทดสอบ)
### - สร้าง VM ขึ้นมา2ตัวเพื่อเป็นเครื่อง jenkins และเครื่อง web server
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%AA%E0%B8%A3%E0%B9%89%E0%B8%B2%E0%B8%87vm.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B21.jpg) 
# 
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B22.jpg)
# 
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B23.jpg)
# 
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B24.jpg)
#
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B25.jpg)
#
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B26.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B27.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B28.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B29.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B210.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B211.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B212.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B213.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B214.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/%E0%B8%81%E0%B8%B3%E0%B8%AB%E0%B8%99%E0%B8%94%E0%B8%84%E0%B9%88%E0%B8%B215.jpg)
# เครื่องที่ 1
### - ติดตั้งเป็นเครื่อง Jenkins ด้วยวิธีต่อไปนี้
### - ติดตั้ง JAVA เวอร์ชัน 8 ขึ้นไปเพื่อใช้ Jenkins
### - ตรวจสอบเวอร์ชันของ JAVA ด้วยคำสั่ง
~~~
java --version
~~~
### - จากนั้นติดตั้ง JAVA ถ้ายังไม่มี
~~~
sudo apt install openjdk-11-jre-headless
~~~
### - ติดตั้ง Jenkins ด้วยชุดคำสั่งนี้
~~~
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
~~~
~~~
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
~~~
~~~
sudo apt update
~~~
~~~
sudo apt install jenkins
~~~
~~~
sudo systemctl status jenkins
~~~
~~~
sudo systemctl start jenkins
~~~
### - ทำการเปิดพอท 8080 หรือที่ต้องการจะใช้
~~~
sudo ufw enable
~~~
~~~
sudo ufw allow 8080/tcp
~~~
### - รีโหลดไฟร์วอล์ลและเช็คสเตตัส
~~~
sudo ufw reload
~~~
~~~
sudo ufw status
~~~
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/setupjk3.5.jpg)
### - เข้าเว็บด้วยเลข IP เครื่องตามด้วยพอท8080
### - จากนั้น jenkins จะถาม password
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/setupjk4.jpg)
### - ดูได้จากคำสั่งนี้
~~~
cat /var/lib/jenkins/secrets/initialAdminPassword
~~~
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/setupjk4.2.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/setupjk4.3.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/setupjk4.4.jpg)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/setupjk4.5.jpg)
### - ติดตั้ง Node.js และอัพเดท npm เพื่อให้ Jenkins ใช้คำสั่งได้
~~~
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt-get install -y nodejs
~~~
~~~
sudo npm install npm@latest -g
~~~
# เครื่องที่2 
### -ติดตั้งเป็นเครื่อง web sever ด้วยวิธีดังนี้
### - ติดตั้ง Node.js
~~~
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt-get install -y nodejs
~~~
### - อัพเดท npm เป็นเวอชั่นล่าสุด
~~~
sudo npm install npm@latest -g
~~~
### - ติดตั้ง NginX
### - update apt และติดตั้ง NginX
~~~
sudo apt update
~~~
~~~
sudo apt install nginx
~~~
~~~
sudo ufw app list
~~~
### - เปิดช่อง NginX HTTP
~~~
sudo ufw allow 'Nginx HTTP'
~~~
~~~
sudo ufw status
~~~
### - ทดสอบด้วยการใช้เลข IP เครื่อง
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/nginx3.jpg)
### - คำสั่งเพิ่มเติมสำหรับ NginX
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/nginxscip.jpg)
### - ต้องทำการ gen keygen เพื่อให้เครื่องแต่ละเครื่องรู้จักกันโดยไม่ถาม password
~~~
ssh-keygen
~~~
~~~
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
~~~
~~~
ssh-copy-id <username>@<ip>
~~~
### - ด้วยชื่อ user@IP เครื่องปลายทาง
### - ทำให้เครื่อง Jenkins รู้จักกับเครื่อง web sever 
### - ทำให้เครื่อง web sever รู้จักกับ Jenkins
### - ต้องเข้าเครื่อง Jenkins แล้วเข้าที่ use Jenkins โดยเข้าไปเปลี่ยนรหัสของ user Jenkins 
~~~
sudo passwd jenkins
~~~
### - จากนั้นเข้าไปที่ user Jenkins แล้วทำการ gen key ไปที่เครื่อง web server
## การใช้งาน jenkins
### - เข้าไปที่เว็บ Jenkins ที่เข้าด้วยเลข IP และพอท 8080
### - สร้าง Freestyle project เพื่อทำการสร้าง Account เชื่อมต่อ GitHub หรืออื่นๆ
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/creeate.jpg)
### - จะมีการ setting เพิ่มเติมด้านใน
### - ตามขั้นตอนดังนี้
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/ac1.jpg)
### - จะได้ Account ที่ใช้เชื่อต่อกับ GitHub โดยในตัวอย่างตั้งชื่อไว้ว่า ’GitHubAccount3’
### 
### - สร้าง Pipeline project
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/creeate.jpg)
### - ชี้ URL ให้ jenkins รู้ว่าเราจะทำงานที่ project ไหนของแหล่งที่มา
### - ตั้งค่าให้ทำงานเมื่อมีการ push ขึ้น git hub หรืออื่นๆ (ตัวอย่างเป็น GitHub)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/setting%20pipe.jpg)
### - การตั้งค่าการทำงานของ pipeline นั้นจะมี syntax เฉพาะตัวอย่างดังนี้
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/pipelinecode.jpg)
### - stages ในนี้จะมีหลาย stage ย่อยได้
### - โดยใน stage ย่อยจะมี step
### - ตั้งการทำงานเพื่อให้ตรวจสอบได้ง่ายว่าผิดพลาดที่ส่วนไหน
### - โดยขั้นตอนเริ่มจากการ pull จาก GitHub ในตัวอย่างเท่านั้นถ้าใช้แบบอื่นสามารถเปลี่ยนได้
### - แล้วทำการ npm install
### - ทำการ build
### - แล้วส่งไปที่เครื่อง web server จากนั้นย้ายไปที่โฟลเดอร์ปลายทาง
### -สร้าง webhook GitHub
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/webhook.jpg)
### - เพิ่ม webhook 
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/webhook1fix.jpg)
### - ในกรอบที่วงไว้ให้ใส่ IP เครื่อง web server ตามหลังด้วย “github-webhook/”
## คู่มือการใช้ Jenkins นี้ทำขึ้นเนื่องจากเห็นได้ว่าการ deploy แบบปกตินั้นเปลืองเวลาและยุ่งยากจึงศึกษาการใช้ Jenkins เพื่อทำ automated deploy สำหรับใช้ในงานต่างๆโดยการศึกษา Jenkins ในครั้งนี้จะเป็นการนำ jenkins มาทดลองทำ automated deploy จากเครื่อง Jenkins ไปเครื่อง web server โดยใช้การ push ผ่าน gitlab แล้วตั้งทริกเกอร์ให้ Jenkins นั้นเริ่มทำการไป pull จาก gitlab เมื่อมีการ push หลังจาก Jenkins ทำการ pull ลงมาจะทำการ build แล้วส่งไปยัง part ปลายทางที่อยู่ที่เครื่อง web server 
