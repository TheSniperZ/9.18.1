# 9.18.1
四舍五入函数

                                           2.1             2.6                -2.1               -2.6
floor : 不大于自变量的最大整数             2                2                  -3                  -3
ceil   :不小于自变量的最大整数             3                3                  -2                  -2
round:四舍五入到最邻近的整数               2                3                  -2                  -3
 
floor(),ceil() 需包含头文件<math.h>
 
C++中没有直接的round函数 需自己建立
double round(double r)
{
    return (r > 0.0) ? floor(r + 0.5) : ceil(r - 0.5);
}

你可以直接加0.5，同时将结果强制转换为整数就好了。
例如：
int i=(int)(0.45+0.5);
    i=0;
int i=(int)(0.55+0.5);
    i=1;
