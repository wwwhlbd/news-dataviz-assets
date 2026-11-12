# 素材读取试例

此目录包含三张来自《经济日报》2026-11-03 数据版的裁切图，以及对应的 JSON 和 SQLite 示例记录。它们仅供同学检查读取接口；保留了白色背景，购物车还带有图表线条，未通过正式质量审核，不计入合格素材总数。

- `sample_records.json`：三条可直接查看的示例记录。
- `sample_assets.sqlite3`：同样三条数据，表名 `assets`；`tags_json` 和 `crop_box_json` 分别是 JSON 数组文本。
- `*.png`：示例图片，记录中的 `relative_path` 相对于**仓库根目录**。

示例库是独立数据库，字段供讨论，与仓库根目录正式 `assets.sqlite3` 的表结构并不完全一致；前端对接尚未确认。可用 SQLite 工具只读打开示例库并执行：

```sql
SELECT id, name, category, tags_json, relative_path FROM assets;
```

请试读后反馈：相对路径是否方便使用；需要哪些字段、标签类型及数据格式；是否需要透明背景、其他图片尺寸或批量读取方式；是否希望正式数据库沿用此表结构。

原版来源：[经济日报 2026-11-03 数据版](http://paper.ce.cn/pc/layout/202611/03/node_09.html)。用户表示版面和裁切元素可以公开；具体授权文件尚未提供。
