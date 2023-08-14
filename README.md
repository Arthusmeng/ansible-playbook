# ansible-playbook
Devops-ansible-playbook

- [Versions](#versions)
- [Configure \& connect](#configure--connect)
    - [host](#host)
    - [docker playbook](#docker-playbook)
    - [sysctl playbook](#sysctl-playbook)

# versions
ansible [ 2.15.1]

# Configure & connect
### host
`0.0.0.0  ansible_host=0.0.0.0 ansible_ssh_port=22 ansible_ssh_pass="Password" ansible_ssh_private_key_file=/root/key `

0.0.0.0 修改自己的主机ip/或者出口ip
ansible_host = 目标主机
ansible_ssh_port = 目标主机端口
ansible_ssh_pass = 目标主机密码
ansible_ssh_private_key_file = 选填写私钥地址

### docker playbook
`ansible-playbook -e "example-dev"  playbooks/install-docker-ubuntu.yaml -vvvv `

### sysctl playbook
`ansible-playbook -tags=tags名称1,tags名称2...  yaml文件名称`

执行时候任务中加入-t 执行tag参数即可

example:
`ansible-playbook -e "example-dev" -t=8G playbooks/sysctl.yaml -vvvv `

### 参数
`-v 参数显示输出 -vvvv 最多4个v`


