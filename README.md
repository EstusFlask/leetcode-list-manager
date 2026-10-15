# 力扣题单批量管理器

A userscript for bulk selection and problem-list management on LeetCode CN (`leetcode.cn`). The guide below is in Chinese.

适用于 `https://leetcode.cn/problem-list/*` 的油猴脚本。它会在题单的每一道题前加入复选框，并在页面底部提供批量工具栏。

## 功能

- 多选当前题单中的题目，滚动虚拟列表后仍保留选择
- 将所选题目一次添加到任意自建题单
- 从当前题单批量移除所选题目
- 按选择顺序将所选题目批量置顶
- 适配力扣的 SPA 导航、深色主题和窄屏布局

## 安装

1. 在 Chrome 安装 Tampermonkey（篡改猴）等用户脚本管理器。
2. 打开 [`leetcode-list-manager.user.js`](./leetcode-list-manager.user.js)，点击 **Raw**，让脚本管理器进入安装页；也可将完整脚本复制到新脚本编辑器。
3. 在脚本管理器的安装页确认安装。
4. 登录力扣中国站并打开任意自建题单。

## 使用说明

页面底部会出现“批量管理”工具栏。“选择可见”只选择当前已经渲染的题目；逐个勾选的结果会在滚动时保留。移除和置顶会在实际修改前再次确认。

脚本使用力扣同源 `/graphql/` 接口，并复用当前浏览器登录态及请求所需的会话/CSRF 字段，不提供独立的账号登录功能。
