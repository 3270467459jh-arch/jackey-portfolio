---
title: 多语言Listing一键生成工作流
publishDate: 2026-05-15 00:00:00
img: /assets/dify-workflow-diagram.svg
img_alt: Dify多语言Listing工作流架构图
description: |
  基于Dify搭建的自动化工作流，输入产品信息一键生成Amazon/Shopify多语言Listing文案，覆盖英/日/德/法/西5种语言。
tags:
  - Dify
  - Workflow
  - Automation
---

## 项目概述

跨境电商多站点运营最头疼的问题之一：同一产品要写5个语言版本的Listing。这个工作流让这件事从2小时缩短到2分钟。

**GitHub:** [查看源码](https://github.com/3270467459jh-arch/dify-multilingual-listing-workflow)

## 工作流设计

### 输入节点
- 产品名称、品类、核心卖点（3-5个）
- 目标平台（Amazon/Shopify/速卖通）
- 目标语言（可多选）

### 处理节点
1. **关键词研究Agent**：根据品类和平台生成SEO关键词
2. **Listing生成Agent**：基于关键词+卖点生成结构化文案
3. **多语言翻译Agent**：非直译，按各市场搜索习惯重写
4. **格式化输出Agent**：按平台字符限制裁剪，输出可直接粘贴的格式

### 输出
- Amazon格式：标题 + 五点描述 + 产品描述 + Search Terms
- Shopify格式：标题 + SEO Meta + 产品描述 + FAQ
- 5种语言独立输出

## 技术实现

- 平台：Dify（低代码AI工作流）
- 模型：Claude / GPT-4o
- 部署：一键发布为Web应用，团队成员直接使用

## 实际效果

- 单品Listing生成时间：2小时 → 2分钟
- 多语言覆盖：人工逐语言写 → 一次输入全部输出
- 文案质量：融入SEO关键词，非机翻，符合各市场表达习惯
