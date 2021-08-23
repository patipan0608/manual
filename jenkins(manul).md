# คู่มือ jenkins automated
## ขั้นแรก (เพื่อทดสอบ)
### - สร้าง VMขึ้นมา2ตัวเพื่อเป็นเครื่อง jenkins และเครื่อง webserver
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
### - ติดตั้ง JAVA เวอร์ชั่น8ขึ้นไปเพื่อใช้ Jenkins
### - เช็คเวอร์ชั่นของ JAVA ด้วยคำสั่ง
~~~
java --version
~~~
### - จากนั้นติดตั้ง JAVA ถ้ายังไม่มี
~~~
sudo apt install openjdk-11-jre-headless
~~~
### - ติดตั้ง jenkins ด้วยชุดคำสั่งนี้
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
### - ทำการเปิดพอท8080 หรือที่ต้องการจะใช้
~~~
sudo ufw enable
~~~
~~~
sudo ufw allow 8080/tcp
~~~
### - รีโหลดไฟล์วอและเช็คสเตตัส
~~~
sudo ufw reload
~~~
~~~
sudo ufw status
~~~
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/setupjk3.5.jpg)
### - เข้าเว็บด้วยเลขipเครื่องตามด้วยพอท8080
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
### - ติดตั้ง angular เพื่อให้ Jenkins ใช้คำสั่งได้
~~~
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt-get install -y nodejs
~~~
~~~
sudo npm install npm@latest -g
~~~
~~~
sudo npm install -g @angular/cli
~~~
# เครื่องที่2 
### -ติดตั้งเป็นเครื่อง websever ด้วยวิธีดังนี้
### - ติดตั้ง angular
### - ติดตั้ง node js
~~~
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt-get install -y nodejs
~~~
### - อัพเดท npm เป็นเวอชั่นล่าสุด
~~~
sudo npm install npm@latest -g
~~~
### - ติดตั้ง angular CLI
~~~
sudo npm install -g @angular/cli
~~~
### - สร้าง workspace
~~~
ng new my-app
~~~
### - run
~~~
cd my-app
~~~
~~~
ng serve --open
~~~
### - ทำการเปิดพอท 4200 จากนั้นเข้าเช็คด้วย ip:4200
### - ติดตั้ง nginx
### - update apt และติดตั้ง nginx
~~~
sudo apt update
~~~
~~~
sudo apt install nginx
~~~
~~~
sudo ufw app list
~~~
### - เปิดช่องnginx HTTP
~~~
sudo ufw allow 'Nginx HTTP'
~~~
~~~
sudo ufw status
~~~
### - ทดสอบด้วยการใช้เลขipเครื่อง
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/nginx3.jpg)
### - คำสั่งเพิ่มเติมสำหรับ nginx
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
### - ด้วยชื่อ user@ip เครื่องปลายทาง
### - ทำให้เครื่อง Jenkins รู้จักกับเครื่อง websever 
### - ทำให้เครื่อง websever รู้จักกับ Jenkins
### - ต้องเข้าเครื่อง Jenkins แล้วเข้าที่ use Jenkins โดยเข้าไปเปลี่ยนรหัสของ user Jenkins 
~~~
sudo passwd jenkins
~~~
### - จากนั้นเข้าไปที่ user Jenkins แล้วทำการ gen key ไปที่เครื่อง web server
## การใช้งาน jenkins
### - เข้าไปที่เว็บ Jenkins ที่เข้าด้วยเลข ip และพอท 8080
### - สร้าง Freestyle project เพื่อทำการสร้างอึเค้าเชื่อมต่อ git hub หรืออื่นๆ
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/creeate.jpg)
### - จะมีการ setting เพิ่มเติมด้านใน
### - ตามขั้นตอนดังนี้
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/ac1.jpg)
### - สร้าง pipelineproject
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/creeate.jpg)
### - ชี้ URL ให้ jenkins รู้ว่าเราจะทำงานที่ project ไหนของแหล่งที่มา
### - ตั้งค่าให้ทำงานเมื่อมีการ push ขึ้น git hub หรืออื่นๆ (ตัวอย่างเป็น git hub)
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/setting%20pipe.jpg)
### - การตั้งค่าการทำงานของ pipeline นั้นจะมี syntax เฉพาะตัวอย่างดังนี้
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/pipelinecode.jpg)
### - stages ในนี้จะมีหลาย stage ย่อยได้
### - โดยใน stage ย่อยจะมี step
### - ตั้งการทำงานเพื่อให้ตรวจสอบได้ง่ายว่าผืดพลาดที่ส่วนไหน
### - โดยขั้นตอนเริ่มจากการ pull จาก github ในตัวอย่างเท่านั้นถ้่าใช้แบบอื่นสามารถเปลี่ยนได้
### - แล้วทำการ npm insatall
### - ทำการ build
### - แล้วส่งไปที่เครื่อง webserver จากนั้นย้ายไปที่โฟลเดอร์ปลายทาง
### -สร้าง web hook github 
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/webhook.jpg)
### - เพิ่ม web hook 
![Editor preferences pane](https://github.com/patipan0608/manul/blob/main/webhook1fix.jpg)
### - ในกรอบที่วงไว้ให้ใส่ ip เครื่อง web server ตามหลังด้วย “github-webhook/”
