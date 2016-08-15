---
title: 面试题
categories: 面试 
photos: https://ss0.bdstatic.com/94oJfD_bAAcT8t7mm9GUKT-xh_/timg?image&quality=100&size=b4000_4000&sec=1471251822&di=ab72cef2ccd91b3948507825d2892b75&src=http://b.hiphotos.baidu.com/image/pic/item/023b5bb5c9ea15cec72cb6d6b2003af33b87b22b.jpg
tags:
- interview
- 
---

## 面试题 ##

<!--more-->

###1.优化代码###
    `if(a==1) name="a1";
	else if(a==2) name="a2";
	else if(a==3) name="a3";
	else name=a0;`
自己答案：

	`name=["a1","a2","a3"];
	function(a){
	return name[a-1]||"a0";}`

###2.动态规划求和###
    1,3,5,10组合和为100，要求组合数不高于50.
贪婪解法：

	for(i=0;i<51;i++)
		for(j=0;j<34&&i+j<51;j++)
			for(k=0;k<21&&i+j+k<51;j++)
				for(m=0;m<11&&m+i+j+k<51;m++)
					if(i+3*j+5*k+10*m==100) {console.log(...);break;}
					if(...>100){break;}

					
动太规划：

    当时没来得及想，后补

因为子问题不具备无后效性，不能动态规划，但有数学公式：

    q(n)=q(n-1)+q(n-5)+q(n-1)-q(n-6)-q(n-11)-q(n-15)+q(n-16)
    q(0)=1;n<0,q(n)=0;代码：
	qmap={0:1};
	fucntion sumA(n){
	if(n==0) return 1;
	else if(n<0) return 0; 
	else if(n in qmap) return qmap[n];
	else{r=..;qmap[n]=r;}}

###3.[1,2,3,4,5].splice(1,2,3,4,5) 返回[2,3],原数组变为【1，3，4，5，4，5】

###4.考察innerHTML,setAttribute("","")

###5.考察flex布局，容器的justify-content,align-items;

###6.响应布局@meaid screen and (){}