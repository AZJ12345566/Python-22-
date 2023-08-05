# Python-22-
Python学习笔记(22)
# p71 集合的概述与创建
#集合属于可变类型的序列
#集合只有键没有值，是一个没有value的字典
#集合创建方式
s={'Python','hello',90}

s={2,4,5,5,6,7,7}
print(s)  #集合中的元素不允许重复，会讲重复的去除
'还可以是由内置函数set()'
s1=set(range(6))
print(s1,type(s1))

s2=set([1,2,4,5,5,5,6,6]) #这里讲列表类型转化为了集合类型，同时去除了重复元素
print(s2,type(s2))

set((1,2,4,4,5,65))  
print(s3,type(s3))  #集合的元素是无序的，因此打印出来的顺序可能是乱的

s4=set('python')
print(s4,type(s4))

s5=set({12,4,34,55,66,44,4})
print(s5,type(s5))

#定义一个空集合
s6=set()
print(type(s6))  #不能用s6{}，这是字典



# p72 集合的相关操作
s={10,20,30,405,60}
print(10 in s)  #True
print(100 in s)  #False
print(10 not in s)  #False
print(100 not in s)  #True
#以上为判断操作

'集合元素的新增操作'
s.add(80)  #一次添加一个元素
print(s)
s.updata({200,400,300})  #updata一次至少添加一个元素
print(s)
s.updata([100,99,8])
s.updata((78,56,64))

'集合元素的删除操作'
s.remove(100)
print(s)
s.remove(500)
print(s)  #在移除元素的操作中，元素一定要在集合中，否则抛警告
s.discard(500)  #这一种移除方式就不会抛异常

s.pop()
print(s)  #随机删除一个幸运儿，而且pop函数必须是无参的

s.clear()
print(s)  #清空整个集合



#  p73 集合间的关系
'两个集合之间是否相等(元素相同就相等)'
s={10,20,30,40}
s2={30,40,20,10}
print(s==s2)  #True
print(s!=s2)  #False

'一个集合是否是另一个集合的子集'
s1={10,20,30,40,50,60}
s2={10,20,30,40}
s3={10,20,90}
print(s2.issubset(s1))  #True
print(s3.issubset(s1))  #False

'一个集合是否是另一个集合的超集'
print(s1.issupret(s2))  #True
print(s1.issupset(s3))  #False

'两个集合是否含有交集'
print(s2.isdisjoint(s3))  #False
s4={100,200,300}
print(s2.isdisjoint(s4))  #True  没有交集为True，有交集为False
