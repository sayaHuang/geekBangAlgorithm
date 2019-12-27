[TOC]

# 训练环境设置,编码技巧 code style

##mac的iterm2+zsh+oh-my-zsh
googel 搜索关键字`iterm2+zsh+oh-my-zsh` 选择第一个搜索结果(需要打开VPN)
* iterm2参考安装连接: https://medium.com/ayuth/iterm2-zsh-oh-my-zsh-the-most-power-full-of-terminal-on-macos-bdb2823fb04c 
* zsh+oh-my-zsh的插件安装教程  https://juejin.im/entry/5ae00e54f265da0b8635ea5c

NOTE: 设置 google浏览器为默认浏览器

##给IntelliJ IDEA 添加Leetcode插件
###安装方法:
路径: IntelliJ IDEA -> Preferences -> Plugins;
https://blog.csdn.net/qq_35246620/article/details/78289074

###使用leetcode方法
https://plugins.jetbrains.com/plugin/12132-leetcode-editor

https://zhuanlan.zhihu.com/p/60309695

##自定向下的变成方式
拿到一个带实现的功能的时候, 考虑具体需要几步完成该能, 编写思路. 更具思路完成代码的编写.
该死路出自 `clean code` 
request:
> 给定一个字符串，验证它是否是回文串，只考虑字母和数字字符，可以忽略字母的大小写。
说明：本题中，我们将空字符串定义为有效的回文串。

示例1:
```java
输入: "A man, a plan, a canal: Panama"
输出: true
```
示例1:
```java
输入: "race a car"
输出: false
```

step 1:
```java
    //本题中，我们将空字符串定义为有效的回文串。
    //1.过滤文本中,只保留字符和数字
    //2.反转文本
    //3.对比文本
```

step2:
```java
    //本题中，我们将空字符串定义为有效的回文串。
    //1.过滤文本中,只保留字符和数字
    //2.反转文本
    //3.对比文本
    public boolean isPalindrome(String s) {
        String filterS = filterStringNumber(s);
        String reverseS = reverseString(filterS);
        return reverseS.equalsIgnoreCase(filterS);
    }

    private String reverseString(String filterS) {
        return null;
    }

    private String filterStringNumber(String s) {
        return null;
    }
```

step3: 完善功能
```java
		public static boolean isPalindrome(String s) {
        String filterS = filterStringNumber(s);
        String reverseS = reverseString(filterS);
        return reverseS.equalsIgnoreCase(filterS);
    }

    private static String reverseString(String filterS) {
        return new StringBuilder(filterS).reverse().toString();
    }

    private static String filterStringNumber(String input) {
        return input.replaceAll("[^a-zA-Z0-9&]", "");
    }
```
leetcode address: https://leetcode-cn.com/problems/valid-palindrome/submissions/
###clean code book review
参考连接: https://markhneedham.com/blog/2008/09/15/clean-code-book-review/


