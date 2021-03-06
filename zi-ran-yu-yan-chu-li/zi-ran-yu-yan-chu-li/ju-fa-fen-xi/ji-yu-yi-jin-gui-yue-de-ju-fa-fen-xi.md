# 基于移进-归约的句法分析

移进—归纳方法（Shift—Reduce Algorithm）是一种自下而上的方法。其从输入串开始，逐步进行“归约”，指导归约到文法的开始符号。移进—归纳算法类似于下推自动机的LR分析法，其操作的基本数据结构是堆栈。

移进—归纳算法主要涉及四种操作（这里符号 $$S$$ 表示句法树的根节点）。

1）移进：从句子左端将一个终结符移到栈顶。

2）归约：根据规则，将栈顶的若干个字符替换为一个符号。

3）接受：句子中所有词语都已移进栈中，且栈中只剩下一个符号 $$S$$ ，分析成功，结束。

4）拒绝：句子中所有词语都已移进栈中，栈中并非只有一个符号 $$S$$ ，也无法进行任何归约操作，分析失败，结束。

