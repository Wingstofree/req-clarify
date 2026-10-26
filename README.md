# req-clarify

CLI需求澄清工作流 skill。提出新业务需求时，先批量提问确认边界，需求明确后再输出需求文档，不开始编码。

## 安装

克隆到 Qoder 的 skills 目录（项目级或用户级二选一）：

```bash
# 项目级：仅当前项目可用
git clone https://github.com/Wingstofree/req-clarify.git .qoder/skills/req-clarify

# 用户级：所有项目可用
git clone https://github.com/Wingstofree/req-clarify.git ~/.qoder/skills/req-clarify
```

安装后重启会话即可使用。

## 使用

```
/req-clarify 你的需求内容
```

工作流：

1. AI 复述理解，必要时给出初步方案
2. 批量提问确认边界：≤4 个问题用点选表单（AskUserQuestion），超过 4 个用纯文本 Q1…Qn 一次列全；禁止逐题交互
3. 能从需求、代码、规范确认的不问；次要细节记入"默认假设"不追问；纯技术实现细节由 AI 自己判断
4. 需求明确后输出需求文档（背景与目标、范围内事项、明确不做、业务规则、边界与异常、数据/接口/权限影响、默认假设、可验证的验收标准），说"需求已明确"后停止
