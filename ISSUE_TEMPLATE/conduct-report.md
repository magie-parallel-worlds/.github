name: 🚨 行为准则举报 / Conduct Report
about: 用于举报违反《行为准则》的事件。团队将严格保密处理。
title: 'Conduct Report: [简要描述，例如“不当言论”或“骚扰行为”]'
labels: ['conduct']
assignees: ''

body:
  - type: markdown
    attributes:
      value: |
        感谢你花时间维护社区的健康环境。  
        本表单用于向维护团队**私密报告**不当行为。  
        **注意**：GitHub 免费版不支持完全私密 Issue，因此**请勿在此填写敏感细节（如姓名、截图、完整对话）**。  
        如需提交证据，请通过 [Discord 向 @Community Manager 发送私信](https://discord.gg/Mu3jvzBE)。

  - type: textarea
    id: description
    attributes:
      label: 事件简述
      description: 请描述发生了什么、涉及哪些公开内容（如 GitHub 评论链接、Discord 消息链接等），以及为何你认为它违反了行为准则。
      placeholder: 例如：“用户 @xxx 在 PR #123 的评论中使用了歧视性语言，链接：https://...”
    validations:
      required: true

  - type: dropdown
    id: location
    attributes:
      label: 发生位置
      description: 事件主要发生在哪个平台？
      options:
        - GitHub（Issues / PR / Discussions）
        - Discord 服务器
        - 社交媒体（Twitter / Reddit 等）
        - 其他（请说明）
    validations:
      required: true

  - type: checkboxes
    id: consent
    attributes:
      label: 我确认
      options:
        - label: 我已阅读 [行为准则](https://github.com/magie-parallel-worlds/.github/blob/main/CODE_OF_CONDUCT.md)
          required: true
        - label: 我理解此 Issue 将对所有维护者可见，但不会公开细节
          required: true
        - label: 我愿意在必要时通过 Discord 私信提供更多信息
          required: false

  - type: markdown
    attributes:
      value: |
        ⏳ 提交后，社区管理员将在 **3 个工作日内** 与你联系。  
        如情况紧急（如涉及人身威胁），请直接通过 Discord 联系 @Community Manager。
