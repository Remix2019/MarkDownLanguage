#一级标题 （建议在井号后加一个空格）
## 二级标题 
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

---
##无序列表
* 第一行
* 第二行
* 第三行 (与---分隔符 要间隔)

---
## 有序列表
1. 第一行
2. 第二行
3. 第三行 


---
## 引用文本
> 文本格式（输入你想写的文字、段落）
  如果你需要引用一小段别处的句子，那么就要用引用的格式。


---

##引用图片 （第一种格式 纯图片）,如有版权问题，请告知，立即删除
![Markdown](http://ww2.sinaimg.cn/large/6aee7dbbgw1esvkj19bqmj20e80e874z.jpg)

##引用图片  （第二种格式 超链接）
！[Markdown](http://ww2.sinaimg.cn/large/6aee7dbbgw1esvkj19bqmj20e80e874z.jpg)

---

## 粗体和斜体  两个** ，在文本的两边，要匹配
**在这里粘贴您的Markdown文档，点击“预览”按钮转换为HTML格式。**

---


## Markdown基础语法

下面是Markdown的常用语法示例，可供参考

### 代码示例
1.插入普通代码 

`
System.out.println("打印一段文字");
`

2.插入JavaScript代码段
```javascript
var OnlineMarkdown = {
  init: function() {
    var self = this;
    self.load().then(function() {
      self.start()
    }).fail(function(){
      self.start();
    });
  },
  start: function() {
    this.updateOutput();
  },
  load: function() {
    return $.ajax({
      type: 'GET',
      url: params.path || './demo.md',
      dateType: 'text',
      timeout: 2000
    }).then(function(data) {
      $('#input').val(data);
    });
  },
  updateOutput: function () {
    var val = this.converter.makeHtml($('#input').val());
    $('#output .wrapper').html(val);
    PR.prettyPrint();
  }
};

OnlineMarkdown.init();
```
---

3.插入`php`代码

```php
echo 'hello,world'
```

---
### 表格示例

| 品类 | 个数 | 备注 |
|-----|-----|------|
| 苹果 | 1   | nice |
| 橘子 | 2   | job |


---
##分割线 
***

***

---

## 地址链接格式<>
<www.baidu.com>  

以上是用的比较多的，还装了几十个使用频度比较低的插件，主要包括 Snippet 和文件高亮配置，可以在这里查看：<https://gist.github.com/barretlee/a5170eb6ca1805f66687063d2e3a4983>，你也可以通过 `Settings Sync` 将这个配置下载下来，id 就是后面半截：`a5170eb6ca1805f66687063d2e3a4983`。

### 在命令行打开 VSC

在安装好 VSC 后，直接配置 `.bash_profile` 或者 `.zshrc` 文件：
插入脚本语言`bash`
```bash
alias vsc='/Applications/Visual\ Studio\ Code.app/Contents/Resources/app/bin/code';
VSC_BIN='/Applications/Visual\ Studio\ Code.app/Contents/Resources/app/bin';
PATH=$VSC_BIN:$PATH;
export PATH;
```

然后让配置生效，在控制台执行：

```bash
# 如果没有安装 zsh，可能是 ~/.bash_profile
source ~/.zshrc 
```

这个时候就可以在全局打开了：

```bash
# -a 的意思是不要新开窗口，在当前已经打开的 vsc 中打开文件
vsc path/to/file.ext -a 
```

有同学提到，VSC 的面板上搜索 `install` 就可以在命令行安装 `code` 这个命令了，不过我更喜欢使用 `vsc` 来打开文件，这也算是折腾吧 ；）
