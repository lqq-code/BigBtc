## 合成简宝

### 本地启动

1. 安装 serve 工具：

   ```bash
   npm i -g serve
   ```

2. 进入 daxigua 目录，运行 serve：

   ```bash
   serve
   ```

3. 打开浏览器访问 localhost:5000 即可！

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210204113347600.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjIyNDA1NQ==,size_16,color_FFFFFF,t_70#pic_center)

### 快速魔改

> 按照下列说明修改即可，持续补充

1. 改分数：改 extraSettings.js 文件

2. 改图片：替换 res/raw-assets 目录下指定目录的图片，必须同文件名、后缀、尺寸，成功覆盖可生效，[可替换素材文档](https://docs.qq.com/sheet/DS0d2VVVJYmpvZ0pZ)

3. 无敌模式：改 extraSettings.js 文件

4. 指定第一个水果：改 extraSettings.js 文件

5. 指定下次出现的水果：改 extraSettings.js 文件

6. 大水果合成小水果：在 project.js 代码中搜索 "大水果合成小水果"

7. 让水果更 Q 弹：改 extraSettings.js 文件，[原理参考](https://docs.cocos.com/creator/api/zh/classes/PhysicsCircleCollider.html?h=circlecollider)

8. 水果下落速度减缓：改 extraSettings.js 文件，[原理参考](https://docs.cocos.com/creator/manual/zh/physics/physics/rigid-body.html?h=%E5%88%9A%E4%BD%93)

9. 替换音乐：，覆盖 res/raw-assets 目录下相同的音乐，[可替换素材文档](https://docs.qq.com/sheet/DS0d2VVVJYmpvZ0pZ)

10. 替换背景：和改图片原理相同，[可替换素材文档](https://docs.qq.com/sheet/DS0d2VVVJYmpvZ0pZ)

11. 去广告：将广告图片替换为[同背景色底图](https://636f-codenav-8grj8px727565176-1256524210.tcb.qcloud.la/0.png)

12. 替换广告链接：改 extraSettings.js 文件

13. 改网站标题：改 extraSettings.js 文件

14. 开启选分弹窗：改 extraSettings.js 文件

### 魔改原理

请先阅读：[魔改和上线你的合成简宝，最全教程！](https://mp.weixin.qq.com/s/H9VR1MWn-9bKSC_1l_MkJw)

我给 `project.js` 文件补充了注释，大家可以搜索关键字，如 "改分" 来快速定位，学习修改原理。

### 问题及解决

1. 无法安装 serve 或者 Vercel？

   答：如果报找不到 npm，请先安装 npm。

   如果安装中卡住，试着按下键盘（可能假死），还不行的话先用 npm 安装 cnpm（国内镜像，比较快）：

   ```bash
   npm install cnpm -g --registry=https://registry.npm.taobao.org
   ```

   再用 cnpm 安装： `cnpm i -g serve` 或 `cnpm i -g vercel`

2. Vercel 网址被微信拦截怎么办？

   答：可以把网址复制到浏览器打开，也可以申请一个域名，在 Vercel 和服务提供商配置域名解析。
   Vercel 基本是海外的服务器，无需备案。

3. 怎么在电脑上浏览网页游戏？

   答：在浏览器中，按 F12 打开开发者工具，点击像手机一样的图标即可。

4. 为什么 serve 后，打开网页一片空白？

   答：大概率是你在错误的目录下执行了 serve，请务必在 index.html 所在的文件夹下执行 serve。

5. 执行 vercel 命令显示 signUp？

   答：要先去 [Vercel 官网](https://vercel.com/) 注册。

6. vercel 邮箱验证失败？

   答：先确认邮箱是否正确，如果验证失败，大概率是网络原因，请尝试 4G 等网络。

7. 怎么使用 vercel 同时上线多个版本？

   答：在输入 vercel 后，选择不和已有项目关联（link），并且使用一个新的项目名（project name）。
