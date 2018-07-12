#任务一
## HTML的定义、概念、发展简史
- HTML 指的是超文本标记语言。
- XHTML 指的更严谨更纯净的HTML版本，是W3C标准。（几乎与HTML4.01相同）
- XML W3C标准 可扩展标记语言 设计本意是传输数据
 - HTML5 新一代的HTML 大部分浏览器已经支持HTML5
- 目前主流的版本是HTML5 

## HTML5 新特性
- 新的语义化标签 ``article``、``footer``、``header``、``nav``、``section``
- 用于绘画的canvas元素
- 用于媒体播放的vedio audio元素
- 本地离线存储 localStorage sessionStorage
- 元素现在可以编辑与拖动 contenteditable draggable
- 新的跨域方式 window.postMessage
- 获取地理位置 上传文件等api
- 使用 html5shiv 兼容低版本ie

## 常用HTML标签
- **body** 展示在页面内容必须在body标签中。
- **p** 段落，块级元素，用来放置文本信息
- **hx** 标题标签有6个 h1 h2 h3 h4 h5 h6 重要性递减 h1会被爬虫和搜索引擎抓取 SEO用
- **strong em** 强调关键字用，strong语义比em更强
- **span** 无语义 文本元素 为了设置单独的样式而使用
- **q** 对简单文本的引用 语义：引用别人的话
- **blockquote** 对长文本的引用
- **br** 回车
- **&nbsp** 在HTML中输入空格、回车是没用的，要想输入空格，必须写入$nbsp;
- **ul** ul>li无序列表
- **ol** ol>li有序列表
- **dl** dl>dt+dd 定义列表 dt定义 dd描述item
- **div** 块级元素 最常用的容器
- **table** table>thead>tr>th>tbody>tr>th thead语义表头 tbody语义表内容 带有tbody标签会等内容下载后再一起显示，和thead一样非必须 tr行 th 列
- **a** anchor标签 超链接 有默认的提交行为 需要使用e.preventDefault()  href=”目标网址” title=”鼠标滑过显示的文本” 链接显示的文本 /a .title属性的作用，鼠标滑过链接文字时会显示这个属性的文本内容。主要方便搜索引擎了解链接地址的内容（语义化更友好） a href=”目标网址” target=”_blank” click here! /a在新的网页中打开
- **img** 插入图片 img src=”图片地址” alt=”下载失败时的替换文本” title = “提示文本” src：标识图像的位置；alt：指定图像的描述性文本，当图像不可见时（下载不成功时），可看到该属性指定的文本；title：提供在图像可见时对图像的描述(鼠标滑过图片时显示的文本)；图像可以是GIF，PNG，JPEG格式的图像文件。
- **form** 表单，把数据传输到服务器，form method=”传送方式” action=”服务器文件” . form标签是成对出现的，以form开始，以/form结束。action ：浏览者输入的数据被传送到的地方,比如一个PHP页面(save.php)。method ： 数据传送的方式（get/post）。所有表单控件（文本框、文本域、按钮、单选框、复选框等）都必须放在标签之间
    - ```<form   method="传送方式"   action="服务器文件">```
- **input** 文本输入框 根据type可以变成文本框（text）密码框（password）value() 文本的默认值 placeholder 默认框内文本，点击即消失
    - ```<form>
            <input type="text/password" name="名称" value="文本" />
</form>```

- **textarea** 当用户输入打断文字时使用 
    - ```<textarea  rows="行数" cols="列数">文本</textarea>``` 
- **radio / checkbox** 单选框、复选框，让用户选择,input type=”radio/checkbox” value=”值” name=”名称” checked=”checked”/> 当 type=”radio” 时，控件为单选框,当 type=”checkbox” 时，控件为复选框,value：提交数据到服务器的值（后台程序PHP使用）,name：为控件命名，以备后台程序 ASP、PHP 使用,checked：当设置 checked=”checked” 时，该选项被默认选中,同一组的单选按钮，name 取值一定要一致，这样同一组的单选按钮才可以起到单选的作用。
    - ```<input   type="radio/checkbox"   value="值"    name="名称"   checked="checked"/>```
- **select** 下拉表单 设置selected=“selected”默认被选中
    - ```<select>
            <option value="看书">看书</option>
            <option value="旅游" selected="selected">旅游</option>
            <option value="运动">运动</option>
            <option value="购物">购物</option>
        </select> ```
- **multiple** 下拉列表也可以进行多选操作，在标签中设置multiple=”multiple”属性，就可以实现多选功能
    - ```<select multiple="multiple">```
- **submit** 使用提交按钮提交数据 有默认提交表单的行为 value为按钮上的字
    - ```<input   type="submit"   value="提交">```
- **reset** 重置表单信息，type：只有当type值设置为reset时，按钮才有重置作用,value：按钮上显示的文字
    - ```<input type="reset" value="重置">```
- **label** 提高可用性，当用户点击该标签，自动将焦点转到标签相关的表单空间上 for的值要和相关空间的id值一样
    - ```<label for="控件id名称">```
