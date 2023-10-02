growpart (to extend partition on linux)

guid: <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/recognize-expanded-volume-linux.html>
trouble shoot: <https://unix.stackexchange.com/questions/687485/ubuntu-ext4-partition-is-not-being-extended-or-resized-as-expected-with-growpart>

1.1.2: <https://mega.nz/file/IcQiVDCR#NdO3exgJXnMW2Fih0l1gLxpi7WXGXx6Sow1OWrEe3gk>

https://mega.nz/file/IU53TCKC#3SvPYKB3JVQ-tQX9kKGh7ljhYdoEldC4suhalC60yo4

beta <https://mega.nz/file/4QoV2abD#8sVYVDU7laBjBjYOVXm0ONNhQZxxN8X3RzdvK7Vt-ko>

```sh
dism /online /set-edition:Windows 10 Pro /productkey:W269N-WFGWX-YVC9B-4J6C9-T83GX /accepteula
```

or

```sh
slmgr /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX
```

<https://learn.microsoft.com/en-us/windows-server/get-started/kms-client-activation-keys>

### Cloudbase-init config

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
san_policy=OnlineAll
metadata_services=cloudbaseinit.metadata.services.configdrive.ConfigDriveService,cloudbaseinit.metadata.services.ec2service.EC2Service,cloudbaseinit.metadata.services.httpservice.HttpService,cloudbaseinit.metadata.services.maasservice.MaaSHttpService
metadata_base_url=http://169.254.169.254/
retry_count=2
retry_count_interval=5

plugins=cloudbaseinit.plugins.windows.extendvolumes.ExtendVolumesPlugin,
         cloudbaseinit.plugins.common.networkconfig.NetworkConfigPlugin,
         cloudbaseinit.plugins.common.sethostname.SetHostNamePlugin,
         cloudbaseinit.plugins.common.setuserpassword.SetUserPasswordPlugin,
         cloudbaseinit.plugins.common.localscripts.LocalScriptsPlugin,
         cloudbaseinit.plugins.common.userdata.UserDataPlugin

verbose=true
debug=true
log_dir=C:\Program Files\Cloudbase Solutions\Cloudbase-Init\log\
log_file=cloudbase-init.log
default_log_levels=comtypes=INFO,suds=INFO,iso8601=WARN,requests=WARN
logging_serial_port_settings=COM1,115200,N,8
mtu_use_dhcp_config=true
ntp_use_dhcp_config=true
local_scripts_path=C:\Program Files\Cloudbase Solutions\Cloudbase-Init\LocalScripts\
C:\powershell
PS C:\Set-ExecutionPolicy Unrestricted
PS C:\net user administrator /active:yes
volumes_to_extend=1,2
[openstack]
add_metadata_private_ip_route=False
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

