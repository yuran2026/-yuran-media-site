# 余然门窗 H5小程序 素材交付清单
> 生成时间：2026-06-02 | 总计：58张图片 + 6篇科普文章
> 电话：17768075973 | 地址：义乌北苑街道雪峰西路 220 号

---

## 一、首页轮播海报（10张）
路径：`images/banners/`

| 文件名 | 用途 | 尺寸 |
|--------|------|------|
| banner_01.jpg | 品牌主视觉 "余然门窗 · 高端系统门窗定制" | 1200×600 |
| banner_02.jpg | "免费量房 · 免费出方案 · 限时到店领取权益" | 1200×600 |
| banner_03.jpg | "无损换窗 · 不破坏装修 · 当天换当天住" | 1200×600 |
| banner_04.jpg | 精装房换窗专题海报 | 1200×600 |
| banner_05.jpg | 小区门窗团购活动海报 | 1200×600 |
| banner_06.jpg | 系统窗定制服务海报 | 1200×600 |
| banner_07.jpg | 阳台封窗案例展示海报 | 1200×600 |
| banner_08.jpg | 阳光房定制海报 | 1200×600 |
| banner_09.jpg | "老房换新窗·专业施工·不破坏装修" | 1200×600 |
| banner_10.jpg | "预约上门量尺·免费出方案" | 1200×600 |

## 二、6类产品案例图（每类6张，共36张）
路径：`images/cases/{分类名}/case_01.jpg ~ case_06.jpg`

| 分类 | 路径 | 图片数 |
|------|------|--------|
| 平开窗实景案例 | images/cases/平开窗/ | 6 |
| 推拉窗实景案例 | images/cases/推拉窗/ | 6 |
| 阳光房定制案例 | images/cases/阳光房/ | 6 |
| 阳台封窗案例 | images/cases/阳台封窗/ | 6 |
| 精装房无损换窗 | images/cases/无损换窗/ | 6 |
| 老房换窗实拍 | images/cases/老房换窗/ | 6 |

## 三、科普文章配图（12张）
路径：`images/articles/article_01.jpg ~ article_12.jpg`

| 文件名 | 对应文章 |
|--------|----------|
| article_01.jpg + article_02.jpg | 系统窗型材怎么选？ |
| article_03.jpg + article_04.jpg | 门窗玻璃挑选干货 |
| article_05.jpg + article_06.jpg | 门窗五金件有多重要？ |
| article_07.jpg + article_08.jpg | 门窗行业内幕秘密 |
| article_09.jpg + article_10.jpg | 看懂门窗安装细节 |
| article_11.jpg + article_12.jpg | 精装老房无损换窗攻略 |

## 四、6篇科普文章
路径：`articles/article_01.html ~ article_06.html`

| 文件 | 标题 | 字数 | 适用Tab |
|------|------|------|---------|
| article_01.html | 系统窗型材怎么选？新手选购不踩坑 | ~400字 | Tab3·避坑科普专栏 |
| article_02.html | 门窗玻璃挑选干货，不同房型适配玻璃详解 | ~450字 | Tab3·避坑科普专栏 |
| article_03.html | 门窗五金件到底有多重要？决定窗户使用寿命 | ~400字 | Tab3·避坑科普专栏 |
| article_04.html | 门窗行业不会告诉你的内幕秘密 | ~450字 | Tab3·避坑科普专栏 |
| article_05.html | 看懂门窗安装细节，避开80%装修踩坑问题 | ~450字 | Tab3·避坑科普专栏 |
| article_06.html | 精装老房无损换窗攻略 | ~500字 | Tab3·避坑科普专栏 |

每篇文章均为独立HTML文件，自带完整样式（深蓝+金色品牌色系），可直接嵌入H5页面。

## 五、品牌视频（1分钟）
| 文件 | 格式 | 大小 | 用途 |
|------|------|------|------|
| video/brand_video.mp4 | MP4 (H.264) | 5.18MB | 首页品牌介绍区 + Tab2动态页置顶 |

视频组件HTML已预制：`video_component.html`（深蓝深色背景+金色装饰+视频播放器+CTA按钮），直接嵌入首页和Tab2。

---

## 六、WorkBuddy 导入清单
> 一键导入：读取 `asset-manifest.json` 获取完整映射配置

| 步骤 | 素材 | 目标位置 |
|------|------|----------|
| 1 | images/banners/banner_01~10.jpg | 首页轮播组件 |
| 2 | video/brand_video.mp4 + video_component.html | 首页品牌视频区 + Tab2动态页置顶 |
| 3 | images/cases/{分类}/case_01~06.jpg | Tab3·6个分类案例列表 |
| 4 | images/articles/article_01~12.jpg | Tab3·6篇科普文章顶部配图（每篇2张） |
| 5 | articles/article_01~06.html (提取body) | Tab3·避坑科普专栏详情页 |
| 6 | asset-manifest.json -> global | 电话17768075973 + 地址义乌北苑街道雪峰西路220号 全局注入 |

### WorkBuddy执行提示词
```
请读取 asset-manifest.json，将 yuaran-h5-assets 目录下的所有素材按映射规则批量替换到H5小程序中：
- 轮播图：images/banners/ → 首页swiper组件
- 品牌视频：video/brand_video.mp4 + video_component.html → 首页第2区块 + Tab2置顶
- 案例图：images/cases/ → Tab3各分类案例列表
- 文章：articles/ → Tab3科普专栏详情页（每篇配2张article图）
- 全局信息：电话17768075973 + 地址义乌北苑街道雪峰西路220号
完成后验证：5个Tab全部可切换、图片加载正常、视频可播放、文章可查看
```
