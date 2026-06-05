# 西格莉卡 / Sigrika Codex Pet

这是一个可用于 Codex 的自定义动态宠物包，角色名为 **西格莉卡 / Sigrika**。

角色设计基于一位橙色长辫、白紫服饰、带有轻科幻纹样的二次元角色形象，并转换为适合 Codex pet 使用的小尺寸 chibi 动画精灵。宠物保留了橙色分段双辫、白色头饰、银色羽翼状装饰、白紫配色服装、金色点缀、腰包挂饰和腿部电路线条等主要视觉特征。

## 文件结构

```text
sigrika_codex_pet/
  pet.json
  spritesheet.webp
  README.md
  qa/
    contact-sheet.png
    validation.json
    review.json
```

## 核心文件

- `pet.json`：Codex 读取宠物时使用的元数据文件。
- `spritesheet.webp`：最终动画图集，Codex 实际加载的宠物精灵表。
- `README.md`：本说明文档。

只安装宠物时，通常只需要 `pet.json` 和 `spritesheet.webp`。`qa/` 目录用于展示和验证，不是运行必需文件。

## 安装方法

将整个 `sigrika_codex_pet` 文件夹复制到 Codex 的 pets 目录，并确保目录名为 `sigrika`：

```text
%USERPROFILE%\.codex\pets\sigrika
```

最终目录应类似：

```text
C:\Users\<你的用户名>\.codex\pets\sigrika\pet.json
C:\Users\<你的用户名>\.codex\pets\sigrika\spritesheet.webp
```

如果你是从 GitHub 下载 zip，可以解压后把文件夹重命名为 `sigrika`，再放入上述目录。

## pet.json

当前元数据如下：

```json
{
  "id": "sigrika",
  "displayName": "西格莉卡 / Sigrika",
  "description": "A tiny anime-inspired Codex pet based on Sigrika, an orange-haired white-and-purple sci-fi shrine dancer.",
  "spritesheetPath": "spritesheet.webp"
}
```

字段说明：

- `id`：宠物的唯一标识，当前为 `sigrika`。
- `displayName`：Codex 中显示的宠物名称。
- `description`：宠物的简短描述。
- `spritesheetPath`：相对于 `pet.json` 的精灵图路径。

## 动画状态

该宠物按照 Codex pet 的 9 行动画状态制作：

| 行号 | 状态 | 帧数 | 含义 |
| --- | --- | ---: | --- |
| 0 | `idle` | 6 | 待机、呼吸、眨眼 |
| 1 | `running-right` | 8 | 向右拖动或移动 |
| 2 | `running-left` | 8 | 向左拖动或移动 |
| 3 | `waving` | 4 | 打招呼 |
| 4 | `jumping` | 5 | 跳跃 |
| 5 | `failed` | 8 | 失败、阻塞或取消时的反应 |
| 6 | `waiting` | 6 | 等待用户输入、确认或帮助 |
| 7 | `running` | 6 | 正在处理任务、思考或工作 |
| 8 | `review` | 6 | 查看结果、完成后的关注状态 |

## 图集规格

- 图集文件：`spritesheet.webp`
- 图集尺寸：`1536 x 1872`
- 单元格尺寸：`192 x 208`
- 列数：8
- 行数：9
- 背景：透明
- 未使用单元格：完全透明

## QA 文件

`qa/` 目录中包含制作过程中的验证结果和预览文件：

- `qa/contact-sheet.png`：所有动画帧的总览图，适合在 GitHub README 或 release 页面展示。
- `qa/validation.json`：最终图集验证结果。
- `qa/review.json`：逐帧检查结果。

最终验证结果：

- `validation.json`：通过
- `review.json`：通过
- 无错误
- 无警告
- 透明像素无残留 RGB 问题

## GitHub 上传建议

推荐仓库结构：

```text
your-repo/
  README.md
  pet.json
  spritesheet.webp
  qa/
    contact-sheet.png
    validation.json
    review.json
```

如果你想做一个 GitHub Release，可以上传：

```text
sigrika_codex_pet.zip
```

Release 描述里可以放：

```markdown
Codex 自定义宠物：西格莉卡 / Sigrika。

- 已包含 pet.json 和 spritesheet.webp
- 已通过 atlas validation 和 frame review
- 包含 contact sheet 预览图
```

## 预览

![西格莉卡 Codex Pet 预览图](qa/contact-sheet.png)

## 制作说明

该宠物使用 hatch-pet 工作流制作：

1. 生成主形象参考。
2. 生成 9 个 Codex pet 动画状态。
3. 将每个动画状态拆分为 `192 x 208` 单元格。
4. 合成为 `1536 x 1872` 的最终 WebP 图集。
5. 生成 contact sheet 预览图。
6. 通过图集验证与逐帧检查。

制作中对 `failed` 和 `running-left` 状态进行了额外修正，以避免边缘碎片和帧提取异常。

## 备注

本项目为个人兴趣制作的 Codex 宠物包，仅用于个人展示、学习交流与非商业使用。

该宠物形象基于《鸣潮》相关角色进行二次创作，本项目并非官方内容，也未获得《鸣潮》官方或相关权利方的授权、认可或赞助。角色原始设定、名称、世界观及相关知识产权均归其各自权利方所有。

请勿将本项目或其中素材用于任何商业活动，包括但不限于售卖、付费分发、商业宣传、商品制作、广告投放或其他营利性用途。如权利方认为本项目存在不当使用，请联系仓库维护者进行删除或调整。
