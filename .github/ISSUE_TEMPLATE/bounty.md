# 赏金 Issue 模板

---

name: 🎯 发布赏金
description: 发布新的赏金任务
title: "BOUNTY: [简短描述]"
labels: ["bounty", "needs-review"]
assignees: []

body:
  - type: markdown
    attributes:
      value: |
        感谢发布赏金！请填写以下详细信息。

  - type: textarea
    id: description
    attributes:
      label: 📋 任务描述
      description: 清晰、详细地描述需要完成的任务
      placeholder: |
        描述你需要什么以及为什么需要它。
        包括背景信息和任何相关的上下文。
      required: true

  - type: textarea
    id: acceptance-criteria
    attributes:
      label: ✅ 验收标准
      description: 列出所有必须满足的条件（至少 3 个）
      placeholder: |
        - [ ] 标准 1
        - [ ] 标准 2  
        - [ ] 标准 3
        - [ ] 标准 4 (可选)
      required: true

  - type: textarea
    id: technical-requirements
    attributes:
      label: 🛠 技术要求
      description: 指定所需的技术栈、语言、框架等
      placeholder: |
        - 编程语言: 
        - 框架/库: 
        - 数据库: 
        - 其他要求:
      required: true

  - type: textarea
    id: resources
    attributes:
      label: 📚 参考资源
      description: 提供有用的链接、文档、示例等（可选）
      placeholder: |
        - 相关 Issue: #123
        - 文档链接: https://...
        - 参考项目: https://...
      required: false

  - type: dropdown
    id: timeline
    attributes:
      label: ⏰ 预期时间框架
      description: 此任务应该需要多长时间完成？
      options:
        - "< 1 小时"
        - "1-2 小时"
        - "2-4 小时"
        - "4-8 小时"
        - "> 8 小时"
      required: true

  - type: input
    id: budget
    attributes:
      label: 💰 奖励金额
      description: 输入美元金额（例如: 50, 100, 250）
      placeholder: "50"
      required: true

  - type: dropdown
    id: difficulty
    attributes:
      label: 🎓 难度等级
      options:
        - "初级 (Beginner)"
        - "中级 (Intermediate)"
        - "高级 (Advanced)"
        - "专家 (Expert)"
      required: true

  - type: checkboxes
    id: verification
    attributes:
      label: ✔️ 验收前检查
      description: 发布前请确保所有项都已完成
      options:
        - label: "任务清晰且可衡量"
          required: true
        - label: "没有暴露敏感信息或 API 密钥"
          required: true
        - label: "金额与复杂度相符"
          required: true
        - label: "我有足够的资源支付此赏金"
          required: true
        - label: "我已阅读并同意 CONTRIBUTING.md"
          required: true

  - type: markdown
    attributes:
      value: |
        ---
        
        ## 📝 下一步
        
        1. 提交此 Issue
        2. 社区成员可能会提出问题或提供反馈
        3. 在获得社区反馈后，评论 `/opire create $XXX` 来激活赏金
        4. 分享此 Issue 链接，吸引贡献者参与
        
        感谢你对 Claude Builders Bounty 社区的贡献！🚀
