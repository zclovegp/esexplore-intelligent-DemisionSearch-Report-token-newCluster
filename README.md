# esexplore-intelligent-DemisionSearch-Report-token-newCluster
已经迁移到物理机ES，搜索内容有指标专题报告，支持业务维度搜索

现在搜索逻辑：

1.有输入搜索词：的主要分为入es的分词和搜索词的分词,对于使用IK分词的中文分词，目前基于远程词库，包含1万个以上的指标，7个层级维度，IP
是http://10.249.216.109:9191/dic/read

2.没有输入搜索词：在es的日志索引中通过用户id统计用户对产品点击量,然后对matchAll(es)或者select(oracle)进行按照点击量排序返回结果
