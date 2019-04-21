项目传递依赖冲突关系处理.

A --> B-1.0 --> C-1.0
A --> C-1.1

A会编译失败。若在A中的dependency B中把C exclude掉，则会成功。

按照依赖关系及maven-enforcer-plugin的设置进行编译，最后通过maven-dependency-plugin
将`user-service`的jar包copy到`target/lib`目录下。

