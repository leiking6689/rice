# 天工开物 · 水稻古今对话（教学网页 GitHub Pages 部署包）

上海金山杭州湾双语学校 生物教学用知识网页：《天工开物·乃粒》古法稻作七步 ↔ 现代杂交水稻，附白描动画与三道模考案例练习。

## 目录结构

```
tiangong-rice/
├── index.html                          # 网页本体（单文件，内联 CSS/JS）
├── 成片/
│   └── 天工开物水稻种植流程动画_成片.mp4   # 84.7 秒白描版画动画（h264/aac）
├── 图片/
│   ├── yadao_1.png                     # 鸭稻共作照片（俯视）
│   └── yadao_3.png                     # 鸭稻共作照片（平视）
└── .nojekyll                           # 关闭 Jekyll，保证中文路径原样可访问
```

网页为纯静态页面，无构建步骤、无外部 CSS/JS 依赖；直接双击 index.html 也可离线使用。

## 部署到 GitHub Pages（约 3 分钟）

1. 在 GitHub 新建仓库，例如 tiangong-rice（建议 Public）。
2. 把本文件夹内的全部内容上传到仓库根目录（index.html 必须在根目录）。
   - 网页方式：仓库页 Add file → Upload files，拖入全部文件和文件夹后 Commit。
   - 命令行方式：
     git init && git add . && git commit -m "tiangong rice" 
     git branch -M main
     git remote add origin https://github.com/<你的用户名>/tiangong-rice.git
     git push -u origin main
3. 打开仓库 Settings → Pages：Source 选 Deploy from a branch；Branch 选 main / (root)，保存。
4. 约 1 分钟后访问：https://<你的用户名>.github.io/tiangong-rice/

## 注意事项

- .nojekyll 必须保留，否则 Jekyll 可能影响中文目录（成片/、图片/）访问。
- 视频约 29MB；网页已配置在线备用源 + 本地相对路径双保险。
- 鸭稻照片优先在线地址、失败自动回退包内 图片/ 文件。
- 离线课堂：整个文件夹拷到教室电脑，双击 index.html 即可。
