# Mikrotik-install

mkdir -p /opt/unetlab/addons/qemu/mikrotik-7.15.3

cd /opt/unetlab/addons/qemu/mikrotik-7.15.3

wget https://download.mikrotik.com/routeros/7.15.3/chr-7.15.3.vmdk.zip

unzip chr-7.15.3.vmdk.zip

/opt/qemu/bin/qemu-img convert -f vmdk -O qcow2 chr-7.15.3.vmdk hda.qcow2

/opt/unetlab/wrappers/unl_wrapper -a fixpermissions

rm -rf chr-7.15.3.vmdk
rm -rf chr-7.15.3.vmdk.zip
