
# Command for disk check
lsblk

# Create temporary Folder for original disk
sudo mkdir /mnt/tempvol

# Mount original disk to temporary disk
sudo mount /dev/xvdf1 /mnt/tempvol

# Copy new key pair to original disk ssh folder 
# Change [ubuntu] parameter with [ec2-user] if you created amazon linux
sudo cp .ssh/authorized_keys /mnt/tempvol/home/ubuntu/.ssh/authorized_keys

# Unmount original disk
sudo umount /mnt/tempvol
