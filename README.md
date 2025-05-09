
# AI 增强型交易系统（AIDev）

📈 这是一个用于黄金（XAUUSD）、美股指数（NAS100、SP500）的 AI 增强型交易系统，包含：

- TradingView 指标（Pine Script v5）
- MetaTrader 5 Expert Advisor（MQL5）
- 新闻自动抓取 + AI 情绪判断
- Telegram 实时推送信号

## 📦 功能亮点

| 模块 | 功能 |
|------|------|
| 📊 技术分析 | 斐波那契回撤、EMA 共振、GMMA、VSA 成交量分析 |
| 🧠 AI 信号判断 | 使用 GPT/Qwen/Claude 判断市场情绪 |
| 📰 新闻抓取 | 来自 Investing.com、ForexFactory、Bloomberg |
| 🤖 Telegram Bot | 实时推送 AI 判断结果 |
| 💻 回测支持 | 可导出 CSV 数据供 Backtrader / QuantConnect 使用 |

## 📥 如何使用？

### 1. 获取 TradingView 指标
- 将 `indicators/fib_ema_strategy.pine` 导入 TradingView
- 设置 Webhook 地址为你的服务器（如 Flask）

### 2. 在 MT5 中运行 EA
- 编译 `mt5_ea/Fib_EMA_SupplyDemand.mq5`
- 加载后连接 VPS 或本地服务器获取 AI 信号

### 3. 部署 Telegram Bot
- 修改 `config.py` 中的 `TELEGRAM_BOT_TOKEN` 和 `CHAT_ID`
- 启动 Flask 服务或部署到 PythonAnywhere

### 4. 自动抓取新闻并分析
- 运行 `news_scraper.py` 自动获取宏观事件
- 运行 `ai_signal_analyzer.py` 获取 AI 判断结果

## 📚 开发者贡献

欢迎提交 PR 和 Issue。请阅读 [CONTRIBUTING.md](CONTRIBUTING.md) 获取更多信息。

![image](https://github.com/user-attachments/assets/904350fb-75b1-4521-8c7b-52930cdea872)


# AI Enhanced Trading System

📈 这是一个用于黄金（XAUUSD）、美股指数（NAS100、SP500）和外汇市场的 AI 增强型交易系统。

## 功能模块

- 📈 TradingView Pine Script 指标（带英文注释）
- 📊 AI 信号判断模块（GPT/Qwen/Claude）
- 🤖 Telegram Bot 推送模块
- 📰 新闻自动抓取 + 解析
- 💻 MetaTrader 5 EA 支持

## 如何使用？

1. 将 `indicators/fib_ema_strategy.pine` 导入 TradingView
2. 在 MT5 中加载 `mt5_ea/Fib_EMA_SupplyDemand.mq5`
3. 修改 `config.py` 中的 API Key 和 Telegram Token
4. 启动 Flask Webhook 服务
5. 运行 `news_scraper.py` 获取实时新闻
6. 使用 `ai_signal_analyzer.py` 获取 AI 判断结果

