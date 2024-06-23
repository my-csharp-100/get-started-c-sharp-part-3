# 使用 C# 中的 do-while 和 while 语句在代码中添加循环逻辑

|本期版本|上期版本
|:---:|:---:
`Sun Jun 23 23:14:14 CST 2024` | -

**在此质询期间管理用户输入**


* 使用 `Console.ReadLine()` 语句获取用户输入时，通常的做法是使用可为 null 的类型字符串（指定的 string?）作为输入


```c#
string? readResult;
Console.WriteLine("Enter a string:");
do
{
    readResult = Console.ReadLine();
} while (readResult == null);
```

* 方法 int.TryParse() 可用于将字符串值转换为整数。 该方法使用两个参数，一个是将计算的字符串，另一个则是将会赋值的整数变量的名称。


```c#
int numericValue = 0;
bool validNumber = false;

validNumber = int.TryParse(readResult, out numericValue);
```