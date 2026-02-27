# L2层网页抓取能力配置

## 状态: ✅ 已启用

---

## 工具位置

- **脚本**: `~/.openclaw/workspace/tools/l2-browser-fetch.py`
- **用途**: 使用Playwright有头浏览器抓取动态页面

---

## 使用方法

### 基本抓取
```bash
python3 tools/l2-browser-fetch.py "https://example.com"
```

### 等待特定元素加载
```bash
python3 tools/l2-browser-fetch.py "https://example.com" --wait-for "#content"
```

### 等待网络空闲
```bash
python3 tools/l2-browser-fetch.py "https://example.com" --wait-for networkidle
```

### 显示浏览器窗口（调试用）
```bash
python3 tools/l2-browser-fetch.py "https://example.com" --visible
```

### 输出JSON格式
```bash
python3 tools/l2-browser-fetch.py "https://example.com" --json
```

---

## 能力层级对比

| 层级 | 工具 | 适用场景 |
|:---|:---|:---|
| **L0** | web_search API | 快速搜索、获取URL |
| **L1** | jina.ai + curl | 静态页面、Markdown转换 |
| **L2** | **Playwright (本工具)** | **动态页面、JS渲染、复杂交互** |
| **L3** | AI视觉API | 验证码识别、图像理解 |

---

## 技术栈

- **引擎**: Playwright 1.58.0
- **浏览器**: Chromium
- **模式**: 默认无头(headless)，支持可视化

---

## 注意事项

1. **资源占用**: L2比L1更耗资源，大量抓取时注意内存
2. **反爬风险**: 频繁抓取可能触发网站防护
3. **速度**: 比L1慢，需要等待页面渲染
4. **适用**: 仅限必要场景使用，优先用L0/L1

---

_配置时间: 2026-02-27_
_版本: v1.0_
