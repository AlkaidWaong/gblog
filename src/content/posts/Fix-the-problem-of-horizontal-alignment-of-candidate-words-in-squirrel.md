---
title: "修复鼠须管候选词横向排列失效问题"
description: "发现鼠须管 1.0.0版本中侯选词横排失效了，去看了一下官方文档发现是因为：style/horizontal 被移除了"
pubDate: "2024-07-01 15:42:01"
category: "pmlife"
banner: "@images/banners/_1553621520_6d34Z1x7UB.jpg"
tags: ["mac输入法", "鼠须管"]
oldViewCount: 2387
oldKeywords: ["mac输入法", "mac", "鼠须管"]
---


发现鼠须管 1.0.0版本中侯选词横排失效了，去看了一下官方文档发现是因为：`style/horizontal` 被移除了，并且官方给出了新控件来支持：

```
candidate_list_layout: stacked/linear
text_orientation: horizontal/vertical
```

修复侯选词横向效果的做法：

1. 删掉horizontal配置
2. 增加 **candidate_list_layout: linear**和**text_orientation: horizontal**

![image-20240701095445744](https://p.ipic.vip/p3djb2.png)