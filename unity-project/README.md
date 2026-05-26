# Unity 工程

> 这个文件夹放 Unity 工程本体。**由主程负责创建**，因为 Unity 版本、
> 工程命名、渲染管线等需要程序团队统一决定。

## 创建步骤（主程操作）

1. 用统一的 Unity 版本创建工程，工程直接建在本文件夹内。
2. 确认根目录的 `.gitignore` 和 `.gitattributes` 对 Unity 生效
   （`Library/`、`Temp/` 等已配置忽略）。
3. 安装并初始化 Git LFS：`git lfs install`。
4. 第一次提交前，确认 `Library/` 等没有被误提交。

## 建议的工程内目录结构

在 `Assets/` 下建立清晰的分类（供参考，团队可调整）：

```
Assets/
├── _Project/        ← 本项目资源总入口（下划线让它排最前）
│   ├── Scripts/     ← 代码：战斗、卡牌、关卡、UI、数据
│   ├── Art/         ← 美术：角色、场景、UI、特效
│   ├── Prefabs/     ← 预制体
│   ├── Scenes/      ← 场景
│   ├── Audio/       ← 音频
│   └── Data/        ← 卡牌表、敌人表等数据资源（ScriptableObject 等）
├── Plugins/         ← 第三方插件
└── Settings/        ← 渲染管线、输入等配置
```

## 团队需要先统一的事项

- [ ] Unity 版本（写在这里：_____）
- [ ] 渲染管线（URP / 内置 / 其他）
- [ ] 版本管理：Git LFS 还是 Plastic SCM
- [ ] 代码规范（命名、注释、文件夹约定）
- [ ] 数据表怎么进游戏（ScriptableObject / CSV / JSON）

## 注意

- 美术的概念图、参考图放在 `docs/美术/`，**进了游戏的正式资源**才放这里。
- 不要把工程的临时文件提交进仓库，提交前检查 `git status`。
