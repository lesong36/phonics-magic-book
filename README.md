# 英语自然拼读魔法书

面向儿童的互动自然拼读课件，内容包括音节、元音、辅音、常见字母组合和特殊拼读规则。

在线版本由 GitHub Pages 提供；发布文件位于 [`docs/index.html`](docs/index.html)。浏览器的语音合成功能用于单词朗读，推荐使用最新版 Chrome、Edge 或 Safari。

## 本地预览

```bash
python3 -m http.server 8000 --directory docs
```

随后在浏览器打开 `http://localhost:8000`。

## 更新网页

编辑并运行 `notebook.ipynb` 后，在项目根目录执行：

```bash
jupyter nbconvert --to html --template lab --no-input --output index --output-dir docs notebook.ipynb
```

提交并推送 `notebook.ipynb` 与 `docs/index.html` 后，GitHub Pages 会自动更新。

## 发布说明

网页不包含 Azure Speech 密钥。若未在浏览器中配置 Azure 密钥，朗读功能会自动使用浏览器自带语音。
