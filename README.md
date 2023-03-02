# 中医开源医典

> Traditional Chinese Medicine Open Classics

中医开源医典希望可以构建一个开源的中医资料库和语料库。目前的重点是收录尽可能多的中医典籍、书籍，并整理出一套元数据结构以及相关工具，并建立开源工作流来帮助资料修订和完善。

## 分门别类

可以参考[《中醫笈成》](https://jicheng.tw/tcm/book/index.html)的分类方法：

1. 医经类
   1. 内经
      1. 素问
      2. 灵枢
      3. 综合
   2. 难经
   3. 其它
2. 诊法类
   1. 脉诊
   2. 望诊
   3. 舌诊
3. 本草类
   1. 唐以前
   2. 宋金元
   3. 明代
   4. 清代
   5. 国外
   6. 炮制
4. 医方类
   1. 唐以前
   2. 宋金元
   3. 明代
   4. 清以后
   5. 国外
   6. 单方验方
5. 针灸经穴类
6. 伤寒金匮类
   1. 伤寒
   2. 金匮
   3. 综合
7. 温病类
8. 内科
   1. 专论
9. 妇产科
10. 儿科
11. 外科
12. 伤科
13. 五官科
    1.  眼科
    2.  喉科
    3.  口齿科
14. 祝由科
15. 养生类
16. 医案类
17. 医论医话随笔类
18. 综合医书类
19. 医史考释类
20. 其他类
21. 丛书


## 文献文件结构

文献可以考虑使用 [Markdown](https://zh.wikipedia.org/wiki/Markdown) 语法进行不同结构文字的表达，比如标题、段落、序言、列表等。文字不使用换行来对齐，换行仅表示段落结束。

文献元数据使用[front-matter](https://jekyllrb.com/docs/front-matter/)的形式在文件开头以YAML的格式标注。

### 文献元数据

每个文献应该提供一些元数据，用于检索以及整理。如：

* `title`: 书名
* `author`: 作者
* `era`: 朝代
* `date`: 年代可以是精确年代，也可以是一个年代范围，起止年数字间用`~`间隔
* `version`: 版本
* `category`: 类别
* `tags`: 标签

### 示例


```markdown
---
title: 海药本草
author: 李珣
date: 907~930
era: 五代 - 前蜀
version:
category: 本草类
tags:
---

# 海药本草

## 玉石部卷第一

### 玉屑

按《异物志》云∶出昆仑。又《淮南子》云∶出钟山。又云蓝田出美玉，燕口出璧玉。味咸，寒，无毒。主消渴，滋养五脏，止烦躁，宜共金银、麦门冬等同煎服之，甚有所益。《仙经》云∶服玉如玉化水法，在《淮南三十六水法》中载。又《别宝经》云∶凡石韫玉，但夜将石映灯看之，内有红光，明如初出日，便知有玉。《楚记》∶卞和三献玉不鉴，所以遭刖足。后有辨者，映灯验之，方知玉在石内，乃为玉玺，价可重连城也。（《大观》卷三页９，《政和》页８２，《纲目》页６１４）

### 车渠

《韵集》云∶生西国，是玉石之类，形似蚌蛤，有文理。大寒，无毒。主安神镇宅，解诸毒药及虫螫。以玳瑁一片、车渠等，同以人乳磨服，极验也。又《西域记》云∶重堂殿梁檐，皆以七宝饰之，此其一也。（《大观》卷三页３７，《政和》页９６，《纲目》页１６４７）

```

对于语料库的生成，可以对 Markdown 进行解析，然后按照特定格式生成文本文件。

## 文献资料参考

* 初步资料来自 https://github.com/xiaopangxia/TCM-Ancient-Books
* 维基文库: https://zh.wikisource.org/wiki/Category:%E4%B8%AD%E9%86%AB
* 中醫笈成: https://jicheng.tw/tcm/index.html
* 中国哲学书电子化计划: https://ctext.org/wiki.pl?if=gb&remap=gb
* 古籍阁: http://gujige.com/
* 柏林国家图书馆数字化收藏: https://digital.staatsbibliothek-berlin.de/suche?results_on_page=20&current_page=1&first_page=true&last_page=false&results_count=2578&sort_on=relevance&sort_direction=desc&category%5B0%5D=Medizin&category%5B1%5D=Ostasiatische%20Handschriften
* 中医科学院 - 古今医案平台: https://tcm.ckcest.cn/
* 早稻田大学图书馆: https://waseda.primo.exlibrisgroup.com/discovery/search?vid=81SOKEI_WUNI:WINE
