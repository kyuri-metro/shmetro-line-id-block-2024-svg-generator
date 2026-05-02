# 上海地铁线路号方块 2025 SVG Generator

> 以下内容为 GPT 5.4 生成，但经过人工正确性检查，你可以作为参考

这是 kyuri-metro 组织下的 2025 版线路号方块 SVG 生成仓库，负责提供单一的纯函数导出接口。

## 示例图

![2025 版线路号方块示例图](https://umamichi.moe/tools/shmetro-idblock/output-example-2025.webp)

统一参数规格：

- foreground
- background
- lineNumber，范围 0 至 99
- height

导出接口位于 [src/index.ts](src/index.ts)。

## 使用例

安装：

```bash
npm install @kyuri-metro/shmetro-line-id-block-2025-svg-generator
```

调用：

```ts
import { generateLineIdBlock2025Svg } from '@kyuri-metro/shmetro-line-id-block-2025-svg-generator'

const svg = generateLineIdBlock2025Svg({
	lineNumber: 21,
	height: 160,
})

document.body.innerHTML = svg
```

自定义颜色：

```ts
import { generateLineIdBlock2025Svg } from '@kyuri-metro/shmetro-line-id-block-2025-svg-generator'

const svg = generateLineIdBlock2025Svg({
	lineNumber: 26,
	height: 120,
	background: '#5F67A9',
	foreground: '#ffffff',
})
```

## 参考资料

- 2025 版参考资料位于 [docs](docs)
- 该目录仅用于仓库留档和人工比对，不参与运行时代码引用
- 该目录已加入 [.npmignore](.npmignore)，不会随 npm 包一起下载