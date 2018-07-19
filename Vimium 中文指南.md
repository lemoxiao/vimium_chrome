# Vim 中文指南

## Github 地址
    https://github.com/mutoo/vimium
## 快捷键
    用 `<c-x>`, `<m-x>` 和 `<a-x>` 替代了ctrl+x, meta+x 和 alt+x.
    用 `<X>` 和 `<c-X>` 可以替代 shift+x 和 ctrl+shift+x.

**使用提示：**
    输入`?`可以唤起帮助教程

### 浏览当前页面：

    ?       打开帮助教程/列出所有Vimium命令
    h       向左滑动
    j       向下滑动
    k       向上滑动
    l       向右滑动
    gg      快速到达页面顶部
    G       快速到达页面底部
    d       向下翻动半页
    u       向上翻动半页
    f       在当前页面打开一个链接
    F       在新标签页打开一个链接
    r       重新载入页面
    gs      查看当前页面的源代码
    i       进入插入模式 - 按esc退出模式
    yy      复制当前页面链接至剪贴板
    yf      从页面中复制一个链接至剪贴板
    gf      跳转到下一框架 - 无用
    gF      聚焦视觉于该框架 - 无用


### 打开新的页面
    o       搜索网址，书签，或历史记录，在当前页面打开
    O       搜索网址，书签，或历史记录，在新的页面打开
    b       搜索书签，在当前页面打开
    B       搜索书签，在新的页面打开

### 查找
    /       进入查找模式，输入关键字查找，ESC退出
    n       切换到下一个匹配
    N       切换到上一个匹配
    
**具体操作参考：https://github.com/philc/vimium/wiki/Find-Mode**

### 浏览历史
    H       后退
    L       前进

### 切换tab
    J, gT   切换到左边tab
    K, gt   切换到右边tab
    g0      切换到第一个tab
    g$      切换到最后一个tab
    ^       切换到刚才的tab
    t       创建一个新的页面
    yt      复制当前页面
    x       关闭当前页面
    X       恢复刚才关闭的页面
    T       在当前所有的tab页面中搜索
    <a-p>   对当前页面进行标记或者取消标记

### 标记
    ma      当页标记，只能在当前tab页面跳转，m + 一个小写字母
    mA      全局标记，可以再切换到其他tab的跳转过来，m + 一个大写字母
    `a      跳转到当页标记
    `A      跳转到全局标记
    ``      跳回之前的位置

### 进阶命令
    ]], [[  点击下一页或者Next等快速跳转按钮
    <a-f>   打开多链接在新的窗口中
    gi      跳转到当前文本框/搜索框
    gu      跳转到当前网址的上一级网址
    gU      跳转到当前网址的跟网址
    ge      编辑当前的网址，在当前页面打开
    gE      编辑当前网址，在新的页面打开
    zH      滚动到最左边
    zL      滚动到最右边
    v       进入行观察模式，快速粘贴并且回车，用y进行快拉
    V       进入行观察模式

**Vimium支持重复命令模式，即使用`5t`可以打开5个新标签页，输入错误可以用esc或者c键入取消**

## 自定义映射
-------------------
    你可以在自定义按键设置中取消或者重新设定默认快捷键，每一行输入以下设定命令:
* `map key command`:将命令映射到vimium中，并且覆盖Chrome的默认设置
* `unmap key`: 取消一个命令，并且重新载入Chrome的默认设置
* `unmapAll`: 取消所有命令绑定，当你尝试删除vimium的所有命令并且开始自己的设定

**eg.**
    `<map <c-d> scrollPageDown>` 设置`<c-d>`为 ctrl+d 的按键，并且覆盖chrome设定
    `map r reload` 设置 `r` 为reload 的快捷键
    `unmap <c-d>` 取消 c-d 的设置


## Vimium快速使用搜索引擎
命令：
    按 `o` 进入搜索模式，然后输入`缩写+搜索内容`.
eg:
    `o`+`g vimium github readme`  //即用google搜索关键词：vimium github readme
    `o`+ `y edsheeran perfect`    //即在youtube中搜索：edsheeran perfect
提示:
    当你输入上述语句时，搜索模式会给出对应的补全提示
    
### 具体设置：   
打开Vimium的设置选项中，在自定义搜索引擎的搜索格式，具体格式可以自行搜索，以下给出常见的搜索引擎格式：
    //谷歌
    # g: http://www.google.com.hk/search?q=%us 
    //油管视频
    # y: https://www.youtube.com/results?search_query=%s 
    //谷歌地图
    # gm: https://www.google.com/maps?q=%s
    //必应 
    # b: https://www.bing.com/search?q=%s 
    //百度
    # bd: http://www.baidu.com/s?wd=%s
    //B站
    # bl: http://www.bilibili.tv/search?keyword=%s 
    //维基
    # w: https://www.wikipedia.org/w/index.php?title=Special:Search&search=%s 
    //知乎
    # zh:https://www.zhihu.com/search?type=content&q=%s
    //爱词霸
    # icb: http://www.iciba.com/%s
    //有道
    # yd: http://dict.youdao.com/search?q=%us
    //谷歌学术：
    # gs: http://scholar.google.com.hk/scholar?q=%us&hl=zh-CN
    //github:
    # gt: https://github.com/search?q=%s
    
注：#号表示注释，使用时去掉#

