# kube-plugin
kubectl plugin with bash  
add permissions
````
chmod +x my-top-plugin
````
Copy plugin to /usr/local/bin
```
sudo mv my-top-plugin /usr/local/bin/kubectl-mytopplugin
```
usage  
kubectl mytopplugin pod/node  
For pod option default namespace is kube-system. You can choose another namespace, if you want
```
kubectl mytopplugin pod
```
example output
```
Name                                               | CPU        | Memory               | Namespace 
-----------------------------------------------------------------------------------------------
NAME                                               | CPU(cores) | MEMORY(bytes)        | kube-system
coredns-6799fbcd5-jd8tk                            | 5m         | 13Mi                 | kube-system
local-path-provisioner-6c86858495-p9p6r            | 1m         | 7Mi                  | kube-system
metrics-server-54fd9b65b-gfvjr                     | 8m         | 23Mi                 | kube-system
svclb-traefik-83caa5fe-cvc6t                       | 0m         | 0Mi                  | kube-system
svclb-traefik-83caa5fe-frkgl                       | 0m         | 0Mi                  | kube-system
svclb-traefik-83caa5fe-xz7th                       | 0m         | 0Mi                  | kube-system
traefik-f4564c4f4-2bx42                            | 1m         | 30Mi                 | kube-system
```

and for node
```
kubectl mytopplugin node
```
example ouput
```
Name                                               | CPU        | Memory               | Namespace 
-----------------------------------------------------------------------------------------------
NAME                                               | CPU(cores) | CPU%                 | kube-system
k3d-demo-cluster-agent-0                           | 92m        | 1%                   | kube-system
k3d-demo-cluster-agent-1                           | 82m        | 1%                   | kube-system
k3d-demo-cluster-server-0                          | 109m       | 1%                   | kube-system
```