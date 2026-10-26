# 余婉瑜的自我介绍页

一个纯静态的小页面，手写的 HTML + CSS，没有框架、没有构建步骤。

- `index.html` —— 源文件，图片从 `assets/` 引用
- `余婉瑜.html` —— 同一页面的单文件版，图片已 base64 内嵌，可以直接双击打开或发给别人
- `assets/portrait.png` —— 页头立绘
- `assets/avatar-*.jpg`、`assets/sticker-*.png` —— 头像与表情包
- `page-shot.png` —— 整页截图（headless Chrome 渲染后裁剪）

改完页面之后重出截图：

```sh
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless=new --disable-gpu --hide-scrollbars \
  --window-size=1000,2400 --screenshot=/tmp/p.png \
  "file://$PWD/index.html"
```

单文件版由 `index.html` 把 `src="assets/..."` 换成 base64 生成，`alt`、类名等不受影响。
