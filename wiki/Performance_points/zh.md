# Performance points

**Performance points**（或简称**pp**）是一个评分标准，旨在准确地反映玩家在 osu! 中的水平。

它的目标是把玩家水平的焦点从游玩的时长转变为玩家技术的实际体现，而不仅仅是总[分数](/wiki/Gameplay/Score)。通过将[谱面](/wiki/Beatmap)的难度与玩家在该谱面上的表现计算得出一个特有分数来达到这一目标。

## 历史

这种分数的最初加入是2012年4月，但只是以神秘的*"???"*被人所知。这个神秘的系统最终在月内得到了它的全名。
之后被称为 "pp"（"performance points"的缩写）。这个新系统寻求的是将先前简单基于玩家总分来判断水平的标准，转变为某种更能准确反映技巧的东西。在当时该系统受到了玩家群体的广泛赞誉。

在它亮相的几个月后，官方在20120722-24 osu! release版本正式加入了这个系统，完全取代了旧的[Ranked](/wiki/Beatmap/Category#ranked)分数系统，新的分数每30分钟被计算一次。在当年的8月，该系统被改进为实时更新。

*注: ppv1，原始的 pp 系统也有一个更新日志，你可以通过它的[论坛主题](https://osu.ppy.sh/community/forums/topics/92185)查看。*

它持续了一年多的服务，直到[Tom94](https://osu.ppy.sh/users/1857058)，*osu!tp* 得分标准的创造者，加入了[osu! team](/wiki/People/The_Team) 并加入了他的设计。新系统被命名为*ppv2*，在2014年1月27日正式上线。于是旧的系统被重命名为 *[ppv1](/wiki/Performance_points/ppv1)*。

ppv2目前仍在提供服务，实时升级发布在它的[更新日志](https://osu.ppy.sh/p/changelog?category=pp)中。

## 计算

Performance points 十分依赖于计算出的谱面难度，由每个[游戏模式](/wiki/Game_mode)独立的算法决定。

玩家玩的谱面的难度决定了成绩的最终pp值。公式被设计为根据四个主要数值：**[瞄准](#瞄准)**，**[速度](#速度)**，**[准确率](#准确率)**，和**[耐力](#耐力)**。上述所有的值以不同的权重组合在一起，得到一个关于谱面特定的[难度](/wiki/Beatmap/Difficulty)，和玩家在上述谱面的个人表现。

然后分数互相"权衡"来确保只有用户的最佳成绩取得最多的pp，即[*权重系统*](#权重系统)，目的是为了防止短时间多次在简单的谱面中取得低pp成绩降低玩家最佳成绩实际得到的pp。

*注: 会根据玩过并留有成绩的Ranked谱面数量奖励少量的额外pp。*

### 权重系统

权重系统是一个在算出一次游玩的成绩的全部pp后用到的简单公式。这个公式用于根据上述游玩在玩家的最佳成绩中的排行减少得到的pp。上述的公式如下所示：

`总 pp = p * 0.95^(n-1)`

根据上述公式，*p*代表每个得分的全部pp（预权衡），*n* 是每个得分的全部pp在玩家`最佳成绩`中的排名。例如，一个玩家的前五个最佳成绩为：110pp，100pp，100pp，90pp，和80pp，权重后的分数约为110pp，95pp，90pp，77pp，和65pp。

### 瞄准

*瞄准* 是一个衡量持续击中谱面中连续的物件的难度的主要标准。

类似于 [缩圈速度](/wiki/Beatmapping/Approach_rate) 和特定的 [Mods](/wiki/Game_modifier)（即[Flashlight](/wiki/Game_modifier/Flashlight)，[Hidden](/wiki/Game_modifier/Hidden)和[Hard Rock](/wiki/Game_modifier/Hard_Rock)）使快速准确地移动光标的难度显著地提升，因此影响了成绩得到pp的数量。

在[osu!](/wiki/Game_mode/osu!)中，包含远距离[jump](/wiki/Beatmap/Pattern/Jump)的谱面的“瞄准”值会很高，于是通常得到的pp会很多。以此类推，包含很多hyperdash的[osu!catch](/wiki/Game_mode/osu!catch)谱面也会有类似的效果。瞄准在类似[osu!taiko](/wiki/Game_mode/osu!taiko) 和 [osu!mania](/wiki/Game_mode/osu!mania)的游戏模式中不会被考虑。

### 速度

*速度* 是一个代表谱面物件速度的主要标准。

短时间内包含了大量物件的谱面*速度*值很高。此时，*速度*越高，谱面难度就越高，也会得到更多的pp。

因此诸如[Double Time](/wiki/Game_modifier/Double_Time)和[Half Time](/wiki/Game_modifier/Half_Time) 等Mod会由于pp算法显著影响谱面的*速度*。

### 准确率

*又见: [准确率](/wiki/Gameplay/Accuracy)*

*准确率* 是一个权衡玩家准时击中[物件](/wiki/Hit_object)能力的百分值；它也是一项和pp算法相关的衡量玩家在谱面中某项表现的标准。

准确率高的得分会得到很多的pp。一个取得 80% 准确率并[全连](/wiki/Full_combo) 的成绩有时相当于 95% 准确率的成绩。由于算法十分依赖于准确率，如Hidden，Hard Rock和Flashlight等Mod对高准确率的成绩得到的pp会增加很多。

### 耐力

*耐力* 是一个衡量玩家面对某个谱面中高密度物件的时长和次数的主要标准。

谱面中*速度* 或难度[特征](/wiki/Beatmap/Pattern) 极高的部分将显著的增加其*耐力*值。如[串](/wiki/Beatmap/Pattern/Stream) 或者有快速连续Jump的谱面*耐力* 值会增加，从而增加谱面得到的pp。

## FAQ

### 我能在哪里查看pp排行榜？

**可以在[排行榜](https://osu.ppy.sh/p/pp)找到所有玩家的pp排行。**

你也可以通过在旧版网页的`ranking` 下拉菜单选择`performance`来查看pp排行榜。

### 我该如何提升自己的排名和pp？

**你的pp主要取决于你在每个谱面中的成绩**

提高pp的最佳办法是在高难度谱面取得好成绩，并且玩很多的谱面。

考虑以下几点建议:

- 高效地玩，找到最适合你的风格。
- 专注于得到更多高分成绩，而不是去盲目刷很多“还行”的成绩。
- 提高你的准确率。 即使是1%也能有很大差别。
- 提高连击数量。 全连（FC）或[SS](/wiki/Gameplay/Grade) 会得到大量pp。

### 为什么我没有得到游玩一个谱面的所有pp？

**pp使用一个权重系统，这意味着你的最高分数会得到所有pp的100%，以下的成绩会逐渐减少。**

更多关于权重系统详见 [上方](#权重系统).

### 多次在Ranked谱面取得成绩有多少额外pp？

**可以通过多次在Ranked谱面取得成绩得到最多416.6667额外pp。大约需要25397个成绩。**

以下这个公式可以用于计算额外pp，`N` 是取得过成绩的Ranked谱面数量：

`416.6667 * (1 - 0.9994 ^ N)`

达到这个限制的一半大约需要1555个成绩。如你所见，随着你接近这个限制，需要的分数数量将会越来越多。

### 我玩简单的谱面得不到pp是因为权重系统吗？

**综上所述，旧的成绩的权重将逐渐减少至不到1%。这意味着随着你的进步，它们几乎不算在你的总成绩内。**

到那时，你一定会取得一些很高的成绩，也就是说你的pp会随着得到的高分逐渐超过之前的。

### 为什么我得到了新成绩pp反而减少了？

**你可能会偶尔因为取得的分数更高但准确率更低的成绩而失去pp，或者用了Mod后总体准确率降低。**

总分对单个谱面的排行仍然很重要，这就造成了很少情况下总分更高而准确率更低，或因为Mod的加成产生了一个“更好”的成绩而使你失去pp。

### 为什么我觉得有些Mod比重太高/太低了？

**这最有可能是你的主观感觉。**

没有绝对完美的系统，不同谱面集和Mod组合的总pp一定是不同的，即使这个谱面的主观难度可能比难度更高的谱面低。

总体来说，现在的pp系统已经是尽可能的公平了，受限于它目前的模型。
