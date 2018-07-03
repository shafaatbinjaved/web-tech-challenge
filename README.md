Welcome to the Orderbird Tech Challenge :-). Thank you for considering joining our team. As for the tech challenge: we like you to setup and develop the following super small website.

# The Goal: get leads from potential customers
We need a web page where potential new orderbird customers can leave their name, email and telephone number, this data will then be stored in a data base to get in touch with them later.
Also we need a simple admin page which is only accessible via a username and password. 

The Website should be based on the PHP framework Laravel and LESS. To get things a little easier we have created a vagrant file to create a virtual machine (Ubuntu, PHP, MySQL and an Apache). You just need to add Laravel and LESS. 

# Where should I put the code?
Your code should be in a publicly accessible repository. Besides the application please include a README file containing at least a guide on how to run the website.

# Some guidelines:
- make it beautiful :-) but don't create too much content, as it is more important to us how you used your skills "under the hood"
- Responsive design? Yes, please!
- If possible, please write tests and validate your inputs (yes, seriously, it is important to us)
- Showcase your abilities, and use the task to demonstrate your idea of best practices, regarding coding style, project
 structure, frameworks, patterns, design, etc.
- There is no right or wrong solution, as long as it is your solution.
- If you only have time to do one thing please do it as good as you possible can. It is better to have an nice but incomplete solution rather than a mediocre "feature complete" one. We want to get a good impression of your abilities.
- Be prepared to describe your work in detail.

# How long should this take?
We know, doing some homework is rarely fun. So please try to keep it as short as possible. Two to three hours should get you to the point where you can demo it. If possible you can also


# Notes
- Vagrant runs an Ubuntu machine on 192.168.33.61 (change the IP if you've got already something going on there in the Vagrant file)
- The project on the Ubuntu machine is located in /vagrant 
- MySqL User and Password are "root"
- Maybe you have to GRANT ALL Priviliges to root
- To enable mysql access from outside the vm you have to edit the /etc/mysql/mysql.conf.d/mysqld.cnf by commenting "bind adress" and "skip-external-locking" out and restart the mysql service.
You can connect then by host 192.168.33.61 root / root

#Tasks to get the laravel installation running
- run vagrant up
- Create a database named orderbird
- Run composer install (you've got sudo inside the machine)
- Save the .env.example to .env

#Some hints
- You can make a quite simple auth for the admin panel by php artisan make:auth
- Laravel comes with "mix" for frontend building - but use what you want for this
