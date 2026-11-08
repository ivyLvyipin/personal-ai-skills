# Global Execution Protocol (L0)

个人 AI 工作系统的基础执行协议：减少重复解释、迎合式分析、虚构信息与“只给建议、不交付”的问题。版本：0.1.0 草案。

## 使用

将整个 `global-execution-protocol` 目录放入目标 Agent 支持的技能目录，保留根级 `SKILL.md`。具体安装与自动发现机制由目标平台决定；本包不承诺跨对话自动生效。也可在任务中明确要求加载此文件。

其他 Skill 可写：“执行前加载已安装的 global-execution-protocol/SKILL.md，应用相关 L0 规则，再执行本技能的领域流程。”路径由所在仓库或宿主解析；无法加载时说明缺失，不假装已应用。

集合仓库： https://github.com/ivyLvyipin/personal-ai-skills 。结构：

```text
personal-ai-skills/
└── global-execution-protocol/
    ├── SKILL.md
    ├── README.md
    ├── references/
    │   ├── delivery-qa.md
    │   └── product-validation.md
    └── tests/
        ├── regression.md
        └── validation-record.md
```

若使用单技能仓库，将本目录内容直接放到仓库根目录即可。采用小写连字符名称，便于符合 Agent Skills 命名约定。不包含平台专用配置、账户资料或私有业务案例。

## 维护与发布

先运行所在环境提供的 Agent Skills 格式校验，再按 tests/regression.md 做行为回归；格式通过不代表行为通过。修改共享规则后重跑受影响场景并记录证据。

目标仓库及公开可见性已由用户确认。后续发布应继续检查现有目录结构。只有远端确认成功后才称已发布。当前未指定开源许可证；公开复用授权应由仓库所有者选择，不能把公开可读等同于开放许可。

规则依据是本次请求明确列出的偏好及所引用对话中的纠错方向。未将过往助手对其他项目的概述视为已验证事实，也未声称审阅了全部历史项目。
