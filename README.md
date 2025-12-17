# CKA_Alias


# Paste this directly into the shell
    alias k="kubectl"
    alias kp="kubectl get pods -o wide"
    alias kd="kubectl get deployment -o wide"
    alias ks="kubectl get svc -o wide"
    alias kc="kubectl config get-contexts"
    source <(kubectl completion bash)
    complete -o default -F __start_kubectl k

# system ctl commands:
    systemctl stop kubelet
    systemctl start kubelet
    systmectl restart kubelet
    systemctl daemon-reload

to change the dns config we have to do change in kubeapiserver.yaml, 


the kube-proxy Pod in the kube-system namespace is erroring or in a CrashLoopBackOff, then running the command 
    kubeadm init phase addon all 

will be a quick way to solve your problem