

### 1. #{}和${}的区别是什么？

- mybatis在处理#{}时，会将sql中的#{}替换为?号，调用PreparedStatement的set方法来赋值。

- mybatis在处理${}时，就是把${}替换成变量的值。

- 使用#{}可以有效的防止SQL注入，提高系统安全性。原因在于：预编译机制。预编译完成之后，SQL的结构已经固定，即便用户输入非法参数，也不会对SQL的结构产生影响，从而避免了潜在的安全风险。

- 预编译是提前对SQL语句进行预编译，而其后注入的参数将不会再进行SQL编译。我们知道，SQL注入是发生在编译的过程中，因为恶意注入了某些特殊字符，最后被编译成了恶意的执行操作。而预编译机制则可以很好的防止SQL注入。

补充1：
$符号一般用来当作占位符，常使用Linux脚本的人应该对此有更深的体会吧。例如：$1，$2等等表示输入参数的占位符。知道了这点就能很容易区分$和#，从而不容易记错了。

补充2：
万事洞明皆学问，对于mybatis与sql这两门技术而言，看似简单，但是深挖进去会发现里面的东西还是挺多的。要想成为一名合格的开发人员，需要不断的去学习，更需要不断的去思考。可以参考：http://www.mybatis.cn/category/mysql-mybatis/，系统的学习sql和mybatis的东西，这是本站2019年计划出版的小册子，欢迎试读。

补充3：
有网友提问：既然${}会引起sql注入，为什么有了#{}还需要有${}呢？那其存在的意义是什么？

可以这么去理解：#{}主要用于预编译，而预编译的场景其实非常受限，而${}用于替换，很多场景会出现替换，而这种场景可不是预编译



### MyBatis 是否可以映射 Enum 枚举类？
映射方式为自定义一个 TypeHandler，实现 TypeHandler 的 setParameter()和 getResult()接口方法。
TypeHandler 有两个作用，一是完成从 javaType 至 jdbcType 的转换，
二是完成 jdbcType 至 javaType 的转换，体现为 setParameter()和 getResult()两个方法，分别代表设置 sql 问号占位符参数和获取列查询结果


### mybati学习

- [MyBatis源码学习（一）](https://juejin.im/post/5ed79de2518825431845aa1c)
- [MyBatis源码学习（二）](https://juejin.im/post/5edb23196fb9a047b11b59e3)
- [MyBatis源码学习（三）](https://juejin.im/post/5edb6059e51d45783e17bb04)
- [MyBatis源码学习（四）](https://juejin.im/post/6857358748152381447/)





