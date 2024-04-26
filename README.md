# 自动挂载硬盘
```bash
sudo fdisk -l
sudo mkdir /mnt/sdb
sudo mount /dev/sdb1 /mnt/sdb

# 自动挂载
sudo nano /etc/fstab
  # 在文件末尾添加一行
  /dev/sdb1 /mnt/sdb ext4 defaults 0 0
```

# 禁用桌面，节省功耗
```bash
sudo systemctl stop gdm
sudo systemctl disable gdm

# 启用桌面
sudo systemctl enable gdm

# 如有必要，卸载与安装桌面
sudo apt purge ubuntu-gnome-desktop gnome-shell gnome-session
sudo apt install ubuntu-gnome-desktop gnome-shell gnome-session
```
