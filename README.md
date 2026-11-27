# TVBox 接口私有化仓库

本仓库由 https://github.com/fish2018/tvbox 项目自动生成与维护，作用是把网上重复率高、失效多的 TVBox 接口整理成一份干净的私有配置。感谢大佬提供的工具！

## 一、APP 配置地址（影视仓 / TVBox 直接用这个）

| 用途 | 地址 |
|---|---|
| 全量线路（推荐，历史累计去重） | `https://ghproxy.net/https://raw.githubusercontent.com/joelee7928/tvbox/main/all.json` |
| 本次抓取线路 | `https://ghproxy.net/https://raw.githubusercontent.com/joelee7928/tvbox/main/tvbox.json` |

> 备用加速：把地址前缀 `https://ghproxy.net/` 换成 `https://gh-proxy.com/`，
> 或改用 jsDelivr 形式 `https://cdn.jsdmirror.com/gh/joelee7928/tvbox@main/all.json`。

在影视仓/TVBox 里：设置 → 配置地址 → 粘贴上面的地址 → 确定 → 重启应用。

## 二、当前数据源

**多仓源**（展开取其前 5 个仓库源）

| 源 | 地址 |
|---|---|
| 小盒子多仓 | `http://xhztv.top/dc` |
| 拾光多仓 | `http://xmbjm.fh4u.org/dc.txt` |
| 挺好分享 GYCK | `http://ztha.top/TVBox/GYCK.json` |

**单仓源**（整仓私有化，逐条线路存为 txt）

| 源 | 站点数 | 地址 |
|---|---|---|
| 俊佬在线 | 24 | `http://home.jundie.top:81/top98.json` |
| 嗷呜 | 80 | `https://9763.kstore.vip/aowu.json` |
| FongMI 线路 | 33 | `https://raw.githubusercontent.com/gaotianliuyun/gao/master/0827.json` |

多仓展开时只取每个仓的前 5 个仓库源（`num=5`），避免一次拉取过多失效线路拖慢速度。

## 三、仓库结构

```
*.txt           各线路的私有化配置（去重、去 emoji、失效线路已剔除）
jar/            本地化的 spider jar 包（避免原站挂掉后线路失效）
all.json        所有历史线路汇总（去重），APP 推荐用这个
tvbox.json      最近一次抓取的线路集合
README.md       本说明
```
