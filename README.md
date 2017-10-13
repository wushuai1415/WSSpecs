# WSSpecs
## 1.创建git仓库
- 在git仓库中创建一个新仓库，这里我们以码云为例：
![创建git仓库](http://picture-ws.oss-cn-beijing.aliyuncs.com/WSCategory/181FF836-4ACD-4A6B-B97A-D3AC031E1816.png?Expires=1507869961&OSSAccessKeyId=TMP.AQF3AWFf2YDKJ_dyvr6nVlvg_vtKzDtjzXDTugc1IOCpP28NKgk23VOIcT3BAAAwLAIUF8Bj-uTz4hlJ2e-zgUt3OOjZ6MMCFHX9nZ0Qmlgrq7C1czPKEf_va67G&Signature=e2gi2zZWml%2BekM1vXR%2FyX%2BPXOv8%3D "创建git仓库")<br />
- 点击创建会生成3个文件，readme为说明文件具体编写格式下面有具体说明，LICENSE文件为开源可许证，这里选择的是MIT License：
![创建成功](http://picture-ws.oss-cn-beijing.aliyuncs.com/WSCategory/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-10-13%20%E4%B8%8A%E5%8D%8811.45.41.png?Expires=1507869974&OSSAccessKeyId=TMP.AQF3AWFf2YDKJ_dyvr6nVlvg_vtKzDtjzXDTugc1IOCpP28NKgk23VOIcT3BAAAwLAIUF8Bj-uTz4hlJ2e-zgUt3OOjZ6MMCFHX9nZ0Qmlgrq7C1czPKEf_va67G&Signature=6Wi8%2FbgKhyEzSYURQ16tijCHtjo%3D "创建成功")<br />
## 2.clone 仓库到本地
- 创建成功后，将仓库clone到本地。首先cd到本地仓库目录，然后clone到本地：

        cd ~
        git clone https://gitee.com/ws1350/WSSpecs.git
- 此时的目录结构为：

        |____LICENSE
        |____README.md

## 3.在本地仓库中添加pod的依赖文件
- 在本地仓库中创建一个文件夹存放共享类，并将相关的类放入目录中，如：

- 执行命令创建podspec文件：

        pod spec create WSSpecs（文件名）
- 编辑podspec文件

- 如果有需要的话可以创建一个demo目录存放测试代码，此时的目录结构为

        |____LICENSE
        |____README.md
        |____WSSpecs.podspec
        |____WSSpecs
        |____WSSpecsDemo
## 4.将代码提交到git仓库中
- 在本地创建私有repo，执行命令：

        pod repo add WSSpecs（仓库名） https://github.com/marklin2012/O2Specs.git（仓库地址）
- 对编辑好的pod库进行验证，执行命令：
        
        pod lib lint --allow-warnings
- 验证成功之后，将podspec添加到repo中

        pod repo push WSSpecs（仓库名） WSSpecs.podspec（podspec文件）


## 附录一（pod lib lint 错误信息 及 解决方法）
## 附录二（pod repo push 错误信息 及 解决方法）
         ERROR | [iOS] unknown: Encountered an unknown error ([!] /usr/bin/git clone https://github.com/wushuai1415/WSSpecs.git /var/folders/h0/dkxsqhyn0ldb6xznmdw3ywyw0000gn/T/d20171013-60019-13ykicu --template= --single-branch --depth 1 --branch 0.0.1
         错误原因：git仓库没有打tag
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br /><br /><br /><br /><br /><br /><br /><br /><br /><br />

## 附录三（readme编辑格式）
readme 格式:
# 大标题：# 标题内容 或 标题内容 下跟上 =========，如：
        大标题
        ==========
        或
        # 大标题
        注意：====上的区域都为大标题，#和标题内容中间有 空格

## 中标题：## 标题内容 或 标题内容 下跟上----------，如：
        中标题
        ---------------------
        或
        ## 中标题
        注意：------上的区域都为中标题，#和标题内容中间有 空格

### 小标题：### 标题内容，如：
        ### 小标题

### 单行文本框：tabtab（两次tab键）文本内容，如：
        单行文本框

### 多行文本框：多个单行文本框组成，如：
        单行文本框
        单行文本框

### 代码块（多行文本框）
        - （void）main {
            NSLog(@"hellow world");
        }

### 连接：\[显示文字\]\(地址\)，如：
\[点击这里你可以链接到www.google.com\]\(http://www.google.com)<br />
[点击这里你可以链接到www.google.com](http://www.google.com)

### 图片：\!\[图片名\]\(地址 "图片名"\)
\!\[github\]\(http://github.com/unicorn.png "github"\)<br />
![github](http://github.com/unicorn.png "github")

### 文字被些字符包围
\> 文字被些字符包围
> 文字被些字符包围
>
> 只要再文字前面加上>空格即可
>
> 如果你要换行的话,新起一行,输入>空格即可,后面不接文字
> 但> 只能放在行首才有效

###
> 文字被些字符包围开始
>
> > 只要再文字前面加上>空格即可
>
>  > > 如果你要换行的话,新起一行,输入>空格即可,后面不接文字
>
> > > > 但> 只能放在行首才有效

### 特殊字符：\字符
你想换行的话其实可以直接用html标签\<br /\>

