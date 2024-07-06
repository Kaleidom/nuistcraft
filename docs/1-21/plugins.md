---
title: 服务器插件
---

本服务器提供丰富的 Paper 插件，同时致力于还原原版特性（包括RNG和红石）

## 常规指令

* `/home` 和 `/sethome`，设置你的家

* `/tpa` ，玩家间传送

* `/tick` ，可以用于加速游戏进程，**请勿滥用**

* `/tabtps`，用于监听服务器 TPS

* `/locate`，用于定位结构和群系

## 存档备份



我们使用 MCD Reforged 插件 [PrimeBackup](https://tisunion.github.io/PrimeBackup/) 进行存档备份。如果忘记任何指令，使用 `!!pb help` 查看帮助。

任何人都有权限触发存档备份和回档，操作方法如下：
```
!!pb make
```

要查看已经有的备份，可以使用

```
!!pb list
```

这么做可以列出所有备份文件，其中第一列是备份文件的 ID，第二列是备份文件的创建时间。

要回档，可以使用

```
!!pb back <id>
```

我们会每隔 24h 进行一次自动存档备份。如果这一天内没有 Bot 以外的玩家出现在服务器内，那么这次备份会被跳过。

:::caution

本插件的设计主要是为了挽救一些灾难性的损失，如基础设施的毁坏、装饰建筑被损毁等情况，不是很推荐通过这个办法来避免个人的死亡。

:::

## 假人（bot）

你可以用假人代替你在某些地方挂机，用于简单地永久加载一些区块，这在本服务器中的一些双维度设施中极其有用。

目前假人插件由 [Leaves 服务端](https://leavesmc.org/) 提供，实现和使用与 Carpet 假人略有不同，但功能同样强大。

要添加名字为 `hsds` 的假人在当前位置，可以使用

```mcfunction
/bot create hsds
```

要移除这一个假人，可以使用

```mcfunction
!!bot remove hsds
```

**右键假人可以编辑它的背包**，使用 `/bot action` 指令甚至可以自定义假人的动作。

:::tip

服务器内假人周围不会生成幻翼、不影响玩家睡觉跳过黑夜、不参加判定是否跳过存档备份的玩家计数。

:::