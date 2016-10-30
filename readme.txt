1、修改名字和邮箱
   -- 输入 git config --global --edit(图 1.PNG)
   --进入编辑器（图 2.PNG），按'i'之后就可以编辑了，修改完成后，     按‘Esc’‘：’，光标会进入到下方（图 3.PNG），输入‘wq’退出（     图 4.PNG）
   --回到原先界面


2、常用命令
   --git init       // 创建版本库（5.PNG）
   --git status     //查看仓库当前状态（6.PNG），英文你应该看的懂
                    //一般我提交一次就看一下，看你喜好
   --git add xxx    //将未追踪的文件添加到仓库（7.PNG）
   --git commit xxx -m 'xxx' //把文件提交到仓库（8.PNG），引号里的是                               //注释，忘加这参数会进入编辑器，编辑、退                             //出方法 和（1）中一样
   --git push       //有点迷，解释不来，就是推送到远程仓库如github


3、配置SSH（懒得写，直接抄的）
   --第1步：创建SSH Key。在用户主目录下，看看有没有.ssh目录，如果有，      再看看这个目录下有没有id_rsa和id_rsa.pub这两个文件，如果已经有了      ，可直接跳到下一步。如果没有，打开Shell（Windows下打开Git Bash）      ，创建SSH Key：

       $ ssh-keygen -t rsa -C "youremail@example.com"

     用默认值，一路回车就好了
     如果一切顺利的话，可以在用户主目录里找到.ssh目录，里面有id_rsa和      id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不       能泄露出去，id_rsa.pub是公钥，可以放心地告诉任何人（12.PNG）
   --登陆GitHub，打开“Account settings”（13.PNG），“SSH Keys”页面      ：然后，点“Add SSH Key”（14.PNG），填上任意Title，在Key文本框     里粘贴id_rsa.pub文件的内容：（15.PNG）
   --点“Add Key”，你就应该看到已经添加的Key


4、以推送到github为例
   --在github上创建一个新的仓库（9.PNG），填好名字（10.PNG），点          Creating repository
   --下一步看提示，有两条命令，照抄就好（11.PNG 16.PNG）ps:第一次推送     要登录（17.PNG）