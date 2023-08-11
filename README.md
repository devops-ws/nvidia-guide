# nvidia-guide

## 安装包
```shell
# 指定 Linux 内核
./NVIDIA-Linux-x86_64-535.86.05.run --kernel-source-path=/usr/src/kernels/5.4.251-1.el7.elrepo.x86_64/ -k $(uname -r)
```

## FAQ
* group 112 is not viable\nPlease ensure all devices within the iommu_group are bound to their vfio bus driver
  * 如果一个设备有多个子设备，那么需要全部挂载到 KVM （或 KubeVirt）中

## 参考资料
* https://blog.csdn.net/zzh516451964zzh/article/details/125792421
* https://www.cnblogs.com/gollong/p/12655424.html
* [更换 Linux Kernel](https://www.cnblogs.com/mstmdev/p/17179398.html)
* https://github.com/NVIDIA/kubevirt-gpu-device-plugin
