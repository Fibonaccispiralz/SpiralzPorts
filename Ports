#!/bin/bash 

echo "Please enter the IP address you'd like to scan:"
read ip

echo "Please enter the port range you'd like to scan (e.g. 1-1000):"
read port 

echo "Scanning $ip:$port"

for port in $(seq $port); do
    (timeout 1 bash -c "echo >/dev/tcp/$ip/$port") &>/dev/null && echo "$port open"
done
