# Rustic Delight Potato Sword Datapack

一个用于解决 **Rustic Delight（乡村乐事）** 与 **More Delight（多趣乐事）** 土豆切割配方冲突的小型数据包。

A small compatibility datapack that resolves the potato cutting recipe conflict between **Rustic Delight** and **More Delight**.

## 功能 / Features

本数据包覆盖以下 Rustic Delight 配方：

```text
rusticdelight:item/potato_slices
```

改动内容：

* 将 Rustic Delight 的土豆片切割工具由刀改为任意剑。
* 接受 `#minecraft:swords` 标签中的所有物品。
* 每个土豆仍然产出 2 个 `rusticdelight:potato_slices`。
* More Delight 的刀切土豆配方保持不变。

This datapack:

* Changes Rustic Delight's potato slices recipe from knives to swords.
* Accepts any item in the `#minecraft:swords` item tag.
* Still produces 2 `rusticdelight:potato_slices` per potato.
* Leaves More Delight's knife-based diced potato recipe unchanged.

## 依赖 / Requirements

测试环境：

| 项目                            | 版本          |
| ----------------------------- | ----------- |
| Minecraft Java Edition        | 26.2        |
| Mod Loader                    | Fabric      |
| Farmer's Delight Refabricated | 26.2-3.6.15 |
| Rustic Delight                | 1.7.0       |
| More Delight                  | 26.06.23    |

必须安装：

* [Farmer's Delight Refabricated](https://github.com/MehVahdJukaar/FarmersDelightRefabricated)
* [Rustic Delight](https://github.com/PhantomWing/RusticDelight)

More Delight 不是运行本数据包的硬依赖，但本数据包最初是为了解决它与 Rustic Delight 之间的配方冲突而制作的。

More Delight is not strictly required, but this datapack was created to resolve its recipe conflict with Rustic Delight.

## 安装 / Installation

1. 打开本仓库的 **Releases** 页面。
2. 下载 `rustic-delight-potato-sword-26.2.zip`。
3. 不要解压 ZIP。
4. 将 ZIP 放入存档的以下目录：

```text
.minecraft/saves/<存档名称>/datapacks/
```

5. 重新进入世界，或执行：

```mcfunction
/reload
```

可以使用以下命令确认数据包已加载：

```mcfunction
/datapack list
```

English:

1. Open the **Releases** page of this repository.
2. Download `rustic-delight-potato-sword-26.2.zip`.
3. Do not extract the ZIP.
4. Place it in `<world>/datapacks/`.
5. Re-enter the world or run `/reload`.

> Do not use GitHub's automatically generated “Source code” archives as the installable datapack. Download the ZIP listed under Release assets.

## 兼容性 / Compatibility

目前仅在以下环境经过测试：

```text
Minecraft Java Edition 26.2 + Fabric
```

其他 Minecraft 或模组版本可能仍然有效，但目前不提供正式支持。不同版本可能使用不同的数据包格式、配方路径或配方语法。

Currently tested only on Minecraft Java Edition 26.2 with Fabric. Other versions may work, but are not officially supported.

## 原理 / How It Works

数据包通过相同的命名空间和路径覆盖 Rustic Delight 的原始配方：

```text
data/rusticdelight/recipe/item/potato_slices.json
```

原配方使用：

```json
"tool": "#c:tools/knife"
```

本数据包将其替换为：

```json
"tool": "#minecraft:swords"
```

除此之外，配方输入、输出数量和 Rustic Delight 的配置加载条件均保持不变。

## AI 使用说明 / AI Assistance Disclosure

本数据包在开发过程中使用了 OpenAI ChatGPT / Codex 进行辅助，包括检查模组配方文件、生成和验证数据包结构，以及协助编写项目文档。

数据包的功能需求、设计选择、实际游戏测试和发布决定均由项目维护者完成。维护者已检查生成内容，并对本项目发布的文件及其维护负责。

This datapack was created with assistance from OpenAI ChatGPT / Codex, including inspection of mod recipe files, generation and validation of the datapack structure, and preparation of project documentation.

The project maintainer defined the requirements, made the design decisions, tested the datapack in-game, reviewed the generated content, and remains responsible for the files published in this repository.

## 许可证 / License

本项目中由仓库维护者编写的内容使用 [MIT License](LICENSE) 发布。

修改后的配方文件基于 Rustic Delight 的原始配方。Rustic Delight 由 PhantomWing 开发并使用 MIT License 发布。详情请参阅 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。

Original project links:

* [Rustic Delight](https://github.com/PhantomWing/RusticDelight)
* [Farmer's Delight Refabricated](https://github.com/MehVahdJukaar/FarmersDelightRefabricated)
* [More Delight](https://github.com/axperty/moredelight)

## 免责声明 / Disclaimer

这是一个非官方社区数据包，与 Minecraft、Mojang Studios、Farmer's Delight、Rustic Delight 或 More Delight 的开发者没有隶属或认可关系。

This is an unofficial community datapack and is not affiliated with or endorsed by Mojang Studios or the developers of Farmer's Delight, Rustic Delight, or More Delight.
