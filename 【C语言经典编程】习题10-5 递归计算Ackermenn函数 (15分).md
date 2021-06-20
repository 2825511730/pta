
<font color='red'> **微信搜索公众号【C you again】:**

- [**回复 ：<font color='green'>“浙大版C语言”</font> 查看本题目实现过程和详细解答** ](  http://gzh.cyouagain.cn/) 
 
- [ **回复 ：<font color='green'>“编程交流群”</font>” 进C/C++/Java编程题交流、问题解答群，和大佬一起进步**  ](  http://cyouagain.cn/    ) 

## 习题10-5 递归计算Ackermenn函数

本题要求实现Ackermenn函数的计算，其函数定义如下：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190418170149343.png)
**函数接口定义：**

> int Ack( int m, int n );

其中<font color="red"> m </font>和<font color="red"> n </font>是用户传入的非负整数。函数<font color="red"> Ack </font>返回Ackermenn函数的相应值。题目保证输入输出都在长整型范围内。

**裁判测试程序样例：**

    #include <stdio.h>
    
    int Ack( int m, int n );
    
    int main()
    {
        int m, n;
    
        scanf("%d %d", &m, &n);
        printf("%d\n", Ack(m, n));
    
        return 0;
    }
    
    /* 你的代码将被嵌在这里 */

**输入样例：**

> 2 3

**输出样例：**
> 9

**代码：**

```c
int Ack( int m, int n )
{
    if(m==0) return n+1;
    else
    {
        if(n==0&&m>0) return Ack(m-1,1);
        if(n>0&&m>0) return Ack(m-1,Ack(m,n-1));
    }
}
```


