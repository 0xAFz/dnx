# DNX

Smart DNS Proxy

## Deployment
1. Clone the repo
```bash
git clone https://github.com/0xAFz/dnx.git
```
2. Install latest nginx from the official repository [docs.nginx.com](https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-open-source/)
3. Install dnsmasq
```bash
apt update
apt install dnsmasq -y
```
4. Edit the `dnsmasq.conf` and replace the `<SERVER_PUBLIC_IP>` with your server IP
```bash
vim dnsmasq.conf
```
5. Replace the config files
```bash
cp ./nginx.conf /etc/nginx/nginx.conf
cp ./dnsmasq.conf /etc/dnsmasq.conf
```
6. Restart the services
```bash
systemctl restart nginx
systemctl restart dnsmasq
```