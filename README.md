# Cloud Incident Coach：出事时先保全证据，再恢复服务

云安全事件里最危险的动作，往往是慌乱中直接删资源、轮换一切、关闭日志，结果既没控制影响，也失去了追查依据。

`cloud-incident-coach` 是一个只面向防御场景的开源 Agent Skill。它帮助响应人员建立时间线、划定影响范围、选择可逆的遏制动作，并保持证据与业务连续性之间的平衡。

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

## 方法参考

本项目独立实现。云事件响应问题域参考了 [mukul975/Anthropic-Cybersecurity-Skills](https://github.com/mukul975/Anthropic-Cybersecurity-Skills) 的防御性公开 Skill，该项目采用 Apache-2.0 License。本项目未复制其脚本、参考文件、模板、自动化代理或文字，也不包含攻击性操作流程。

## License

MIT License。
