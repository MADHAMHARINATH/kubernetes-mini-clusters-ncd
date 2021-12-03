<!-- Headings -->
<!-- Italics -->
<!--Blockquote -->
# To setup K3S cluster with 2Nodes
## Step-1 : Prerequisites
* Two ubuntu servers
## Step-2 : Install k3s using below command on VM1 & Copy the accesskey token and copy ip of this server.
```
curl -sfL https://get.k3s.io | sh - && cat /var/lib/rancher/k3s/server/node-token
```
## Step-3 : Login to another VM2 manually and excute below command paste the accesskey (key) and server ip (myserver).
```
curl -sfL https://get.k3s.io | K3S_URL=https://<myserver>:6443 K3S_TOKEN=<key> sh -
```
## Step-4 : To see list of nodes
```
sudo k3s kubectl get nodes
```
