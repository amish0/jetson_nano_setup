# jetson_nano_setup
Jetson_nano_setup


# Increase swap Memory
check the current swap memory
https://www.youtube.com/watch?v=uvU8AXY1170&list=PL5B692fm6--uQRRDTPsJDp4o0xbzkoyf8&index=15
(11:12 to 14:00)

```bash
free -h

free -m
```

```bash
sudo systemctl disable nvzramconfig
sudo fallocate -l 4G /mnt/4GB.swap
sudo chmod 600 /mnt/4GB.swap
sudo mkswap /mnt/4GB.swap
echo '/mnt/4GB.swap swap swap defaults 0 0' | sudo tee -a /etc/fstab
sudo reboot
```

```bash
free -m
```
# Youtube video link
https://www.youtube.com/watch?v=uvU8AXY1170&list=PL5B692fm6--uQRRDTPsJDp4o0xbzkoyf8&index=15
