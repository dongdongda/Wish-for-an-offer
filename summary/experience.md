md文件是我用markdown做的，推荐给大家，特别适合用来做笔记和写博客展示啥的。

网址：`markdown.com.cn`

## 1. 正式秋招前
### 1.1 确定技术栈
先考虑是否技术岗还是非技术岗吧。以下都是默认技术岗了。

目前主流的是C++和Java，其中Java目前来看岗位更广，但是也比较卷；C++的话面稍窄一点，主要是后台开发、游戏研发、嵌入式开发；还有新兴的go语言其实也可以，目前趋势很不错。

目前拿offer难度是前端<客户端<后台吧，当然越难的以后的发展平均下来肯定也更好，这都是市场规律。


### 1.2 基础学习

普遍适用的就是：
- 语言（c++/java）
- 计算机网络
- 操作系统
- 数据库
- 数据结构和算法题

还有一些和岗位相关的有余力再针对性的学。

至于具体的学习，需要你自己有一些信息搜集获取的能力。

### 1.3 尽可能的实习！！！

三个感叹号，自己体会。

但总还是有想我这样的进了坑不能实习的。只有自己提前准备，基础学的更牢固，项目自己找开源的做吧，最好能把握细节（当然也比较难）。



## 2 相关资料

### 2.1 几个好的网站

必备的
- `https://www.nowcoder.com/`
             
（牛客网，笔试面试面积招聘综合）
 - `https://leetcode-cn.com/`
             
  （leetcode，刷题） 

基础知识及综合
- `https://interviewguide.cn/#/`                
（C++强推）
- `https://imageslr.com/`

刷题相关
- `https://codetop.cc/home`

（按部门和岗位真实出现频次排序，强推）
- `https://www.algomooc.com/`
### 2.2 秋招信息获取

我目前接触到的主要有以下渠道

- 学校的：北京邮电大学就业信息网、北邮就业创业微信公众号、论坛
- offershow：关注校招薪水公众号，进大群可以获取很多公司的秋招信息
- 自己关注的公司的官网

## 3 笔试

### 3.1 笔试的意义

大公司简历会很多，就会用笔试筛人，有的很重视必须好好做；有的就是更看面试一些。
不管怎么说，笔试更高总是有些优势的，所以还是好好准备吧，

### 3.1 笔试的一些注意事项

- 提前熟悉笔试环境，一般是牛客，但也有别的
- 有的公司运行使用本地IDE，有的不允许，这个要注意
- 一定要注意输入输出，有的题要自己定义好输入输出而不是LeetCode上直接写函数就行，这个自己提前准备好各种输入输出怎么写，下面给出两个例子：


```
/* 第一行输入t代表t个测试用例，第二、三行分别输入一个n和n个数，以此类推。*/
#include <iostream>
#include <vector>
using namespace std;

int main()
{
	int t = 0;
	cin >> t;
	int num = 0;
	vector<int> n;
	vector<int> res;
	vector<vector<int>> a;
	for (int i = 0; i < t; i++)
	{
		cin >> num;
		n.push_back(num);
		a.push_back(vector<int>());
		for (int j = 0; j < n[i]; j++)
		{
			cin >> num;
			a[i].push_back(num);
		}
	}

	for (int i = 0; i < t; i++)
	{
		cout << n[i] << endl;;
		for (int j = 0; j < n[i]; j++)
		{	
			cout << a[i][j]<<endl;
		}

	}

}
```


```
/*输入不确定行数字，每行不确定个数*/
#include <iostream>
#include <vector>
#include<sstream>
using namespace std;

int main()
{
	string str; //接收带空格的字符串
	int num; //读入的数
	vector<int> v; //一维数组存一行数
	vector<vector<int> > nums; //二维数组存多行数
	while (getline(cin, str))
	{
		istringstream iss(str);//从str中读入字符
		v.clear();

		while (iss >> num)
		{
			v.push_back(num);
		}
		nums.push_back(v);
	}
	for (int i = 0; i < nums.size(); ++i)
	{
		for (int j = 0; j < nums[i].size(); ++j)
		{
			cout << nums[i][j] << " ";
		}
		cout << endl;
	}
}
```

### 3.1 笔试其它

我会在另外的文件夹下更新一些我认为比较好比较经典的题目。


## 4 面试

面试的话不同面试官风格可能不一样，总结下来就一些几点吧：

- 八股文基础（可能从一个点深挖）
- 项目（可能会深挖细节，会问你难点以及你的解决思路）
- 和岗位或者你本人相关的经历

我会在另外的文件夹下更新一些面经和面试常考题。
