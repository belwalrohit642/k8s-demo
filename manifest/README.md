Communication Flow:
External requests are made to Nginx through the assigned NodePort.
Nginx, running in its container, receives the requests.
Nginx forwards the requests to either App1 or App2 based on the defined upstream configuration in the nginx.conf file.
The requests reach the respective App1 or App2 service, which load-balances the traffic among the available pods.
Finally, the requests are directed to the running pods of App1 or App2, where the Node.js applications are serving on port 3000.
