
<font color='red'> **微信搜索公众号【C you again】:**

- [**回复 ：<font color='green'>“浙大版C语言”</font> 查看本题目实现过程和详细解答** ](  http://gzh.cyouagain.cn/) 
 
- [ **回复 ：<font color='green'>“编程交流群”</font>” 进C/C++/Java编程题交流、问题解答群，和大佬一起进步**  ](  http://cyouagain.cn/    ) 




## 习题10-6 递归求Fabonacci数列

本题要求实现求Fabonacci数列项的函数。Fabonacci数列的定义如下：

f(n)=f(n−2)+f(n−1) (n≥2)，其中f(0)=0，f(1)=1。

**函数接口定义：**

> int f( int n );

函数<font color="red"> f </font>应返回第<font color="red"> n </font>个Fabonacci数。题目保证输入输出在长整型范围内。建议用递归实现。

**裁判测试程序样例：**

    #include <stdio.h>
    
    int f( int n );
    
    int main()
    {
        int n;
    
        scanf("%d", &n);
        printf("%d\n", f(n));
    
        return 0;
    }
    
    /* 你的代码将被嵌在这里 */

**输入样例：**

> 6

**输出样例：**

> 8

**代码：**

```c
int f( int n )
{
    if(n==0||n==1) return n;
    //else if(n==1) return 1;
    else
    {
        return f(n-2)+f(n-1);
    }
}
```



