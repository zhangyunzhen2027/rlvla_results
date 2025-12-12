# 实验结果展示网站

这是一个用于展示实验结果的GitHub Pages网站，包含一个可以嵌入视频的表格。

## 功能特点

- 📊 美观的表格布局
- 🎬 支持在表格中嵌入视频
- 📱 响应式设计，支持移动设备
- ➕ 动态添加新实验行
- 🎨 现代化的UI设计

## 使用方法

### 1. 设置GitHub Pages

1. 将代码推送到GitHub仓库
2. 在仓库设置中，进入 "Pages" 选项
3. 选择 "Source" 为 "main" 分支（或您的主分支）
4. 选择 "/ (root)" 作为文件夹
5. 点击保存

### 2. 添加视频

有两种方式添加视频：

#### 方式一：通过界面添加
1. 点击表格中的视频占位符
2. 输入视频URL（可以是GitHub仓库中的视频文件路径，或在线视频链接）

#### 方式二：直接编辑HTML
1. 打开 `index.html` 文件
2. 找到对应的 `<div class="video-placeholder">` 标签
3. 替换为 `<video>` 标签，例如：

```html
<video controls style="width: 100%; max-width: 600px; height: auto; border-radius: 10px; box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15); background: #000; margin: 0 auto; display: block;">
    <source src="videos/experiment1.mp4" type="video/mp4">
    您的浏览器不支持视频标签。
</video>
```

### 3. 编辑实验信息

直接编辑 `index.html` 文件中的表格内容：
- 修改实验名称
- 更新描述信息
- 添加或删除实验行

### 4. 添加视频文件到仓库

如果使用本地视频文件：
1. 在仓库中创建 `videos` 文件夹
2. 将视频文件上传到该文件夹
3. 在HTML中使用相对路径引用，例如：`videos/experiment1.mp4`

**注意**：GitHub对文件大小有限制，建议：
- 单个文件不超过100MB
- 如果视频较大，建议使用外部视频托管服务（如YouTube、Bilibili等），然后使用iframe嵌入

## 支持的视频格式

- MP4 (推荐)
- WebM
- OGG

## 使用外部视频服务

### YouTube
```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="border-radius: 10px;"></iframe>
```

### Bilibili
```html
<iframe src="//player.bilibili.com/player.html?aid=VIDEO_AID&bvid=BVID&cid=CID&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" style="width: 100%; max-width: 600px; height: 400px; border-radius: 10px;"></iframe>
```

## 自定义样式

可以修改 `index.html` 中的 `<style>` 部分来自定义：
- 颜色主题
- 表格样式
- 字体大小
- 间距和布局

## 许可证

MIT License

