# 更新记录

## bot-0.0.4 — 2026-09-18

### 前缀修订（按部署实际配置）

- 依据用户提供的部署前缀配置，重写第 9 节前缀速查表，全部改为部署实际生效前缀，并标注与源码默认的差异（自定义/关闭强制/代码默认）。
- **鸣潮生态统一 `fb`**：XutheringWavesUID、RoverSign、RoverReminder、ScoreEcho、WavesGachaSim、WWBetaDiff、TodayEcho、XWUIDCollection、gs_kuro_cos 的源码默认 `ww` 已在部署关闭；全部命令示例从 `ww` 改为 `fb`（`fb帮助`、`fb签到`、`fbng` 等），与 GS 知识库口径一致。
- 其他前缀更新：GenshinUID 加 `ys`；StarRailUID 加 `bt`/`xqtd`/`星穹铁道`；BBBUID 加 `b3`；EndUID 加 `END`；DNAUID 加 `eclx` 系/`二重螺旋`；DeltaUID 加 `三角洲`/`sjz`；BlueArchiveUID 加 `blda`/`bl`；RocomUID 改为 `lk`/`rc`/`洛克王国`；WzryUID 前缀 `王者荣耀`；gs_kuro_cos 改为 `fb` 系。
- 说明“菲比”双通道：鸣潮系插件接受“菲比”作游戏前缀（`菲比签到`），与 AstrBot 的“菲比”唤醒前缀（`菲比helps`）互不冲突。
- 同步更新：需求入口表、快速判断（游戏类）、FAQ Q11/Q12/Q13、第 0 节前缀规则、第 13 节限制说明。

### 新增条目（部署存在但未提供仓库）

- TodayEcho（鸣潮梭哈）：命令整理自 GS 知识库（`fb梭哈`/`fb梭哈结果`/`fb梭哈列表`）。
- XWUIDCollection（鸣潮收藏）、ChatRank（群聊排行）、DeerSignCalendar（签到日历，`🦌`/`鹿`/`补签` 触发）：仅收录前缀，命令细节待提供仓库后补充。

## bot-0.0.3 — 2026-09-17

### 新增：GsCore 游戏与娱乐插件（26 个）

- 新增第 9 节总览与 9.1–9.5 分节，收录 26 个 gsuid_core 体系插件，全部基于本地源码分析。
- 前缀速查表：明确游戏命令使用游戏前缀（`gs`/`sr`/`ww`/`zzz`/`bbb`/`nte`/`end`/`pgr`/`dna`/`ss`/`ba`/`rc`/`vr`/`day`），无前缀插件（JRYS、TodayWaifu、ChisaEating、gs_kuro_cos、MomoTune）单独标注；与 BOT 功能的“菲比”前缀严格区分。
- 通用命令模式（帮助/绑定/查询/每日/签到/面板/刷新）与 pm 权限分级说明。
- 依赖关系：PGRUID、RoverSign、RoverReminder 硬依赖 XutheringWavesUID；EndUID 等可用 RemoteRender 外置渲染；ScoreEcho、WavesGachaSim 软依赖主插件。
- 已知坑与未实现功能：BBBUID 扫码登陆未注册、WavesGachaSim 抽卡统计未注册、EndUID 绑定未实现、MomoTune 酷狗源禁用、ZZZeroUID 抽卡无 URL 导入、DeltaUID 扫码使旧 token 失效等。
- 隐私/安全注意：DailyAnalyisis 归档群消息、WzryUID 小号 CK 建议、gs_kuro_cos 搬运风控、RemoteRender 无鉴权仅限内网。
- 新增游戏类与 BOT 类“快速判断”回复（9.5 与 9.9 节）、FAQ Q11–Q14（前缀混用、鸣潮双前缀、战双登录依赖、绑定方式差异）。
- 来源与版本表新增 26 行固定提交链接；勘误：StarRailUID 实际仓库为 baiqwerdvd/StarRailUID（原链接 qwerdvd 不存在）、MomoTune 实际为 MimoKit/MomoTune（原链接 Xinzhus 不存在）。
- 鸣潮前缀口径：本批插件源码为 `ww`，GS 知识库为 `fb`，知识库不强行统一，以部署实测为准。

## bot-0.0.2 — 2026-09-17

### 复审修订

- 对照本地源码复审全部关键声明：Help Typst、QQ 资料、群导出共 18 项（命令注册、权限、缓存、默认值、文件名格式、成员资格检查等）全部核验属实；群管 15 个 LLM 工具注册清单逐项确认。
- 补充说明：mcskin 插件自带用法提示仍显示斜杠形式，本部署继续按“菲比”前缀使用。
- 补充说明：helps 搜索不区分大小写。
- 修正表述：关系管理的加好友/加群扩展模块仅有占位说明，命令静默无响应，明确不作为可用功能教学。
- 统一交互确认例外：群管清理的“确认清理/取消清理”按原文回复，不加前缀的说明同步写入排错步骤与 Agent 规则。
- 修正快捷投稿话术：默认推荐带名称上传，无名称方式保留为配置视觉模型后的可选用法。

## bot-0.0.1 — 2026-09-16

### 初始化

- 建立 `fzm-fb-zsk-bot`，以 Markdown 主知识库和版本记录组织内容，参考 `Fzm-fb-zsk-gs` 的新手教程风格。
- 收录 7 个 AstrBot 插件：Help Typst、Minecraft Skin、PhoebeHub、QQ 群管、QQ 资料、关系管理、群成员信息导出。
- 统一机器人命令前缀为“菲比”，推荐前缀紧贴命令名、参数之间保留必要空格。
- 增加需求入口、分插件教程、常见问题、可复制回复、管理员带新人话术及 Agent 检索/调用边界。
- 保留 GS 游戏知识库原有游戏前缀，不将 BOT 前缀规则误用于 `fb`、`gs`、`yh` 等游戏命令。

### 准确性与权限

- 区分插件真实命令、现有 LLM 工具与未实现/未经验证的扩展，不把知识库当作执行器。
- 补充真实 @、引用消息、用户名、秒数、序号和群号的参数说明。
- 明确机器人账号资料与当前群资料、好友邀请与本群进群审核的区别。
- 明确群管清理的 AND 筛选条件、名单预览、60 秒确认窗口及交互确认文字。
- 记录群管刷屏禁言配置字段错误和跨群配置授权复核不足，禁止利用缺口执行操作。
- 核对 PhoebeHub 工具开关在调用入口检查、搜索结果数量 1～10、LLM 工具返回图片链接而非直接发送图片。
- 提醒关系管理抽查的目标/数量绑定问题、随机目标行为，以及未公开完整实现的主动加好友/加群功能。
- 明确群成员导出文件的实际接收会话、部分失败、非去重人数、上传失败反馈及内存生成行为。
- 补充资料修改、公开 PR、删除、批量群管理、跨会话数据披露和人格 Prompt 的确认/隐私要求。

### 来源与验证范围

- README 列出上游固定提交链接，便于后续更新核对。
- 本版完成文档与源码层面的整理；未在实际 AstrBot/QQ 实例逐命令执行，未验证外部服务实时可用性。
- 本仓库不包含自动安装器、插件代码、凭证、真实群成员数据或聊天记录。
