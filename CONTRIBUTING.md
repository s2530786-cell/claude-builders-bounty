# 贡献指南 (Contributing Guide)

感谢你对 Claude Builders Bounty 的兴趣！本指南将帮助你有效地参与我们的社区。

## 快速开始

### 我想发布赏金

1. **打开 Issue** - 点击 "Issues" → "New Issue" → 选择 "赏金发布" 模板
2. **填写详情** - 包含清晰的描述和验收标准
3. **激活赏金** - 在 Issue 中评论 `/opire create $金额` (例如: `/opire create $50`)
4. **分享** - 将链接分享给社区

### 我想领取赏金

1. **浏览赏金** - 查看 "Issues" 找到感兴趣的任务
2. **理解需求** - 仔细阅读描述和验收标准
3. **声明赏金** - 评论 `/opire try` 表示你将处理此任务
4. **创建 PR** - 提交拉取请求解决问题
5. **获得报酬** - PR 合并后自动支付 ✅

## 赏金发布者指南

### 发布前检查表

- [ ] 任务与 Claude Code 或 AI 工具相关
- [ ] 有清晰、可测试的验收标准
- [ ] 预期工作量与报酬相符
- [ ] 没有暴露敏感信息或凭证
- [ ] 至少 2 个维护者审查过描述

### 最佳实践

#### 清晰的描述

```markdown
## 目标
简明扼要地说明需要完成的事项。

## 背景
为什么需要这个功能？

## 验收标准
- [ ] 具体要求 1
- [ ] 具体要求 2
- [ ] 具体要求 3

## 文件/目录
涉及的特定文件或目录。

## 时间估计
预期需要多长时间？

## 额外信息
任何其他相关细节。
```

#### 合理的报酬指南

| 复杂度 | 时间 | 建议报酬 |
|--------|------|--------|
| 简单 | < 1 小时 | $25-50 |
| 中等 | 1-4 小时 | $50-150 |
| 复杂 | 4-8 小时 | $150-300 |
| 非常复杂 | > 8 小时 | $300+ |

### 评估 PR 时

✅ **接受标准**：
- 完成了所有验收标准
- 代码质量高且可维护
- 包含必要的测试（如适用）
- 清晰的提交消息和文档
- 遵循项目代码风格

❌ **拒绝原因**：
- 只完成了部分要求
- 代码难以理解或维护
- 没有进行必要的测试
- 包含不相关的更改

## 赏金领取者指南

### 开始之前

1. **理解需求** - 仔细阅读所有验收标准
2. **提问** - 在 Issue 中澄清任何疑惑
3. **检查重复** - 确保没有人已经在做这个任务
4. **本地测试** - 在本地验证你的解决方案

### 编写高质量代码

```typescript
// ✅ 好的代码
function validateBountyAmount(amount: number): boolean {
  // 检查金额是否为正数
  if (amount <= 0) {
    throw new Error('赏金金额必须大于 0');
  }
  
  // 检查是否为整数
  if (!Number.isInteger(amount)) {
    throw new Error('赏金金额必须是整数');
  }
  
  return true;
}

// ❌ 不好的代码
function validate(x) {
  return x > 0;
}
```

### 提交 PR

```markdown
## 关联 Issue
Closes #123

## 更改描述
简要说明你做了什么。

## 验证
- [ ] 完成了所有验收标准
- [ ] 本地测试通过
- [ ] 遵循代码风格
- [ ] 更新了相关文档

## 截图（如适用）
添加相关截图或演示。
```

### PR 流程

1. **创建分支** - `git checkout -b fix/issue-123`
2. **提交更改** - 清晰的、原子性的提交
3. **推送并创建 PR** - 填写完整的 PR 模板
4. **响应反馈** - 及时处理审查意见
5. **合并和支付** - 维护者合并后自动支付

## 代码标准

### 通用标准

- 使用描述性变量名
- 添加必要的注释和文档
- 保持函数简短且专注
- 处理边界情况和错误
- 编写可测试的代码

### 语言特定

**JavaScript/TypeScript:**
```typescript
// 使用 TypeScript 进行类型检查
interface BountyTask {
  id: string;
  title: string;
  amount: number;
  status: 'open' | 'claimed' | 'completed';
}

// 使用箭头函数和现代语法
const getBounties = (tasks: BountyTask[]) => 
  tasks.filter(t => t.status === 'open');
```

**Python:**
```python
# 遵循 PEP 8 风格指南
def validate_bounty_amount(amount: int) -> bool:
    """验证赏金金额是否有效。"""
    if amount <= 0:
        raise ValueError("赏金金额必须大于 0")
    return True
```

## 沟通

### Issue 中的礼仪

- ✅ 使用清晰、尊重的语言
- ✅ 一次性解决一个问题
- ✅ 提供足够的背景信息
- ❌ 不要骚扰或威胁
- ❌ 不要跨题目讨论

### 问题和反馈

**有疑问？**  
在 Issue 中评论并使用 `@mention` 标记相关人员。

**有建议？**  
开设讨论或创建一个新 Issue 来讨论改进。

**有问题？**  
参考 README.md 或发送邮件至 help@claudebounty.dev

## 许可和版权

通过贡献代码，你同意在 MIT 许可下发布你的工作。这意味着任何人都可以使用、修改和分发你的代码。

## 行为和安全

所有贡献者必须遵守 [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)。

有安全问题？参考 [SECURITY.md](SECURITY.md)。

---

感谢你的贡献！🎉

有任何问题，请联系 team@claudebounty.dev