# Linux-DNF-YUM-Repository-Server-Configuration
Configured and managed a Linux DNF/YUM repository server to provide software package installation, update, and removal services for client systems in a virtual machine environment.


ON Server Machine  
How to configure DNF/YUM Server in RHEL - 
To mount RHEL DVD inside your Linux server use the mount command.
[root@skynetlinux ~]# mount /dev/sr0 /mnt  
[root@skynetlinux ~]# mkdir -p /var/www/html/rhel           [to create directory]  
[root@skynetlinux ~]# cd /mnt                                   [go to /mnt directory]  
[root@skynetlinux mnt]# cp –Rv  BaseOS  AppStream /var/www/html/rhel  [copy all file/folder] 
[root@skynetlinux mnt]# cd      
[root@skynetlinux ~]# vim /etc/yum.repos.d/rhel.repo                  [Edit rhel.repo file] 

![image alt](https://github.com/Sidh1911/Linux-DNF-YUM-Repository-Server-Configuration/blob/b92152bd85be58c0a7947f029b8550a7d1b6c997/Screenshot%202026-05-23%20171634.png)

Client Site: -  
 # vim /etc/yum.repos.d/rhel.repo              [to create repo file]  
  (Add the following line) 

  ![image alt](https://github.com/Sidh1911/Linux-DNF-YUM-Repository-Server-Configuration/blob/8716ae4e697a93a17b68a598bb95d51312687e32/Screenshot%202026-05-23%20171808.png)

  ESC: wq  
 # dnf clean all  
 # dnf repolist  all  -v                    [to check status]  
 
 *** How to install/remove/update Package via yum Server ***  
  
  # dnf install vsftpd                (to install pkg)  
  # dnf remove vsftpd                (to uninstall pkg)  
  # dnf update vsftpd                 (to update pkg)  
  # dnf search vsftpd                                        (to search pkg)  
  # dnf list vsftpd                   (to show pkg install of not)  
  # dnf history                       (to show history)  


  install 

  ![image alt](https://github.com/Sidh1911/Linux-DNF-YUM-Repository-Server-Configuration/blob/7812c8ddc137d17ae91d142a480029ca801d7ed3/6093565678649544607.jpg)

  update

    ![image alt]()

