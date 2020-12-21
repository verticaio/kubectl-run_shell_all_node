# kubeclt-run_shell_all_node, run shell commands kubernetes nodes over kubectl plugin options

```
➜  ~ export   KUBECONFIG=~/.kube/config
➜  ~ chmod kubectl-run_shell_all_node kubectl-run_shell_single_node
➜  ~ cp kubectl-run_shell_all_node kubectl-run_shell_single_node /usr/local/bin/

➜  ~ kubectl plugin list
The following compatible plugins are available:
/usr/local/bin/kubectl-cmd
/usr/local/bin/kubectl-run_shell_all_node
/usr/local/bin/kubectl-run_shell_single_node

➜  ~ kubectl get nodes
NAME       STATUS   ROLES    AGE    VERSION
master01   Ready    master   108d   v1.13.5
worker01   Ready    node     108d   v1.13.5
worker02   Ready    node     108d   v1.13.5

➜  ~ kubectl run_shell_all_node echo "Hello World"
executing command  on "master01"
Hello World

executing command  on "worker01"
Hello World

executing command  on "worker02"
Hello World

➜  ~ kubectl run_shell_all_node nc -zv localhost 22
executing command  on "master01"
Ncat: Version 7.50 ( https://nmap.org/ncat )
Ncat: Connected to 127.0.0.1:22.
Ncat: 0 bytes sent, 0 bytes received in 0.01 seconds.

executing command  on "worker01"
Ncat: Version 7.50 ( https://nmap.org/ncat )
Ncat: Connected to 127.0.0.1:22.
Ncat: 0 bytes sent, 0 bytes received in 0.02 seconds.

executing command  on "worker02"
Ncat: Version 7.50 ( https://nmap.org/ncat )
Ncat: Connected to 127.0.0.1:22.
Ncat: 0 bytes sent, 0 bytes received in 0.02 seconds.
```

### Resources
[youtube_tutorial](https://www.youtube.com/watch?v=PvWr_Au-934&feature=youtu.be)<br/>
[awesome-kubectl-plugins](https://github.com/ishantanu/awesome-kubectl-plugins)<br/>
[alexeiled_nsenter_docker](https://alexei-led.github.io/post/k8s_node_shell/)<br/>
[sample_example](https://www.bmc.com/blogs/kubernetes-how-to-write-kubectl-subcommands/)<br/>
