https://mega.nz/file/IU53TCKC#3SvPYKB3JVQ-tQX9kKGh7ljhYdoEldC4suhalC60yo4

```sh
dism /online /set-edition:Windows 10 Pro /productkey:W269N-WFGWX-YVC9B-4J6C9-T83GX /accepteula
```

or

```sh
slmgr /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX
```

<https://learn.microsoft.com/en-us/windows-server/get-started/kms-client-activation-keys>

```sh
[DEFAULT]
username=Administrators
groups=Administrators
inject_user_password=true
first_logon_behaviour=no
config_drive_raw_hhd=true
config_drive_cdrom=true
config_drive_vfat=true
bsdtar_path=C:\Program Files\Cloudbase Solutions\Cloudbase-Init\bin\bsdtar.exe
mtools_path=C:\Program Files\Cloudbase Solutions\Cloudbase-Init\bin\
verbose=true
debug=true
logdir=C:\Program Files\Cloudbase Solutions\Cloudbase-Init\log\
logfile=cloudbase-init.log
default_log_levels=comtypes=INFO,suds=INFO,iso8601=WARN,requests=WARN
logging_serial_port_settings=COM1,115200,N,8
mtu_use_dhcp_config=true
ntp_use_dhcp_config=true
local_scripts_path=C:\Program Files\Cloudbase Solutions\Cloudbase-Init\LocalScripts\
C:\powershell
C:\Set-ExecutionPolicy Unrestricted

```



# Git-L
# 1.tạo ssh key: sử dụng ssh-keygen (tạo auto) hoặc ssh-keygen -t tên_key_private -f tên_key_pubblic
# 2.thêm shh key vào tài khoản github
# 3.clone 1 repo: chọn ssh rồi copy link
#                 mở Comman Line chọn 1 file bất kỳ, sử dụng lệnh git clone link_repo
# 4. sử dụng lệnh git remote -v để xem tên các remote, mở file config trong tệp .git để xem các branch-merge
# 5. dùng git status để kiểm tra trạng thái các file trong floder nếu xanh là có thể push ngay, nếu đỏ thì cần commit
# 6. dùng git add . để tiến hành push tất cả lên git hoặc git add tên_file để add file xác định
# 7. để commit dùng lệnh git commit - m "nội dung của commit"
# 8. push file lên git dùng git push tên_remote tên_branch

