
# 任务
## 任务类型
Gradle Task 的默认类型是 DefaultTask，也可以显示地声明 Task 的类型，甚至可以自定义 Task 类型。

```
task copyFile(type: Copy) {
   from 'xml'
   into 'destination'
}
```

## 任务依赖

Gradle Task 之间存在依赖关系，被依赖的 Task 会优先执行。

```
task taskA(dependsOn: taskB) {
   //do something
}
```

## 任务帮助

Gradle 在默认情况下为我们提供了几个常用的Task，例如查看 Project 的 Properties、显示当前 Project 中定义的所有 Task 等。

- `gradle tasks`：查看所有任务
- `gradle tasks --all`：查看所有任务和明细信息
- `gradle help --task <task>`：查看某个任务的明细信息
- `gradle properties`：显示项目的所有属性
- `gradle dependencies`：显示项目的依赖信息
- `gradle projects`：显示所有项目，包括根项目和子项目