# Copy theme to the theme directory
sudo cp -R simple-image-manjaro /usr/share/plymouth/themes/

# Set correct ownership to the 'arch-glow' theme files:
sudo chown -R root.root /usr/share/plymouth/themes/simple-image-manjaro

# Set the 'arch-glow' theme as default, editing the following file *
sudo vim /etc/plymouth/plymouthd.conf
-------------------------------
[Daemon]
   Theme=simple-image-manjaro
   ShowDelay=5

# Open a terminal and execute
sudo plymouth-set-default-theme -R simple-image-manjaro
