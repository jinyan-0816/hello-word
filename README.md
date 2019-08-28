# hello-word
s=input("亲输入字符串:")
print("您输入的字符串:",s)

# 练习：
# 1. 今天是小明20周岁的生日，假设每年365天，计算他过了多少个星期，余多少天
a=int(input("亲输入小明的年纪："))
b=365
c=7
print("今天是小明",a,"周岁的生日，他过了",a*b//c,"个星期，余",a*b%c,"天")

# 2. 分三次输入当前的小时，分钟,秒数,在终端打印已距离凌晨 0:0:0过了多少秒?
d=int(input("亲输入当前的小时："))
e=int(input("亲输入当前的分钟："))
g=int(input("亲输入当前的秒数："))
print("距离凌晨 0:0:0过了",d*360+e*60+g,"秒")

# 练习：
#   任意输入一个数:
#   1. 判断这个数是否大于100
#   2. 判断这个数是否小于0
#   3. 判断这个数是否在20 ~ 50之间
s=input("请输入一个数：")
n=int(s)
if n>100:
	print("这个数大于100")
elif n<0:
	print("这个数小于0")
elif 20<n<50:
	print("这个数在20 ~ 50之间")

# 练习:
#   1. 输入个季度 1~4 输出这个季度有哪儿几个月，如果输入不是1~4的数，提示用户您的输入有误！
month=int(input(" 输入一个季度(1~4):"))
if month==1:
	print("该季度有一月，二月，三月")
elif month==2:
	print("该季度有四月，五月，六月")
elif month==3:
	print("该季度有七月，八月，九月")
elif month==4:
	print("该季度有十月，十一月，十二月")
else:
	print("输入有误！")

#   2. 输入一年中的月份(1~12), 输出这个月在哪儿个季度，如果输入的是其它数，提示您的输入有误!
month=int(input("输入一年中的月份(1~12):"))
if month<=3:
	print("春天来了")
elif month<=6:
	print("夏天来了")
elif month<=9:
	print("秋天来了")
elif month<=12:
	print("冬天来了")
else:
	print("输入有误！")

# 练习：
#   输入一个学生的成绩(0~100),判断这个学生的成绩是优（90~100），良(80~89)，及格(60~79)，不及格，成绩不合法5种状态
grade=int(input("输入一个学生的成绩(0~100):"))
if 0<=grade<=100:
	if grade<60:
		print("不及格")
	elif grade<80:
		print("及格")
	elif grade<90:
		print("良")
	else:
		print("优")
else:
	print("成绩不合法")

# 练习：
#   写程序，输入一个数
#     1) 用if语句计算出这个数的绝对值并打印出来
#     2) 用条件表达式计算出这个数的绝对值并打印出来
# 方法一
i=int(input("输入一个数:"))
if i:
	print("这个数的绝对值",abs(i))

# 方法二
i=int(input("输入一个数:"))
if i<0:
	print("这个数的绝对值",-i)
else:
	print("这个数的绝对值",i)

# 方法三
i=int(input("输入一个数:"))
absolute=i if i>0 else -i
print("这个数的绝对值",absolute)

# 方法四
i=int(input("输入一个数:"))
absolute=i 
if i<0:
    absolute=-absolute 
print("这个数的绝对值",absolute)


score = input("请输入成绩: ") or '0'
score = int(score)
if score < 0 or score > 100:
    print("您的成绩不合法!!!")
else:
    print("您输入的成绩是:", score)

# 练习：
#   1. 北京出租车计费
#     收费标准:
#       3公里以内收费13元
#       超过3公里后基本单价为 2.3元/公里
#       空驶费: 超过15公里后，每公里加收基本单价的50%作为返程的空驶费(3.45元/公里)
#     要求：
#       输入公里数，打印出费用的金额(以元为单位进行四舍五入)

gongli=input("请输入公里数：") or '0'
gongli=float(gongli)
money=13
if gongli<3.0:
	print("您要支付的费用是：",round(money))
elif gongli<15.0:
	print("您要支付的费用是：",round(money+(gongli-3.0)*2.3))
else:
	print("您要支付的费用是：",round(money+12*2.3+(gongli-15)*3.45))

#   2. 输一个学生的三科成绩：
#      1. 打印出最高分是多少分
#      2. 打印出最低分是多少分
#      3. 打印出平均分是多少分
score1=input("请输入语文成绩：")or '0'
score1=float(score1)
score2=input("请输入数学成绩：")or '0'
score2=float(score2)
score3=input("请输入英语成绩：")or '0'
score3=float(score3)
if score1<score2 and score1<score3:
	if score2>score3:
		print("最高分是英语成绩",score3)
		print("最低分是语文成绩",score1)
	else:
		print("最高分是数学成绩",score2)
		print("最低分是语文成绩",score1)
elif score2>score3:
	print("最高分是语文成绩:",score1)
	print("最低分是英语成绩",score3)
else:
	print("最高分是语文成绩",score1)
	print("最低分是数学成绩",score2)
print("平均成绩是：",(score1+score2+score3)/3)

#   3. 给出一个年份，判断是否为闰年并打印结果
#     闰年规则: 每四年一闰，每百年不闰，四百年又是一个闰年
#     例:
#       2016年 闰年 
#       2100年 不是闰年
#       2400年 是闰年
year=input("请输入一个年份：")or'0'
year=int(year)
if (year%4==0 and year%100!=0) or year%400==0:
	print(year,"年是闰年")
else:
	print(year,"年不是闰年")

#   4 BMI 指数(Body Mass Index) 以称身体质量指数
#     BMI值计算公式: 
#          BMI = 体重(公斤)/ 身高(米)的平方
#     例如:
#        一个69公斤的人，身高是 173公分
#        BMI = 69 / 1.73 ** 2 = 23.05
#     标准表:
#        BMI < 18.5        体重过轻
#        18.5 <= BMI <= 24 正常范围
#        BMI > 24          体重过重（超标)
#     输入身高和体重，打印BMI值，并打印体重状况
high=input("请输入身高(cm)：") or '0'
weight=input("请输入体重(kg)：") or '0'
high=float(high)
weight=float(weight)
BMI=weight/(round(high/100,2))**2
if BMI<18.5:
	print("体重过轻")
elif BMI<=24:
	print("正常范围")
else:
	print("体重过重（超标)")
