# 底盘采购 Process House

> **端到端流程标准 | Process Handbook | GitHub模块化版 V10.0**

本仓库采用“主目录 + 分模块流程文件”的结构。每个业务板块独立维护，便于GitHub渲染、版本审查、责任分配和后续更新。

## 文档导航

| 层级 | 模块 | 主要内容 | 文件 |
|---|---|---|---|
| L0-L1 | 流程架构 | 全生命周期、角色协同 | [打开](docs/00_process-architecture.md) |
| L2-01 | 询价与预算 | 需求检查、询价、报价审核、预算 | [打开](docs/01_inquiry-budget.md) |
| L2-02 | 中标后采购准备 | 技术检查、订购资料 | [打开](docs/02_post-award-preparation.md) |
| L2-03 | SAP采购订单 | BANF、ME21N、价格、文本、附件 | [打开](docs/03_sap-purchase-order.md) |
| L2-04 | 审批与正式订单 | 签字、审批、订单发送 | [打开](docs/04_approval-order-release.md) |
| L2-05 | 订单确认AB | 催收、审核、差异闭环 | [打开](docs/05_order-confirmation.md) |
| L2-06 | 交期与变更管控 | SOP差异、风险分级、变更 | [打开](docs/06_delivery-change-control.md) |
| L2-07 | 到货、入库与质量 | 到货识别、主数据、质量放行 | [打开](docs/07_receipt-quality.md) |
| L2-08 | 注册文件与归档 | 注册资料、版本、结案检查 | [打开](docs/08_registration-archiving.md) |
| L2-09 | 周期性管理 | 日、周、月管理节奏 | [打开](docs/09_periodic-management.md) |
| L2-10 | 质量门与结案 | 七个质量门、快速检查、结案 | [打开](docs/10_quality-gates-closing.md) |
| 治理 | RACI与KPI | 职责矩阵、指标、例外升级 | [打开](docs/11_governance-raci-kpi.md) |

## Process House

```mermaid
graph LR
    A["L0 底盘采购端到端价值链"] --> B["询价与预算"] --> C["中标后准备"] --> D["SAP采购订单"] --> E["审批与订单发送"] --> F["订单确认AB"] --> G["交期与变更"] --> H["到货与质量"] --> I["注册与归档"] --> J["结案与持续改进"]
```

## 仓库结构

```text
chassis-process-house/
├── README.md
├── CHANGELOG.md
├── CONTRIBUTING.md
└── docs/
    ├── 00_process-architecture.md
    ├── 01_inquiry-budget.md
    ├── 02_post-award-preparation.md
    ├── 03_sap-purchase-order.md
    ├── 04_approval-order-release.md
    ├── 05_order-confirmation.md
    ├── 06_delivery-change-control.md
    ├── 07_receipt-quality.md
    ├── 08_registration-archiving.md
    ├── 09_periodic-management.md
    ├── 10_quality-gates-closing.md
    └── 11_governance-raci-kpi.md
```

## 发布规则

1. `README.md`仅作为入口和流程架构页。
2. 业务变化在对应的`docs/*.md`文件中修改。
3. 每次变更同步更新`CHANGELOG.md`。
4. Mermaid仅使用GitHub原生兼容语法：`graph LR`、标准节点和标准连线。
5. 合并到主分支前，应逐个打开所有Markdown文件确认流程图正常渲染。
