# Entity-Search
## 1.什么是Entity_Search

Entity_Search能够帮助你从海量的实体-概念对(如包子-食物)文本中，查找你所提出的概念(如“金融”)所对应的实体。当然，如果文本的标记质量足够高，那么
工作将非常简单：只需要找出所有对应标记中存在“金融”的实体就可以了。但百科的编写者们常常没有一个统一的标准：他们可能会给“汇丰银行”标上“货币”、“经济”、
“银行”...但就是忘了标上“金融”。这种情况并不少见，而Entity_Search所能做的，就是帮助你找出这些隐藏的实体。

## 2.Entity_Search是如何工作的

回到之前的例子，尽管“汇丰银行”并没有被标上“金融”的标签，但它有“货币”、“经济”等标签，这些标签与金融具有非常紧密的关系(很多时候，也是从属关系)，以至于
我们可以认为有“货币”或“经济”标签的实体都应该被找到。因此，找到这些与核心概念“金融”关系密切的拓展标签就是任务的关键。

首先，我们自然需要找出所有标有核心概念“金融”的实体。这些实体的标签集合(我们称之为“拓展标签”)中，有许多可能与“金融” 有关，而更多则是无关紧要的。
区别这两者的重要依据，是在这些拓展标签对应的实体中，有多少实体的标记包括核心概念“金融”。举例来说在实际
搜索过程中，
