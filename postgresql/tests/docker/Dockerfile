FROM centos:7

RUN yum -y install openssh-server && \
    systemctl enable sshd.service && \
    sed -ri 's/^#PermitRootLogin yes/PermitRootLogin yes/' /etc/ssh/sshd_config && \
    echo 'root:password' | chpasswd && \
    ssh-keygen -t rsa -N "" -f /etc/ssh/ssh_host_rsa_key

EXPOSE 22

CMD ["/usr/sbin/init"]
