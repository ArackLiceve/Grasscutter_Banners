# Grasscutter_Banners|割草机卡池文件

Json file collection for Grasscutter gacha Banners

收集割草机的卡池Json文件

to use the banners, select the one you want to use and place it inside "grasscutter/data" folder on your server installation.

要使用这些卡池文件，请选择任意一个下载下来然后放在“grasscutter/data”文件夹里面。

Remember to rename it to "Banners.json"

记得把文件重命名为“Banners.json”

Use "/reload" command in game to reload the banners.

你可以在游戏中使用"/reload"命令来重新加载卡池配置文件。

You're all welcome to submit a pull request and make a change on the project.

欢迎提交pr！


## Thanks|鸣谢:

[https://github.com/davidbeltrane01/grasscutters_banners_json](https://github.com/davidbeltrane01/grasscutters_banners_json)

[https://github.com/KeyPJ/genshin-gacha-banners](https://github.com/KeyPJ/genshin-gacha-banners)

[https://github.com/Grasscutters/Grasscutter](https://github.com/Grasscutters/Grasscutter)

[https://github.com/jie65535/GrasscutterCommandGenerator](https://github.com/jie65535/GrasscutterCommandGenerator)

## 后记：

修卡池的时候发现了一些经验。

如果卡池出现类似A022的字样不正常的时候，可能是gachaType写错了，需要修改正确之后才能显示。

以下是我尝试之后的可能结果，可能不一定准确但是这样确实外表看上去就是对的


>100 初行祈愿

>200 常驻祈愿

>301 角色活动祈愿1

>302 武器活动祈愿

>400 角色活动祈愿2


另外gachaType写对之后还可能出现卡池的标题消失的情况，这时候可能是titlePath的编号不对导致的。

比如2.1上半

"prefabPath":"GachaShowPanel_A054",

"titlePath":"UI_GACHA_SHOW_PANEL_A020_TITLE",

这里的titlePath里面必须是A020才能正确显示出“神铸赋形”这个武器池的标题，如果惯性思维还是填A054的话会导致标题区域空白

（众所周知prefabPath是控制卡池封面的，titlePath是控制卡池标题的）

### 后续发现了一些规律：
关于卡池prefabPath代号和titlePath的规律：

A016初行祈愿，A017原神1.0常驻池，A022常驻池

除了这三个卡池外大致遵循以下规律：

①每个大版本的卡池为连续的prefabPath编号，prefabPath编号和上一个版本的最后一个prefabPath编号是接着的

②2.3版本之前编号按照上半角色-下半角色-上半武器-下半武器的顺序。2.3版本第一次加入角色活动祈愿2，大致也是之前的规律，
2.3之后的版本顺序变成了上半角色-上半武器-下半角色-下半武器。如果有两个角色up则先为角色活动祈愿1再编号角色活动祈愿2

③有关titlePath，如果是武器池的titlePath都是一样的A020（武器池的标题全都是神铸赋形），角色池看是不是第一次up，如果是第一次up则与prefabPath的编号保持一致，如果是复刻则与该角色第一次up的prefabPath保持一致
此外，如果编号大于100，titlePath需要多加一个0，比如妮露的prefabPath是A100，那她的titlePath是A0100而不是A100

以下是总结出的表格：
titlePath留空表示是首次up，值与prefabPath一致（100以后的编号需要在前面加一个0）
| prefabPath | titlePath | 五星up          | 卡池类型 | gachaType | 版本号   |
|------------|-----------|-----------------|----------|-----------|-------|
| Default    | Default   |                 |  施工中  |           |       |
| A016       |           | 初行祈愿          | 初行   | 100       | 1.0.1 |
| A017       |           | 常驻卡池          | 常驻   | 200       | 1.0.1 |
| A018       |           | 可莉            | 角色1  | 301       | 1.0.2 |
| A019       |           | 温迪            | 角色1  | 301       | 1.0.1 |
| A020       | A020      | 阿莫斯/风鹰剑       | 武器   | 302       | 1.0.1 |
| A021       | A020      | 四风原典/狼末       | 武器   | 302       | 1.0.2 |
| A022       |           | 常驻卡池          | 常驻   | 200       | 1.1.1 |
| A023       |           | 达达利亚          | 角色1  | 301       | 1.1.1 |
| A024       |           | 钟离            | 角色1  | 301       | 1.1.2 |
| A025       | A020      | 天空之翼/尘世之锁     | 武器   | 302       | 1.1.1 |
| A026       | A020      | 贯虹/无工         | 武器   | 302       | 1.1.2 |
| A027       |           | 阿贝多           | 角色1  | 301       | 1.2.1 |
| A028       |           | 甘雨            | 角色1  | 301       | 1.2.2 |
| A029       | A020      | 斫峰之刃/天空之卷     | 武器   | 302       | 1.2.1 |
| A030       | A020      | 阿莫斯/天空之傲      | 武器   | 302       | 1.2.2 |
| A031       |           | 魈             | 角色1  | 301       | 1.3.1 |
| A032       |           | 刻晴            | 角色1  | 301       | 1.3.2 |
| A033       |           | 胡桃            | 角色1  | 301       | 1.3.3 |
| A034       | A020      | 磐岩结绿/和璞鸢      | 武器   | 302       | 1.3.1 |
| A035       | A020      | 护摩/狼末         | 武器   | 302       | 1.3.3 |
| A036       | A019      | 温迪            | 角色1  | 301       | 1.4.1 |
| A037       | A023      | 达达利亚          | 角色1  | 301       | 1.4.2 |
| A038       | A020      | 终末/天空之刃       | 武器   | 302       | 1.4.1 |
| A039       | A020      | 天空之翼/四风原典     | 武器   | 302       | 1.4.2 |
| A040       | A024      | 钟离            | 角色1  | 301       | 1.5.1 |
| A041       |           | 优菈            | 角色1  | 301       | 1.5.2 |
| A042       | A020      | 斫峰之刃/尘世之锁     | 武器   | 302       | 1.5.1 |
| A043       | A020      | 松籁/风鹰剑        | 武器   | 302       | 1.5.2 |
| A044       | A018      | 可莉            | 角色1  | 301       | 1.6.1 |
| A045       |           | 万叶            | 角色1  | 301       | 1.6.2 |
| A046       | A020      | 四风原典/天空之傲     | 武器   | 302       | 1.6.1 |
| A047       | A020      | 天空之卷/苍古       | 武器   | 302       | 1.6.2 |
| A048       |           | 神里绫华          | 角色1  | 301       | 2.0.1 |
| A049       |           | 宵宫            | 角色1  | 301       | 2.0.2 |
| A050       | A020      | 雾切/天空之脊       | 武器   | 302       | 2.0.1 |
| A051       | A020      | 飞雷/天空之刃       | 武器   | 302       | 2.0.2 |
| A052       |           | 雷电将军          | 角色1  | 301       | 2.1.1 |
| A053       |           | 珊瑚宫心海         | 角色1  | 301       | 2.1.2 |
| A054       | A020      | 无工/薙刀         | 武器   | 302       | 2.1.1 |
| A055       | A020      | 月华/磐岩结绿       | 武器   | 302       | 2.1.2 |
| A056       | A023      | 达达利亚          | 角色1  | 301       | 2.2.1 |
| A057       | A033      | 胡桃            | 角色1  | 301       | 2.2.2 |
| A058       | A020      | 冬极/尘世之锁       | 武器   | 302       | 2.2.1 |
| A059       | A020      | 护摩/终末         | 武器   | 302       | 2.2.2 |
| A060       | A027      | 阿贝多           | 角色1  | 301       | 2.3.1 |
| A061       |           | 荒泷一斗          | 角色1  | 301       | 2.3.2 |
| A062       | A041      | 优菈            | 角色2  | 400       | 2.3.1 |
| A063       | A020      | 苍古/松籁         | 武器   | 302       | 2.3.1 |
| A064       | A020      | 赤角石溃杵/天空之翼    | 武器   | 302       | 2.3.2 |
| A065       |           | 申鹤            | 角色1  | 301       | 2.4.1 |
| A066       | A031      | 魈             | 角色2  | 400       | 2.4.1 |
| A067       | A020      | 息灾/和璞鸢        | 武器   | 302       | 2.4.1 |
| A068       | A024      | 钟离            | 角色1  | 301       | 2.4.2 |
| A069       | A028      | 甘雨            | 角色2  | 400       | 2.4.2 |
| A070       | A020      | 贯虹/阿莫斯        | 武器   | 302       | 2.4.2 |
| A071       |           | 八重神子          | 角色1  | 301       | 2.5.1 |
| A072       | A020      | 神乐/磐岩结绿       | 武器   | 302       | 2.5.1 |
| A073       | A052      | 雷电将军          | 角色1  | 301       | 2.5.2 |
| A074       | A053      | 珊瑚宫心海         | 角色2  | 400       | 2.5.2 |
| A075       | A020      | 薙刀/月华         | 武器   | 302       | 2.5.2 |
| A076       |           | 神里绫人          | 角色1  | 301       | 2.6.1 |
| A077       | A019      | 温迪            | 角色2  | 400       | 2.6.1 |
| A078       | A020      | 终末/月白         | 武器   | 302       | 2.6.1 |
| A079       | A048      | 神里绫华          | 角色1  | 301       | 2.6.2 |
| A080       | A020      | 雾切/无工         | 武器   | 302       | 2.6.2 |
| A081       |           | 夜兰            | 角色1  | 301       | 2.7.1 |
| A082       | A031      | 魈             | 角色2  | 400       | 2.7.1 |
| A083       | A020      | 若水/和璞鸢        | 武器   | 302       | 2.7.1 |
| A084       | A061      | 荒泷一斗          | 角色1  | 301       | 2.7.2 |
| A085       | A020      | 赤角石溃杵/尘世之锁    | 武器   | 302       | 2.7.2 |
| A086       | A045      | 万叶            | 角色1  | 301       | 2.8.1 |
| A087       | A018      | 可莉            | 角色2  | 400       | 2.8.1 |
| A088       | A020      | 苍古自由之誓/四风原典   | 武器   | 302       | 2.8.1 |
| A089       | A049      | 宵宫            | 角色1  | 301       | 2.8.2 |
| A090       | A020      | 飞雷之弦振/斫峰之刃    | 武器   | 302       | 2.8.2 |
| A091       |           | 提纳里           | 角色1  | 301       | 3.0.1 |
| A092       | A024      | 钟离            | 角色2  | 400       | 3.0.1 |
| A093       | A020      | 猎人之径/贯虹之槊     | 武器   | 302       | 3.0.1 |
| A094       | A028      | 甘雨            | 角色1  | 301       | 3.0.2 |
| A095       | A053      | 心海            | 角色2  | 400       | 3.0.2 |
| A096       | A020      | 阿莫斯之弓/不灭月华    | 武器   | 302       | 3.0.2 |
| A097       |           | 赛诺            | 角色1  | 301       | 3.1.1 |
| A098       | A019      | 温迪            | 角色2  | 400       | 3.1.1 |
| A099       | A020      | 终未嗟叹之诗/赤沙之杖   | 武器   | 302       | 3.1.1 |
| A100       |           | 妮露            | 角色1  | 301       | 3.1.2 |
| A101       | A027      | 阿贝多           | 角色2  | 400       | 3.1.2 |
| A102       | A020      | 圣显之钥/磐岩结绿     | 武器   | 302       | 3.1.2 |
| A103       |           | 纳西妲           | 角色1  | 301       | 3.2.1 |
| A104       | A049      | 宵宫            | 角色2  | 400       | 3.2.1 |
| A105       | A020      | 千夜浮梦/飞雷之弦振    | 武器   | 302       | 3.2.1 |
| A106       | A071      | 八重神子          | 角色1  | 301       | 3.2.2 |
| A107       | A023      | 达达利亚          | 角色2  | 400       | 3.2.2 |
| A108       | A020      | 神乐之真意/冬极白星    | 武器   | 302       | 3.2.2 |
| A109       |           | 流浪者           | 角色1  | 301       | 3.3.1 |
| A110       | A061      | 荒泷一斗          | 角色2  | 400       | 3.3.1 |
| A111       | A020      | 图莱杜拉的回忆/赤角石溃杵 | 武器   | 302       | 3.3.1 |
| A112       | A052      | 雷电将军          | 角色1  | 301       | 3.3.2 |
| A113       | A076      | 神里绫人          | 角色2  | 400       | 3.3.2 |
| A114       | A020      | 波乱月白经津/薙草之稻光  | 武器   | 302       | 3.3.2 |
| A115       |           | 艾尔海森          | 角色1  | 301       | 3.4.1 |
| A116       | A031      | 魈             | 角色2  | 400       | 3.4.1 |
| A117       | A020      | 裁叶萃光/和璞鸢      | 武器   | 302       | 3.4.1 |
| A118       | A033      | 胡桃            | 角色1  | 301       | 3.4.2 |
| A119       | A082      | 夜兰            | 角色2  | 400       | 3.4.2 |
| A120       | A020      | 若水/护摩之杖       | 武器   | 302       | 3.4.2 |
| A121       |           | 迪希雅           | 角色1  | 301       | 3.5.1 |
| A122       | A097      | 赛诺            | 角色2  | 400       | 3.5.1 |
| A123       | A020      | 苇海信标/赤沙之杖     | 武器   | 302       | 3.5.1 |
| A124       | A065      | 申鹤            | 角色1  | 301       | 3.5.2 |
| A125       | A048      | 神里绫华          | 角色2  | 400       | 3.5.2 |
| A126       | A020      | 雾切之回光/息灾      | 武器   | 302       | 3.5.2 |
| A127       | A0103     | 纳西妲       | 角色1   | 301       | 3.6.1 |
| A128       | A0100     | 妮露      | 角色2   | 400       | 3.6.1 |
| A129       | A020      | 千夜浮梦/圣显之钥      | 武器   | 302       | 3.6.1 |
| A130       |           | 白术      | 角色1   | 301       | 3.6.2 |
| A131       | A028      | 甘雨      | 角色2   | 400       | 3.6.2 |
| A132       | A020      | 碧落之珑/阿莫斯之弓      | 武器   | 302       | 3.6.2 |
| A133       | A049      | 宵宫          | 角色1   | 301       | 3.7.1 |
| A134       | A071      | 八重神子      | 角色2   | 400       | 3.7.1 |
| A135       | A020      | 飞雷之弦振/神乐之真意      | 武器   | 302       | 3.7.1 |
| A136       | A0115     | 艾尔海森      | 角色1   | 301       | 3.7.2 |
| A137       | A045      | 枫原万叶      | 角色2   | 400       | 3.7.2 |
| A138       | A020      | 苍古自由之誓/裁叶萃光      | 武器   | 302       | 3.7.2 |
| A139       | A041      | 优菈      | 角色1   | 301       | 3.8.1 |
| A140       | A018      | 可莉      | 角色2   | 400       | 3.8.1 |
| A141       | A020      | 松籁响起之时/四风原典      | 武器   | 302       | 3.8.1 |
| A142       | A053      | 珊瑚宫心海      | 角色1   | 301       | 3.8.2 |
| A143       | A0109     | 流浪者      | 角色2   | 400       | 3.8.2 |
| A144       | A020      | 不灭月华/图莱杜拉的回忆      | 武器   | 302       | 3.8.2 |
| A145       |           | 林尼      | 角色1   | 301       | 4.0.1 |
| A146       | A081      | 夜兰      | 角色2   | 400       | 4.0.1 |
| A147       | A020      | 最初的大魔术/若水      | 武器   | 302       |4.0.1|

>以下为预测内容

| prefabPath | titlePath | 五星up        | 卡池类型 | gachaType | 版本号   |
|------------|-----------|---------------|------|-----------|-------|
| A148       | A024      | 钟离      | 角色1   | 301       | 4.0.2 |
| A149       | A023      | 公子     | 角色2   | 400       |4.0.2 |
| A150       | A020      | 贯虹之槊/冬极白星      | 武器   | 302       | 4.0.2 |
| A151       |           | 莱欧斯利      | 角色1   | 301       | 4.1.1 |
| A152       | A019      | 温迪     | 角色2   | 400       |4.1.1 |
| A153       | A020      | 金流监督/终未嗟叹之诗      | 武器   | 302       | 4.1.1 |
| A154       |           | 那维莱特      | 角色1   | 301       | 4.1.2 |
| A155       | A033      | 胡桃     | 角色2   | 400       |4.1.2 |
| A156       | A020      | 万世流涌大典/护摩之杖      | 武器   | 302       | 4.1.2 |
| A157       | A076      | 神里绫人      | 角色1   | 301       | 4.2.1 |
| A158       | A0130     | 白术     | 角色2   | 400       |4.2.1 |
| A159       | A020      | 波乱月白经津/碧落之珑      | 武器   | 302       | 4.2.1 |
| A160       |           | 芙宁娜      | 角色1   | 301       | 4.2.2 |
| A161       | A097      | 赛诺     | 角色2   | 400       |4.2.2 |
| A162       | A020      | ???/赤沙之杖      | 武器   | 302       | 4.2.2 |


附每个角色第一次up的代号
```shell
Venti:019
Klee:018
Tartaglia:023
Zhongli:024
Albedo:027
Ganyu:028
Xiao:031
Keqing:032
Hu Tao:033
Eula:041
Kaedehara Kazuha:045
Kamizato Ayaka:048
Yoimiya:049
Raiden Shogun:052
Sangonomiya Kokomi:053
Arataki Itto:061
Shenhe:065
Yae Miko:071
Kamisato Ayato:076
Yelan:081
Tighnari:091
Cyno:097
Nilou:100
Nahida:103
Wanderer:109
Alhaitham:115
Dehya:121
Baizhu:130
Lyney:145
Neuvllette:
Wriothesley:
Furina:
```

## 关于测试服卡池：
最近测试CBT2的时候就在想正式服的卡池是从A016开始编号的，那之前的编号是不是就是测试服的？
果不其然，我在CBT2中发现了一些影子。
以下是在CBT2（0.7.1版本）中测试好的卡池。

其中有一些`扭蛋预览Prefab路径`是可以直接填角色的英文名的，比如`UI_Tab_GachaShowPanel_Xiao`和`UI_Tab_GachaShowPanel_A003`都能正常显示魈的卡池预览

| 扭蛋Prefab路径 | 扭蛋预览Prefab路径 | 五星up          | 四星up | 备注 |
|------------|-----------|---------------|------|-----|
|GachaShowPanel_A008|	UI_Tab_GachaShowPanel_Diluc | | | 奔行世间（常驻）|
|GachaShowPanel_A007|	UI_Tab_GachaShowPanel_Noel |  | 诺艾尔 | 新手祈愿 |
|GachaShowPanel_A006| | | | 卡池和预览都是空的 |
|GachaShowPanel_A005|	UI_Tab_GachaShowPanel_A005 | | | 迪卢克头像但是没卡池|
|GachaShowPanel_A004|	UI_Tab_GachaShowPanel_A004 | 钟离 | 凝光 | 斗转星移 |
|GachaShowPanel_A003|	UI_Tab_GachaShowPanel_Xiao | 魈 | 北斗 | 靖妖降魔 |
|GachaShowPanel_A002|	UI_Tab_GachaShowPanel_Venti | 温迪 | 雷泽 | 北风的诗篇 |
|GachaShowPanel_A001|	UI_Tab_GachaShowPanel_A001 | 琴/迪卢克 | | 新的旅程 普通祈愿（内测） |

