# generate_204

This project provides a simple way to test your network latency, similar to `www.google.com/generate_204`.

## Steps

1. **Clone the repository**

   First, clone the repository to your remote server:

   ```bash
   git clone https://github.com/yonomesh/generate_204.git
   ```

2. **Modify Nginx Configuration**

   Edit the `nginx.conf` file to set your server's IP:

   ```nginx
   # 36 line
   # server_name your_server_ip;
   # For example:
   server_name 1.1.1.1;
   ```

3. **Modify Port (optional)**

   By default, the app listens on port 80. If you want to change the port, modify it in the compose.yaml.

4. **Run the Docker Compose**

   Once you've made the necessary changes, run the application:

   ```bash
   docker compose up
   ```

## Usage 
```
curl -i http://ip:port/generate_204

HTTP/1.1 204 No Content
Server: nginx/1.29.2
Date: Fri, 17 Oct 2025 08:03:56 GMT
Connection: keep-alive
Content-Type: text/plain
```