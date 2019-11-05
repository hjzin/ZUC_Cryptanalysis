# ZUC_Cryptanalysis

密码学作业3：ZUC算法的密码分析

1910210403 胡兆杰



## 问题1：实现ZUC的差分分析表(DDT)和线性逼近表(LAT)

- Code：源代码文件[ZUC_cryptanalysis.py](https://github.com/hjzin/ZUC_Cryptanalysis/blob/master/Code/ZUC_cryptanalysis.py)
- output目录是输出的差分分析表和线性逼近表，共有四个excel文件
- [ZUC密码实验.pdf]([https://github.com/hjzin/ZUC_Cryptanalysis/blob/master/ZUC%E5%AF%86%E7%A0%81%E5%88%86%E6%9E%90%E5%AE%9E%E9%AA%8C.pdf](https://github.com/hjzin/ZUC_Cryptanalysis/blob/master/ZUC密码分析实验.pdf)) ：实验思路和结果文档



## 问题2：为什么最后还需要进行异或轮密钥操作？

以SPN(Substitution - Permutation)为例，其计算框图如下所示。

![](https://tva1.sinaimg.cn/large/006y8mN6ly1g8n66ck5i9j30js0wkdgg.jpg)

如图可以看到，该密码的第一步和最后一步都是异或轮密钥。这样就保证了攻击者在不知道密钥的情况下无法开始加密和解密操作。如果没有这一步的话，那么攻击者拿到密文即可通过S盒进行第一步解密，增加了密码被破解的风险。