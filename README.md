<div id="header" align="center">
  <img src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" width="100"/>
</div>
<div id="badges" align="center">
  <a href="https://www.linkedin.com/in/kevin-christianto/">
    <img src="https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
  </a>
</div>
<div id="github" align="center">
    <img src="https://komarev.com/ghpvc/?username=kevhoz&style=flat-square&color=blue" alt=""/>
</div>
<div id="body-header" align="center">
<h1>
  Simple XSS Scripting Testing
</h1>
</div>
### :hammer_and_wrench: Languages and Tools:
<div>
  <img src="https://github.com/devicons/devicon/blob/master/icons/php/php-original.svg" title="PHP"  alt="PHP" width="40" height="40"/>&nbsp;
</div>

### :woman_technologist: This repository cover:

1. Prepare The Environment.
2. Simple Case of XSS Scripting Testing

<div id="prepare-environment">
<h2>
  Prepare The Environment
</h2>

What we need is:

PHP & MYSQL
  - You can install PHP & MYSQL from Xampp (apachefriends.org)
  - We need that 2 to be active for this testing

Get Development Folder Ready:
- Create folder "xss-scripting" inside your root folder for web hosting (if xampp, then htdocs)
- Go inside the folder and create 2 file ("index.php" and "secure.php"), like this structure:
```
-xss-scripting
--index.php
--secure.php
```
- Open "index.php" and write this code:

  ![image](https://github.com/user-attachments/assets/9de90d2d-a370-4b6d-9066-a837f9f016a0)

- Open "secure.php" and write this code:

  ![image](https://github.com/user-attachments/assets/f8c1250d-38a8-455f-bde5-d16e0249bd0b)

- Next, open PhpMyAdmin to create database, here is the step:
  1. Create database "testdb"
  2. Create table "comments"
  3. Create field:
     - id INT AUTO_INCREMENT PRIMARY KEY
     - content TEXT NOT NULL
  4. No need to input data
- Or, you can write this code in SQL script:

  ![image](https://github.com/user-attachments/assets/4fdea873-6f18-4dd4-89db-6fa5075e6c7d)

</div>

<div id="xss-scripting">
<h2>
  Use case comments: XSS Scripting
</h2>

- Lets play the XSS Scripting case:

- Not safe code:
- Open your php code on: "localhost/xss-scripting", it will shown like this:

![image](https://github.com/user-attachments/assets/2d9e5531-d1dd-402e-878c-3e890f002d94)

- Test for copmment success:
  1. Input any comment into field komentar
  2. click kirim!
  3. it will shown comment success

![image](https://github.com/user-attachments/assets/0232d2e5-0450-4daa-b443-9dc0fe5f5746)

- Test for XSS Scripting:
  1. Input this value into field komentar:
  ```
  <script>alert('XSS Attack!');</script>
  ```
  3. click kirim!
  4. see the result

- Test the SQL Injection into the secure (localhost/xss-scripting/secure.php)
  1. Input this value into field komentar:
  ```
  <script>alert('XSS Attack!');</script>
  ```
  3. click kirim!
  4. see the result

- Compare it, and why it secure.
- XSS Scripting case, Done

</div>
