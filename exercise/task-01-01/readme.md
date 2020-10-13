>选择题 

1、下面关于虚拟 DOM 的说法正确的是：（A C D）

A. 使用虚拟 DOM 不需要手动操作 DOM，可以极大的提高程序的性能。

B. 使用虚拟 DOM 不需要手动操作 DOM，可以极大的提高开发效率。

C. 虚拟 DOM 可以维护程序的状态，通过对比两次状态的差异更新真实 DOM。

D. 虚拟 DOM 本质上是 JavaScript 对象，可以跨平台，例如服务器渲染、Weex 开发等。

2、下面关于 Snabbdom 库的描述错误的是：（B D）

A. Snabbdom 库是一个高效的虚拟 DOM 库，Vue.js 的虚拟 DOM 借鉴了 Snabbdom 库。

B. 使用 h() 函数创建 VNode 对象，描述真实 DOM 结构。

C. Snabbdom 库本身可以处理 DOM 的属性、事件、样式等操作。

D. 使用 patch(oldVnode, null) 可以清空页面元素

>简答题

1、请简述 patchVnode 函数的执行过程。

找到对应的真实 dom，称为 el

判断 vnode 和 oldVnode 是否指向同一个对象。

如果是，那么直接 return。

如果他们都有文本节点并且不相等，那么将 el 的文本节点设置为 vnode 的文本节点。

如果 oldVnode 有子节点而 vnode 没有，则删除 el 的子节点。

如果 oldVnode 没有子节点而 vnode 有，则将 vnode 的子节点真实化之后添加到 el

如果两者都有子节点，则执行 updateChildren 函数比较子节点。
