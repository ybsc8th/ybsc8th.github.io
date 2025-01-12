---
date: 2024-12-23 12:26:40
layout: post
title: 代加工详情事项
subtitle: 我们有着最优惠的代加工服务
description: 我们有着最优惠的代加工服务
image: https://res.cloudinary.com/dm7h7e8xj/image/upload/v1559821648/theme1_eoyjtl.jpg
optimized_image: https://res.cloudinary.com/dm7h7e8xj/image/upload/c_scale,w_380/v1559821648/theme1_eoyjtl.jpg
category: 'tips'
tags:
  - service
  - technology
author: Albert
---
欢迎您前来咨询代加工事项，我们的抽水率极低，有极大的价格优势。我们支持多种定价方式，可以商讨不同的生产成本分配方案。

我们当前附赠的服务有：

- `产品3D建模服务`
- `产品原料检查（帮您检查是否有漏掉的原料，让您方在答辩时更加从容）`
- `产品结构设计检查（帮您检查产品的结构是否合理，设计是否可行）`


我们希望能够找到优秀的原料公司、传媒公司与经销公司，在合理的报价范围内，我相信我们可以达成愉快的协定。
我方目前对于展销位的需求量较大，希望各经销公司能火速与我们取得联系！

# 抽成方案：
## 方案1：固定比率
在此方案下，我方比率为：
`20 20 25 28 碳排五五`
与其他制造公司保持`一致`，但是我们的附赠服务无疑会为您的展销带来极大的优势！

## 方案2:科学算法
我方算法代码如下：

```python
# CodeIgniter
# This content is released under the MIT License (MIT)
# Copyright (c) 2025 - 2026, Tianjin No.1 High School
# Copyright (c) 2025 - 2026, StarRingCorporation Team (https://starringcorporation.github.io/)
#Permission is hereby granted, free of charge, to any person obtaining a copy
#of this software and associated documentation files (the "Software"), to deal
#in the Software without restriction, including without limitation the rights
#to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
#copies of the Software, and to permit persons to whom the Software is
#furnished to do so, subject to the following conditions:

#It is strictly prohibited for other commercial competition companies to use our algorithm code, 
#and copying our code is not allowed. Otherwise, 
# we will be sued after participating, and we reserve all rights to the code.

#The above copyright notice and this permission notice shall be included in
#all copies or substantial portions of the Software.

#THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
#IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
#FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
#AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
#LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
#THE SOFTWARE.

#@package	CodeIgniter
#@author	EllisLab Dev Team
#@copyright	Copyright (c) 2025 - 2026, Tianjin No.1 High School
#@copyright	Copyright (c) 2025 - 2026, StarRingCorporation Team (https://starringcorporation.github.io/)
#@license	http://opensource.org/licenses/MIT	MIT License
#@link	https://starringcorporation.github.io/
#@since	Version 1.0.0
#@filesource

import sys
# 常量部分
P = 0.02  # 目标起步净挣系数（净利润抽成率）
# 从用户输入获取数据
S = float(input("请输入年度总销售额（黄金）："))
s = float(input("请输入原料成本（黄金）："))
X = float(input("请输入生产中消耗的黄金量："))

# 基础计算部分
# 计算生产成本C（黄金+碳排），碳排五五分
C = X * 1.5
print(f"生产成本为：{C}黄金")


# 算法部分
# 计算回本抽成比例R_cost和R_realcost，也就是低于这个数字我们会亏本
R_cost = C / S
print(f"成本抽成比例为：总销售额的{R_cost:.2%}")
R_realcost = C /(S-s-X)
print(f"成本抽成比例为：净利润的{R_realcost:.2%}")
if R_realcost > 0.24:
    print("您方利润率过低，这种情况无论在哪一家制造公司都是不被接受的水准")
    print("请更换代数再次尝试")
    sys.exit()#终止程序
# 根据财年确定额外增加的百分点
#一到四财年预估为0.02 0.03 0.04 0.05
additional_percent = 0.05
# 计算最低目标抽成比例R_real
R_real = (C + (S-s-X)*P ) / (S-s-X)
if R_real <= 0.24:
    R_min = (C + (S-s-X)*P ) / S
    print(f"最低抽成比例为：总销售额的{R_min:.2%}")
    print(f"最低抽成比例为：净利润的{R_real:.2%}")
    R = R_real + additional_percent
    # 以下的数字是根据其他公司的报价进行的计算
    # 一到四财年最高抽成为0.20 0.20 0.23 0.27
    # 我方算法的优点：
    # 方便我方了解我们能够赚多少，方便您方了解我们有多赚钱，以及便于您方了解可以跟我方回旋的利润空间
    if R < 0.24:#0.24为最低高利润系数，目的是让我们的利润足够多，不会倒闭
        R= 0.24
    #如果您方利润率过低，也就是根据算法，加上额外抽成比例后高于27%的比率，我们一律按照27%进行抽成，当然如果我们有更多更深入的合作的话，可以帮您把比例降到28%
    elif R > 0.27:
        R = 0.27
    #如果您方利润率一般，根据算法，加上额外抽成比例后处于20%~25%之间，我们一律按照25%进行抽成
    else:
        R = 0.25
    # 计算实际抽成比例
    R_total = R*(S-s-X)/S
    print(f"实际抽成比例为：总销售额的{R_total:.2%}")
    print(f"实际抽成比例为：净利润的{R:.2%}")
else:
    print("您方利润率似乎太低了，但是我们也不是不能做")
    R = 0.24
    R_total = R*(S-s-X)/S
    print(f"实际抽成比例为：总销售额的{R_total:.2%}")
    print(f"实际抽成比例为：净利润的{R:.2%}")



```

***算法代码一切版权归我方所有，严禁复制/在自己制造公司内部使用，否则我方将追究您方责任！***

算法计价的取值区间一般为普通计价方案的-3%到+0.5%之间，多数情况下低于其他公司报价。

`我方算法的好处：`

- 您的产品利润率越高，我们的抽成越低，你们赚的就更多
- 方便我方了解我们能够赚多少
- 方便您方了解其他制造公司还有我们自己有多 ~~“坑人”~~ （bushi）
- 便于您方了解可以跟我方回旋的利润空间

同时，您需要注意：
 1. 如果对于系数有疑问的话可以提出质疑
 2. 如果双方合作密切的话最后的抽成可以接近我们的最低抽成比例
 3. 如果希望能够带数试一下的话可以访问：（对不起，目前发布的程序正在审核中）
 4. 您方可以调整碳排放承担系数，您方承担的越低，我们抽得越低

#### 来几组数据试一下：

> tips：我们具体的抽成，需要在您方把产品卖完后，把数据给我们（总销售额，原料成本），您监督我们，我们把我们的制造消耗还有您方数据输入进去，得到最后的抽成。不等到您方卖完，我们自己都不知道这个数据会是多少。而且，我们设的最高实际抽成率就是根据其他制造公司> 的抽成率定的，因此我们的定价只低不高。具体的定价范围由最低目标抽成比例和最高抽成比例（最高抽成比例<=其他制造公司最高抽成率）（假设最低最高两个相差x）决定，具体为你们减多少是要看你们能拿出多大的诚意，决定我们能降的是x的百分之多少。

**年度总销售额**：我们生产的这些产品一共买了多少钱

**原料成本**：原料是原料，制造是制造，我们公司不负责任何与原料有关的承担，但是可以为您联系原料公司

**生产中消耗的黄金量**：这个是由商赛系统算的，我们也不知道具体是多少

**生产成本**：我们的黄金+碳排，因为黄金：碳排=100:1，碳排五五分成，所以生产成本折合为黄金就是1.5倍原来的黄金

**成本抽成**：这个是我们的生产成本所占的百分比

**最低抽成**：至少也得有一点利润吧，太低了我们活不下去啊

**实际抽成**：能抽尽抽，这个就相当于是我们的最高报价

```python
请输入年度总销售额（黄金）：300000
请输入原料成本（黄金）：30000
请输入生产中消耗的黄金量：30000
生产成本为：45000.0黄金
成本抽成比例为：总销售额的15.00%
成本抽成比例为：净利润的18.75%
最低抽成比例为：总销售额的16.60%
最低抽成比例为：净利润的20.75%
实际抽成比例为：总销售额的20.00%
实际抽成比例为：净利润的25.00%
```

```python
请输入年度总销售额（黄金）：300000
请输入原料成本（黄金）：30000
请输入生产中消耗的黄金量：10000
生产成本为：15000.0黄金
成本抽成比例为：总销售额的5.00%
成本抽成比例为：净利润的5.77%
最低抽成比例为：总销售额的6.73%
最低抽成比例为：净利润的7.77%
实际抽成比例为：总销售额的20.80%
实际抽成比例为：净利润的24.00%
```
```python
请输入年度总销售额（黄金）：300000
请输入原料成本（黄金）：100000
请输入生产中消耗的黄金量：10000
生产成本为：15000.0黄金
成本抽成比例为：总销售额的5.00%
成本抽成比例为：净利润的7.89%
最低抽成比例为：总销售额的6.27%
最低抽成比例为：净利润的9.89%
实际抽成比例为：总销售额的15.20%
实际抽成比例为：净利润的24.00%
```
```python
请输入年度总销售额（黄金）：300000
请输入原料成本（黄金）：10000
请输入生产中消耗的黄金量：1000
生产成本为：1500.0黄金
成本抽成比例为：总销售额的0.50%
成本抽成比例为：净利润的0.52%
最低抽成比例为：总销售额的2.43%
最低抽成比例为：净利润的2.52%
实际抽成比例为：总销售额的23.12%
实际抽成比例为：净利润的24.00%
```
```python
请输入年度总销售额（黄金）：687500
请输入原料成本（黄金）：431250
请输入生产中消耗的黄金量：98000
生产成本为：147000.0黄金
成本抽成比例为：总销售额的21.38%
成本抽成比例为：净利润的92.89%
您方利润率过低，这种情况无论在哪一家制造公司都是不被接受的水准
请更换代数再次尝试
```
最后这一组数据说明：别的公司在这个情况下如果仍然报价28%的话，那就是骗人的，根本回不了本

### 答疑

**问：这个算法的适用条件是什么？**

> 答：所有的，无论是竞标还是普通。


**问：这个算法是第几财年的？**

> 答：目前的数字是`第四财年`的，如果需要其他财年的请联系我们
> 或者等到我们出第二版

**问：最高抽成是多少？**

> 答：如果您方利润率过低，也就是根据算法，加上额外抽成比例后高于27%的比率，我们一律按照`27%`进行抽成，当然如果我们有更多更深入的合作的话，可以帮您把比例降到`27%`
> 最坏的情况，出现在产品品质极差的情况下，这个时候我们的抽成就是回本抽成了。这个回本抽成我们不知道其他公司是怎么定的，反正我们要的是完全回本。

**问：碳排和消耗黄金？**

> 答：`碳排五五，黄金我们全出（已包含在算法中）`，这两部分就是我们算法给出的成本抽成。您需要注意，我们的碳排放承担可以进行协商，这样我们的抽水将会更低！

**问：您方的升级方案？**

> 答：我们有这个在第三财年升到四级工厂的意愿，但是未来难测，能不能升级，也需要靠你们的全产业链支撑



