### Script: kubplugin

The [kubeplugin](https://raw.githubusercontent.com/redman-dev29/ascii-artify/main/scripts/kubeplugin) - a Bash script that can display information about the use of system resources.

#### How to use?

1. Download plugin:
`wget -O /tmp/kubeplugin https://raw.githubusercontent.com/redman-dev29/ascii-artify/main/scripts/kubeplugin`
2. Use:
`bash /tmp/kubeplugin {pods, nodes, deployments} <namespace>`

#### Output

The script will output the resource usage statistics in the following format:

Resource, Namespace, Name, CPU, Memory