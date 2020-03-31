# activeWinServer2019
how to install and active windows server 2019
怎样安装和激活windows server 2019



1. windows server 2019 镜像文件在 MSDN i tell you https://msdn.itellyou.cn/?lang=zh-cn 下载。

2. 写盘工具用的是 ultraiso 。因为镜像文件大于4G，所以写出来的盘，占用只有1G。把U盘转换格式为 ntfs ，把U盘内的 sources 文件夹删掉。再从原版iso 镜像中复制 sources 文件夹到 U 盘。

3. 安装系统

4. KMS激活  用的是 沧水的 kms https://kms.cangshui.net/

激活失败，一度认为是秘钥有问题，后续又找到一个帖子，Windows基础排查之一 - 激活  https://yq.aliyun.com/articles/215241

摘要如下：

slmgr /skms重新设置KMS服务器。

slmgr /rilc重新安装许可证。

slmgr /upk后slmgr /ipk 重新安装产品密钥。

重启Software Protection服务。（此步未执行）

我的情况，一开始执行 kms 激活失败，过程中秘钥被删除，后续也一直失败。直到 “slmgr /rilc重新安装许可证。” 这一步，重装了许可证，再接下来就成功了。

后续安装的office 2013也是自动激活的。
