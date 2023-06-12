FROM linuxserver/rsnapshot:1.4.5
RUN ssh-keygen -A &&\
    echo "root:secretpassword" | chpasswd &&\
    passwd -u root
