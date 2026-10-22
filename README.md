# 我的个人简历网站 — 维护手册

网站地址：https://你的用户名.github.io

## 文件说明（日常只需要改带 ★ 的）

| 文件 | 作用 |
|---|---|
| ★ `_data/news.yml` | 首页"动态"，加一条新闻就在最上面加 3 行 |
| ★ `_data/upcoming.yml` | 首页"近期安排" |
| ★ `_data/publications.yml` | 论文列表 |
| ★ `_data/presentations.yml` | 学术报告列表 |
| ★ `_data/profile.yml` | 姓名、照片、邮箱、单位、学术主页链接、最后更新日期 |
| `cv.md` / `research.md` / `links.md` | 关于我、研究、链接页面正文（Markdown） |
| `_data/navigation.yml` | 顶部导航菜单 |
| `_config.yml` | 网站标题等全局设置 |
| `assets/style.css` | 样式，换主题色改最上面的 `--accent` |
| `_layouts/default.html` | 所有页面共用的框架（页头、侧栏），一般不用动 |
| `images/` `files/` | 图片、PDF（简历、论文）放这里 |

## 最快的更新方法（只用浏览器）

1. 打开仓库，点进要改的文件（比如 `_data/news.yml`）
2. 点右上角铅笔图标 ✏️
3. 修改后点 **Commit changes**
4. 等 1–2 分钟，刷新网站即可看到

上传图片/PDF：进入 `images` 或 `files` 文件夹 → **Add file → Upload files**。

## YAML 注意事项（出错最常见的原因）

- 缩进只能用**空格**，不能用 Tab
- 冒号后面要有一个空格：`date: 2026-10-22`
- 内容里有英文冒号 `:` 或以 `*` 开头时，用双引号把整段包起来
- 改完如果网站没变化：仓库 **Actions** 页签里看是否有红色 ✗，点进去能看到报错行号

## 新增一个页面

1. 新建 `teaching.md`，开头写：
   ```
   ---
   layout: default
   title: 教学
   ---
   # 教学
   正文……
   ```
2. 在 `_data/navigation.yml` 加：
   ```
   - title: 教学
     url: /teaching.html
   ```

## 长期维护建议

- 每次有新论文/报告/获奖，当天就加进 yml，顺手改 `profile.yml` 里的 `last_update`
- 每年年初检查一次：单位、职位、照片、外部链接是否失效
- 想用自己的域名：仓库 Settings → Pages → Custom domain
