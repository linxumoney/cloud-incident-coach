# Cloud Incident Coach：云安全事件响应与取证处置 Skill

云安全事件里最危险的动作，往往是慌乱中直接删资源、轮换一切、关闭日志，结果既没控制影响，也失去了追查依据。

`cloud-incident-coach` 是一个只面向防御场景的开源云安全事件响应与取证 Agent Skill。它帮助响应人员保全日志和快照、建立事件时间线、划定身份与数据影响范围、选择可逆遏制动作，并规划恢复和复盘。兼容 Codex、Claude Code、Cursor 和 OpenCode 等支持 `SKILL.md` 的工具。

## 它能协助

- 建立事件指挥结构和严重度
- 生成证据保全清单与时间线
- 区分身份、网络、数据和工作负载影响
- 设计分阶段、可回滚的遏制方案
- 整理内部沟通、监管与客户通知所需事实
- 形成复盘中的根因、促成因素和修复负责人

## 使用示例

```text
用 $cloud-incident-coach 帮我梳理这次云账号异常登录事件。
只做防御响应，先列需要保全的证据，再给可逆的遏制动作。
```

## 安装

```bash
cp -R skills/cloud-incident-coach ~/.codex/skills/
```

## 适用场景

- AWS、Azure、GCP 等云账号异常登录和凭据泄露
- 云资源配置误改、公开暴露和数据访问异常
- 容器、虚拟机、函数和工作负载安全事件
- 事件证据保全、时间线、影响范围和遏制方案
- 安全事件沟通、服务恢复和事后复盘

## 常见问题

### 它会执行隔离或删除资源吗？

不会自动执行破坏性操作。输出会说明动作目的、业务风险、回滚方法和验证信号，高风险操作需要人工审批。

### 为什么先保全证据？

直接删除资源或关闭服务可能破坏日志、内存、磁盘和配置证据，也可能扩大业务影响。Skill 会优先设计可逆的处置顺序。

### 可以用于渗透测试吗？

它只覆盖防御、取证、遏制、恢复和复盘，不提供提权、持久化、横向移动或规避检测指导。

## 方法参考

本项目独立实现。云事件响应问题域参考了 [mukul975/Anthropic-Cybersecurity-Skills](https://github.com/mukul975/Anthropic-Cybersecurity-Skills) 的防御性公开 Skill，该项目采用 Apache-2.0 License。本项目未复制其脚本、参考文件、模板、自动化代理或文字，也不包含攻击性操作流程。

## License

MIT License。

## 商业授权

个人学习、研究、测试和非商业使用可以。商业使用请先联系 **linxu.money@gmail.com** 获得授权，详见 [COMMERCIAL-LICENSING.md](COMMERCIAL-LICENSING.md)。

