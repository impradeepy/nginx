# nginx
This guide explains how to expose a locally running application to a public network using Nginx as a reverse proxy with SSL offloading. This setup keeps local ports hidden from external access while securing traffic with SSL.

Prerequisites

	•	Nginx installed on your server.
	•	A domain name pointing to your server’s IP address.
	•	Certbot installed for obtaining a free SSL certificate from Let’s Encrypt.

Steps

1. Install Nginx

If Nginx isn’t installed, run:
sudo apt update
sudo apt install nginx
2. Obtain an SSL Certificate
sudo apt install certbot python3-certbot-nginx
sudo certbot --nginx -d yourdomain.com
3. Configure Nginx as a Reverse Proxy
sudo nano /etc/nginx/sites-available/yourdomain.com
4.Enable Nginx
sudo ln -s /etc/nginx/sites-available/yourdomain.com /etc/nginx/sites-enabled/
