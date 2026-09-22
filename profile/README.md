# LuminaryFixtures

工业视觉 **实验室回归 / 基准图片** 组织。  
给 [VistaCast](https://github.com/VistaCast)、[SyncroBrain](https://github.com/SyncroBrain) 等产品本机调试、换电脑复现用。

> **诚实边界**：这里的图不是客户板准确率，不是已售租赁，也不是可勾选的评测集。  
> `accuracyClaimed` / `hasEvalSet` / `sellable` / `krEligible` 仍由各产品保持 **false**。

## 本机约定

```text
/Users/andyzhou/www/LuminaryFixtures/
```

与产品 Meta 仓同级。图片 **不进** 产品 Git。VistaCast 下的 `pcb-fixtures/` 是指向本目录 `pcb/` 的符号链接。

## 仓库一览（均为私有）

| 仓库 | 用途 |
| :--- | :--- |
| [pcb-images](https://github.com/LuminaryFixtures/pcb-images) | PCB/AOI、螺丝、焊点邻近图（由原 VistaCast/pcb-fixtures 迁入；本机目录仍叫 `pcb/`） |
| [surface](https://github.com/LuminaryFixtures/surface) | 铸造、磁瓦、Kolektor、BSData、ELPV、木板等表面缺陷 |
| [site](https://github.com/LuminaryFixtures/site) | 绝缘子、CrackForest（更贴 SyncroBrain 现场视觉） |
| [weld-tig-train](https://github.com/LuminaryFixtures/weld-tig-train) / [weld-tig-test](https://github.com/LuminaryFixtures/weld-tig-test) | TIG 铝焊训练/测试（已拆分，单仓 ≤10GB） |
| [weld-tig](https://github.com/LuminaryFixtures/weld-tig) | 索引：指向 train/test |
| [shelf-nutrigreen](https://github.com/LuminaryFixtures/shelf-nutrigreen) | NutriGreen 货架/营养标签（`label.presence` 邻近外观） |

未齐：SKU-110K、GRAIN 酒标（本机下载未完整）。

## 使用注意

- **单文件 &lt; 100MB**；不要提交整包 zip
- 大仓推送需分批（GitHub 单次 pack ≤ 2GB）
- 许可各异：铸造等为 CC-BY-NC-ND，只留私有仓，勿公开镜像
- Cursor / Agent：**不要** Read、搜索或解析图片字节；测试只用路径字符串

## 与产品的关系

- VistaCast：PCB AOI、组装有无件、标签、胶路等实验室包的公开邻近图
- SyncroBrain：可用 `site` 类现场视觉素材；**不会**接收 `pcb.` / `assy.` / `label.` / `bead.` 告警

以后若上 MinIO / 对象存储，本组织各仓按目录迁出即可，产品仓只改克隆地址。
