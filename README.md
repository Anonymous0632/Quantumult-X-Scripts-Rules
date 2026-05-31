# Quantumult X Scripts Rules

![preview](./quantumult配置示例.png)

[![Anonymous0632's GitHub stats](https://github-readme-stats.vercel.app/api?username=Anonymous0632)](https://github.com/Anonymous0632/Quantumult-X-Scripts-Rules)

## 语言 / Languages

- [中文说明](#中文说明)
- [English](#english)

## 中文说明

这是自用的 Quantumult X 配置文件，已经覆盖常用的国内外分流、广告拦截、重写、脚本任务和部分解锁场景。配置整体以日常使用稳定性和去广告完整度为主，规则大约 80% 来自其他开源项目，剩余部分结合个人使用习惯补充和调整。

如果发现规则失效、误拦截或上游资源变更，会不定期基于本地最新配置文件更新。

### 最新配置

| 项目 | 内容 |
| --- | --- |
| 最新配置文件 | [`quantumult_20260531224706.conf`](./quantumult_20260531224706.conf) |
| 更新时间 | 2026-05-31 22:47:06 |
| 本次 README 来源 | 以仓库内本地最新配置文件为准 |
| 主要模块 | `general`、`dns`、`policy`、`filter_remote`、`filter_local`、`rewrite_remote`、`task_local`、`mitm` |

### 功能概览

- 国内网站和服务优先直连，常见境外网站按规则或 GeoIP 分流。
- 集成多个广告拦截、隐私保护和运营商劫持过滤规则。
- 内置常用服务策略组，包括 AI、Telegram、YouTube、Netflix、Disney+、Spotify、Twitter、PayPal、Facebook、Reddit、Discord、BiliBili、TikTok、游戏、媒体、金融、Apple 和 Microsoft 服务等。
- DNS 配置包含 DoH3、常用公共 DNS、IPv6 DNS 以及部分国内服务的指定解析。
- 集成部分 iRingo、DualSubs、BoxJs、去广告重写、签到任务和流媒体解锁检测脚本。

### 使用方法

1. 自行准备代理节点或机场订阅。
2. 在 Quantumult X 中配置并信任 MITM 证书。具体步骤可参考 @Shawn 的 [Quantumult X 不完全指南](https://www.notion.so/Quantumult-X-1d32ddc6e61c4892ad2ec5ea47f00917#bb2dce7c01114955bbdbbd222f2a5fcf)。
3. 使用 Safari 或系统文件管理下载 [`quantumult_20260531224706.conf`](./quantumult_20260531224706.conf)。
4. 打开 Quantumult X，点击右下角设置按钮。
5. 进入「配置文件」模块，选择「导入配置」。
6. 在文件管理器中选择下载的 `.conf` 文件。
7. 点击右上角确认。导入后请自行添加或替换代理节点，并检查 `[mitm]` 中的证书、密码和 `hostname` 是否适合你的设备。

### DNS 推荐

以下 DNS 已包含在最新配置文件中，实际生效情况以 Quantumult X 配置为准。

```text
https://doh.pub/dns-query
119.29.29.29
114.114.114.114
202.141.176.93
202.141.178.13
117.50.10.10
223.5.5.5
119.28.28.28
8.8.8.8
1.1.1.1
[2400:3200::1]
[2400:3200:baba::1]
[2402:4e00::]
[2606:4700:4700::1111]
[2606:4700:4700::1001]
[2a07:a8c0::74:d6b8]
[2a07:a8c1::74:d6b8]
```

### 资源解析器

配置使用 KOP-XIAO 的 Quantumult X 资源解析器：

```text
resource_parser_url=https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/resource-parser.js
```

### 注意事项

- 配置文件不会包含你的机场订阅、代理节点账号或个人 Token，请自行添加。
- 最新本地配置包含 `[mitm]` 段，公开发布或分享前请确认其中的证书信息是否需要删除或替换。
- BoxJs 需要单独手动配置，具体参考 [Chavy / BoxJs 文档](https://docs.boxjs.app/)。
- 重写、解锁和去广告规则可能受上游维护状态影响，遇到异常时建议先禁用对应远程资源排查。
- 使用 MITM、重写脚本和第三方规则前，请自行确认所在地区法律法规和应用服务条款。

### 致谢

排名不分先后。感谢以下项目和作者的规则、脚本与长期维护：

* [Semporia](https://github.com/Semporia)
* [scomper](https://github.com/scomper/Surge)
* [zqzess](https://github.com/zqzess)
* [han3013](https://github.com/han3013?tab=repositories)
* [chouchoui](https://github.com/chouchoui)
* [zZPiglet](https://github.com/zZPiglet/Task/tree/master)
* [app2smile](https://github.com/app2smile)
* [smartmimi](https://github.com/smartmimi/conf/tree/master)
* [id77](https://github.com/id77)
* [MuTu](https://github.com/githubdulong/Script)
* [Keywos](https://github.com/Keywos)
* [Yichahucha](https://github.com/yichahucha/surge/tree/master)
* [Hackl0us](https://github.com/Hackl0us)
* [NobyDa](https://github.com/NobyDa)
* [VirgilClyne](https://github.com/VirgilClyne)
* [KOP-XIAO](https://github.com/KOP-XIAO)
* [Peng-YM](https://github.com/Peng-YM)
* [Chavy](https://github.com/chavyleung)
* [nzw9314](https://github.com/nzw9314)
* [Tartarus2014](https://github.com/Tartarus2014)
* [Rabbit-Spec](https://github.com/Rabbit-Spec/Surge)
* [MartinsKing](https://github.com/ClydeTime?tab=repositories)
* [ExaAlice](https://github.com/ExaAlice/Alice)
* [Alexandr Garbuzov](https://github.com/anuraghazra/github-readme-stats/blob/master/docs/readme_cn.md)
* [Orz-3](https://github.com/Orz-3)
* [ConnersHua](https://github.com/DivineEngine/Profiles/tree/master)
* [mieqq](https://github.com/mieqq/mieqq)
* [Yachen Liu](https://github.com/Blankwonder)
* [maicoo](https://github.com/blankmagic/surge)

欢迎 Star。

### 免责声明

- 项目内所涉及脚本、LOGO 仅为资源共享和学习参考目的，不保证其合法性、正当性、准确性，请勿用于任何商业用途或牟利。
- 遵循避风港原则，若有图片和内容侵权，请在 Issues 告知，核实后删除，其版权均归原作者及其网站所有。
- 本人不对任何内容承担任何责任，包括但不限于任何内容错误导致的任何损失、损害。
- 任何人通过任何方式访问、使用或转载项目相关资源，即视为已接受本免责声明。
- 本项目内所有资源文件，禁止任何公众号、自媒体进行任何形式的转载、发布。
- 本项目涉及的数据由使用的个人或组织自行填写，本项目不对数据内容负责，包括但不限于数据的真实性、准确性、合法性。
- 本项目中涉及的第三方硬件、软件等，与本项目没有任何直接或间接关系。本项目仅对部署和使用过程进行客观描述，不代表支持使用任何第三方硬件、软件。
- 本项目中所有内容只供学习和研究使用，不得用于违反国家、地区、组织法律法规或相关规定的用途。
- 所有基于本项目源代码进行的任何修改，均为其他个人或组织的自发行为，与本项目没有任何直接或间接关系。
- 所有直接或间接使用本项目的个人和组织，应在 24 小时内完成学习和研究，并及时删除本项目中的所有内容。如对功能有需求，应自行开发相关功能。
- 本项目保留随时对免责声明进行补充或更改的权利。

## English

This repository contains a personal Quantumult X configuration. It covers common domestic and international routing, ad blocking, rewrites, scheduled scripts, and selected unlock scenarios. The configuration focuses on day-to-day stability and a high level of ad-blocking coverage. Around 80% of the rules come from other open-source projects, while the rest is adjusted for personal usage.

The project will be updated from time to time based on the latest local configuration file in this repository.

### Latest Configuration

| Item | Value |
| --- | --- |
| Latest config file | [`quantumult_20260531224706.conf`](./quantumult_20260531224706.conf) |
| Updated at | 2026-05-31 22:47:06 |
| README source | Generated from the latest local config file in this repository |
| Main sections | `general`, `dns`, `policy`, `filter_remote`, `filter_local`, `rewrite_remote`, `task_local`, `mitm` |

### Features

- Domestic websites and services are routed directly when possible; common international services are routed by rules or GeoIP.
- Multiple ad-blocking, privacy-protection, and carrier-hijacking filters are included.
- Built-in policy groups cover AI, Telegram, YouTube, Netflix, Disney+, Spotify, Twitter, PayPal, Facebook, Reddit, Discord, BiliBili, TikTok, gaming, media, finance, Apple, Microsoft, and more.
- DNS settings include DoH3, common public DNS servers, IPv6 DNS servers, and domain-specific DNS routing for selected Chinese services.
- The configuration includes selected iRingo, DualSubs, BoxJs, ad-blocking rewrites, scheduled tasks, and streaming unlock check scripts.

### How to Use

1. Prepare your own proxy nodes or airport subscription.
2. Configure and trust the MITM certificate in Quantumult X. For the general process, see @Shawn's [Quantumult X guide](https://www.notion.so/Quantumult-X-1d32ddc6e61c4892ad2ec5ea47f00917#bb2dce7c01114955bbdbbd222f2a5fcf).
3. Download [`quantumult_20260531224706.conf`](./quantumult_20260531224706.conf) with Safari or the system file manager.
4. Open Quantumult X and tap the settings button in the bottom-right corner.
5. Go to the "Profiles" section and choose "Import Profile".
6. Select the downloaded `.conf` file from the file manager.
7. Confirm the import. After importing, add or replace your proxy nodes and review the certificate, passphrase, and `hostname` values in the `[mitm]` section for your own device.

### Recommended DNS

The following DNS servers are already included in the latest config file. The actual behavior depends on the Quantumult X runtime configuration.

```text
https://doh.pub/dns-query
119.29.29.29
114.114.114.114
202.141.176.93
202.141.178.13
117.50.10.10
223.5.5.5
119.28.28.28
8.8.8.8
1.1.1.1
[2400:3200::1]
[2400:3200:baba::1]
[2402:4e00::]
[2606:4700:4700::1111]
[2606:4700:4700::1001]
[2a07:a8c0::74:d6b8]
[2a07:a8c1::74:d6b8]
```

### Resource Parser

This configuration uses KOP-XIAO's Quantumult X resource parser:

```text
resource_parser_url=https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/resource-parser.js
```

### Notes

- This config does not include your airport subscription, proxy account, or personal tokens. Add them yourself.
- The latest local config includes a `[mitm]` section. Before publishing or sharing it, review whether the certificate data should be removed or replaced.
- BoxJs must be configured separately. See the [Chavy / BoxJs documentation](https://docs.boxjs.app/).
- Rewrites, unlock scripts, and ad-blocking rules depend on upstream maintainers. If something breaks, disable the related remote resource first for troubleshooting.
- Before using MITM, rewrite scripts, or third-party rules, make sure you comply with local laws, regulations, and app terms of service.

### Credits

In no particular order. Thanks to the following projects and authors for their rules, scripts, and maintenance:

* [Semporia](https://github.com/Semporia)
* [scomper](https://github.com/scomper/Surge)
* [zqzess](https://github.com/zqzess)
* [han3013](https://github.com/han3013?tab=repositories)
* [chouchoui](https://github.com/chouchoui)
* [zZPiglet](https://github.com/zZPiglet/Task/tree/master)
* [app2smile](https://github.com/app2smile)
* [smartmimi](https://github.com/smartmimi/conf/tree/master)
* [id77](https://github.com/id77)
* [MuTu](https://github.com/githubdulong/Script)
* [Keywos](https://github.com/Keywos)
* [Yichahucha](https://github.com/yichahucha/surge/tree/master)
* [Hackl0us](https://github.com/Hackl0us)
* [NobyDa](https://github.com/NobyDa)
* [VirgilClyne](https://github.com/VirgilClyne)
* [KOP-XIAO](https://github.com/KOP-XIAO)
* [Peng-YM](https://github.com/Peng-YM)
* [Chavy](https://github.com/chavyleung)
* [nzw9314](https://github.com/nzw9314)
* [Tartarus2014](https://github.com/Tartarus2014)
* [Rabbit-Spec](https://github.com/Rabbit-Spec/Surge)
* [MartinsKing](https://github.com/ClydeTime?tab=repositories)
* [ExaAlice](https://github.com/ExaAlice/Alice)
* [Alexandr Garbuzov](https://github.com/anuraghazra/github-readme-stats/blob/master/docs/readme_cn.md)
* [Orz-3](https://github.com/Orz-3)
* [ConnersHua](https://github.com/DivineEngine/Profiles/tree/master)
* [mieqq](https://github.com/mieqq/mieqq)
* [Yachen Liu](https://github.com/Blankwonder)
* [maicoo](https://github.com/blankmagic/surge)

Stars are welcome.

### Disclaimer

- The scripts and logos in this project are provided only for resource sharing, learning, and research. Their legality, legitimacy, and accuracy are not guaranteed. Do not use this project for commercial purposes or profit.
- This project follows the safe-harbor principle. If any image or content infringes your rights, please open an Issue. It will be removed after verification. Copyright belongs to the original authors and websites.
- The author is not responsible for any content in this project, including but not limited to any loss or damage caused by incorrect content.
- Anyone who accesses, uses, or redistributes any resource from this project is deemed to have accepted this disclaimer.
- All resource files in this project may not be republished by public accounts, self-media, or similar channels in any form.
- Data involved in this project is filled in by users or organizations themselves. This project is not responsible for the authenticity, accuracy, or legality of that data.
- Third-party hardware, software, or services mentioned in this project have no direct or indirect relationship with this project. This project only describes deployment and usage objectively.
- All content in this project is for learning and research only. It must not be used for purposes that violate laws, regulations, or related rules of any country, region, or organization.
- Any modification based on this project is a voluntary action by other individuals or organizations and has no direct or indirect relationship with this project.
- Individuals and organizations that directly or indirectly use this project should complete learning and research within 24 hours and delete all project content in time. If you need related functionality, develop it yourself.
- This project reserves the right to supplement or change this disclaimer at any time.
