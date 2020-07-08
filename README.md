# 1 D
# 2 D
# 3 patchVnode执行过程
### 1，触发prepatch钩子函数
### 2，触发update钩子函数
### 3，新节点有text属性，且不等于旧节点的text属性
1）如果老节点有children,移除老节点children对应的dom元素
2）设置新节点对应dom元素的textContent
### 4，新老节点都有children,且不相等
1）调用updateChildren()
2）对比子节点，并且更新子节点的差异
### 5，只有新节点有children属性
1）如果老节点有text属性，清空对应dom元素的textContent
2）添加所有的子节点
### 6，只有老节点有children属性
1）移除所有的老节点
### 7，只有老节点有text属性
1）清空对应dom元素的textContent
### 8，触发postpatch钩子函数
