# WarZFracture - 真实骨折系统插件

## 插件概述

WarZFracture是一款为Minecraft服务器打造的高度真实的骨折系统插件，灵感来源于《三角洲行动》等FPS游戏。该插件为您的服务器带来更加真实的受伤机制，玩家在受到伤害时可能会导致不同部位的骨折，从而影响游戏体验。

## 主要特性

### 多部位骨折系统
- **头部骨折**：导致视觉模糊（混乱效果）、最大生命值降低和虚弱效果
- **手臂骨折**：降低攻击伤害和挖掘速度（挖掘疲劳效果）
- **腿部骨折**：显著降低移动速度和跳跃能力

### 真实的治疗系统
- **手术包**：用于彻底治愈骨折，使用需要一定时间，可配置多种类型
- **止痛药**：暂时缓解骨折带来的负面效果，但不会治愈骨折

### 高度可配置
- 每种骨折的概率、效果和持续时间均可在配置文件中自定义
- 可配置多种手术包和止痛药，包括使用时间、效果持续时间和音效
- 支持多语言系统（目前支持中文和英文）

### 其他功能
- 摔落伤害系统：从高处摔落可能导致骨折，高度和伤害倍数可配置
- 骨折状态持久化：玩家的骨折状态会被保存，重新登录后依然存在
- 命令系统：管理员可以通过命令管理玩家的骨折状态和获取治疗物品

## 配置示例

```yaml
# 骨折系统配置
fracture:
  # 头部骨折
  headFracture:
    probability: 0.05  # 受伤时头部骨折概率 (5%)
    maxHealthPenalty: 2.0  # 最大生命值减少量
    maxFractures: 1  # 头部骨折最大数量

  # 手臂骨折
  armFracture:
    probability: 0.15  # 受伤时手臂骨折概率 (15%)
    miningSpeedMultiplier: 0.5  # 挖掘速度减慢倍数
    maxFractures: 2  # 手臂骨折最大数量

  # 腿部骨折
  legFracture:
    probability: 0.20  # 受伤时腿部骨折概率 (20%)
    walkSpeedMultiplier: 0.5  # 移动速度减慢至正常速度的比例
    maxFractures: 2  # 腿部骨折最大数量
```

## 命令使用

- `/fz status` - 查看你的骨折状态
- `/fz heal all` - 治愈所有骨折
- `/fz heal <head|arm|leg>` - 治愈特定部位的骨折
- `/fz reload` - 重新加载配置文件
- `/fz give painkiller [类型] [数量]` - 获取止痛药
- `/fz give firstaidkit [类型] [数量]` - 获取手术包
- `/fz help` - 显示帮助信息

## 权限节点

- `warzfracture.reload` - 允许重新加载插件配置
- `warzfracture.give` - 允许获取治疗物品

## 安装说明

1. 将插件jar文件放入服务器的 `plugins` 文件夹
2. 重启服务器或使用 `/reload` 命令
3. 根据需要修改 `config.yml` 配置文件
4. 使用 `/fz reload` 重新加载配置

## 依赖

- **必需**: Bukkit/Spigot/Paper 1.16+
- **可选**: PlaceholderAPI (用于变量支持)

## 作者信息

- **作者**: Crazy_Jky
- **联系**: QQ 1285988665
- **版本**: 1.0

## 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。