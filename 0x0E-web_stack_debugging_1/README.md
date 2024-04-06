This is 0x0E.Web stack debugging #1.
i have learned about the following;
1.check Nginx configuration.
First, ensure that Nginx is configured to listen on port 80. The default Nginx configuration file is located at /etc/nginx/nginx.conf or /etc/nginx/sites-available/default for site-specific configurations. and for my case am going to use;
"cat /etct/nginx/nginx.conf | grep listen
2.check if UFW(uncomplicated firewall) is enabled:
by using;
"sudo ufw status"
3.Allow traffic on port 80;
-If UFW is enabled and blocking port 80, allow traffic
"sudo ufw allow 80"
step 3:Ensure Ngix is running 
-Make sure Nginx is running and listening on port 80.
1.Check if Nginx is running;
"sudo systemctl status nginx"
2.Restart Nginx to apply any configuration changes:
"sudo systemctl restart nginx"
step 4: Automate the Fix with a Bash Script
