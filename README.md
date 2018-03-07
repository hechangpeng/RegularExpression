---
title: Java常见的正则表达式匹配
date: 2017-10-24 15:04:00
tags:
categories: Java
---
<img src="http://owiq5fnuk.bkt.clouddn.com/0new.jpg"/>
正则表达式的作用无处不在，可以替代我们平常的字符串遍历操作，效率上有很大的提升，网络爬虫爬取数据也会用到正则表达式。<!--more-->

/** 手机号码 */
String telPhone = "1[3|5|4|8][0-9]{9}";

/** 中文 */
String chinese = "[\u4e00-\u9fa5]";

/** 邮箱 */
String email = "[a-zA-Z0-9_-]+@\\w+\\.[a-z]+(\\.[a-z]+)?";

/** 数字 */
String digits = "[0-9]";

/** 英文字母 */
String enWord = "[a-zA-Z]";

String temp = "热烈庆祝中国共产党第19届全国代表大会胜利召开";

Pattern pattern = Pattern.compile(enWord);

Matcher m = pattern.matcher(temp);

while (m.find()) {

    System.out.println(m.group());
	
}