<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <!-- 适配移动端屏幕 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        /* 重置默认样式，确保无内外边距干扰 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* 让 body 占满整个屏幕，并作为 Flex 容器实现居中 */
        body {
            min-height: 100vh; /* 高度占满视口 */
            display: flex;
            justify-content: center; /* 水平居中 */
            align-items: center; /* 垂直居中 */
            background-color: #f0f0f0; /* 背景色，可选 */
        }

        /* 变色文字样式 */
        .colorful-text {
            font-size: 3rem; /* 文字大小，可根据需求调整 */
            font-weight: bold;
            /* 动画：名称 color-change，时长 3 秒，线性循环 */
            animation: color-change 3s linear infinite;
        }

        /* 定义颜色变化动画 */
        @keyframes color-change {
            0% {
                /* hsl(色相, 饱和度, 亮度)，色相 0-360 循环 */
                color: hsl(0, 100%, 50%); /* 红色 */
            }
            20% {
                color: hsl(72, 100%, 50%); /* 黄绿色 */
            }
            40% {
                color: hsl(144, 100%, 50%); /* 绿色 */
            }
            60% {
                color: hsl(216, 100%, 50%); /* 蓝色 */
            }
            80% {
                color: hsl(288, 100%, 50%); /* 紫色 */
            }
            100% {
                color: hsl(360, 100%, 50%); /* 回到红色 */
            }
        }

        /* 响应式调整：小屏幕缩小文字尺寸 */
        @media (max-width: 768px) {
            .colorful-text {
                font-size: 2rem;
            }
        }

        @media (max-width: 480px) {
            .colorful-text {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="colorful-text">Hello</div>
</body>
</html>
