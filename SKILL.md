---
name: knowledge-learner
description: AI as导师，为任意学科创建30-60天系统学习课程，生成12课HTML学习网站
description_zh: AI导师引导的系统学习课程生成器 - 为任意学科创建12课HTML学习网站
version: 1.0.0
author: WorkBuddy User
tags:
  - learning
  - education
  - course-generator
  - html
  - interactive
---

# Knowledge Learner SKILL

AI 扮演导师角色，为用户创建一套完整的系统学习课程（HTML 网站形式）。

---

## 激活条件

当用户表达以下意图时，激活此 SKILL：

- "帮我学 XXX" / "我想学 XXX"
- "创建一个学习课程"
- "做一个 XXX 的教学网站"
- "用知识掌握学习规划器"
- 任何要求系统学习某个学科/主题的请求

---

## 执行流程

### 步骤 1：确认学习主题

与用户确认以下信息（至少确认前两项）：

1. **学习主题**：要学习什么领域？（如：浪漫主义、宋元山水、存在主义）
2. **经典著作/主线**：选择 1 本经典作为学习主线（如：《浪漫主义的根源》）
3. **学习时长**：30天（精简版）或 60天（完整版）
4. **特定目标**：用户想达到什么程度？需要产出什么？

### 步骤 2：设计 12 课框架

根据主题特点，设计 12 课结构：

```
第1课：导入与基础概念
第2课：历史背景与学科起源
第3课：核心理论/方法论
第4课：第一位大师 + 代表作品
第5课：第二位大师 + 代表作品
第6课：对比分析（两种风格的碰撞）
第7课：演变与创新
第8课：第三位大师 + 代表作品
第9课：第四位大师 + 代表作品
第10课：综合理解
第11课：深度专题（时间/空间/哲学维度）
第12课：总结与当代意义
```

可根据学科特点灵活调整。

### 步骤 3：内容创作标准

每课必须包含以下要素：

1. **核心概念**：200-400 字，解释关键术语
2. **经典案例分析**：选取 1-2 个代表性案例深入分析
3. **原文引用**：引用一手文献/经典原句
4. **概念框**：用特殊样式突出重要术语
5. **视觉资源**：1-2 幅经典图像/案例图片
6. **思考练习**：3 道题目
7. **参考答案**：每道题详细展开（至少 300 字）

### 步骤 4：三个层次写作

每个知识点都要覆盖：

1. **是什么**：基础定义和概念
2. **为什么**：历史背景和深层原因
3. **意味着什么**：对后世的影响和当代意义

### 步骤 5：技术实现

生成单页 HTML 应用：

- 响应式设计（适配手机/平板/桌面）
- 语义化 HTML 结构
- 模块化 CSS
- 原生 JavaScript（无框架依赖）

### 步骤 6：必含功能组件

1. **导航系统**：顶部固定导航 + 课程目录 + 平滑滚动 + 当前章节高亮
2. **课程卡片**：标题 + 导入段落 + 内容区域
3. **作品卡片**：图片 + 标题 + 作者/年代/收藏地 + 描述
4. **概念框**：渐变背景样式，突出重点术语
5. **引用框**：原文献引用样式
6. **思考练习区**：黄色边框醒目样式
7. **答案展开按钮**：点击展开/收起参考答案

---

## 输出规范

### 文件位置

保存到用户工作目录（默认为 D:\WORKBUDDY），文件名格式：

```
{主题名}-学习课程.html
```

如：`浪漫主义学习课程.html`

### 质量检查清单

生成完成后，自检以下项目：

- [ ] 每课有明确的学习目标
- [ ] 核心概念至少出现 3 次
- [ ] 至少有 6 幅高清图片（使用可靠图源）
- [ ] 每课有 3 道思考练习
- [ ] 每道练习有详细参考答案（300+ 字）
- [ ] 术语解释清晰准确
- [ ] 引用来源可靠
- [ ] 导航链接全部有效
- [ ] 图片正常加载
- [ ] 答案展开/收起正常
- [ ] 移动端显示正常

---

## 代码模板参考

### HTML 课程模板

```html
<div id="lessonX" class="lesson">
    <h3 class="lesson-title">第X课：[课程主题]</h3>
    
    <!-- 导入段落 -->
    <p>...</p>
    
    <!-- 核心概念 -->
    <div class="concept-box">
        <h4>关键概念</h4>
        <p>...</p>
    </div>
    
    <!-- 作品分析 -->
    <div class="artwork-card">
        <img src="..." alt="...">
        <div class="artwork-info">
            <h4 class="artwork-title">《作品名》</h4>
            <p class="artwork-meta">作者 | 年代 | 收藏地</p>
            <p class="artwork-desc">...</p>
        </div>
    </div>
    
    <!-- 引用框 -->
    <div class="quote-box">
        <p>...</p>
        <p class="author">——来源</p>
    </div>
    
    <!-- 思考练习 -->
    <div class="practice-section">
        <h4>思考练习</h4>
        <ol>
            <li>...</li>
            <li>...</li>
            <li>...</li>
        </ol>
        <button class="answer-toggle" onclick="toggleAnswer(this)">
            <span>查看参考答案</span>
        </button>
        <div class="answer-content">
            <h5>参考答案</h5>
            <p><strong>问题1：</strong>...</p>
        </div>
    </div>
</div>
```

### CSS 样式要点

```css
/* 课程卡片 */
.lesson {
    margin: 30px 0;
    padding: 25px;
    background: #faf8f5;
    border-radius: 12px;
    border-left: 4px solid #0f3460;
}

/* 概念框 - 渐变背景 */
.concept-box {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 30px;
    border-radius: 15px;
}

/* 思考练习 - 黄色边框 */
.practice-section {
    background: #fff3cd;
    border: 2px solid #ffc107;
    padding: 25px;
    border-radius: 12px;
}

/* 答案展开 */
.answer-content {
    display: none;
    margin-top: 20px;
    padding: 25px;
    background: white;
    border-radius: 12px;
}

.answer-content.show {
    display: block;
}
```

### JavaScript 交互

```javascript
// 展开/收起答案
function toggleAnswer(button) {
    const answerContent = button.nextElementSibling;
    button.classList.toggle('active');
    
    if (answerContent.classList.contains('answer-content')) {
        answerContent.classList.toggle('show');
        const span = button.querySelector('span');
        span.textContent = answerContent.classList.contains('show') 
            ? '收起参考答案' 
            : '查看参考答案';
    }
}

// 平滑滚动导航
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        document.querySelector(this.getAttribute('href')).scrollIntoView({
            behavior: 'smooth'
        });
    });
});
```

---

## 示例主题参考

| 主题 | 经典著作 | 建议时长 |
|------|----------|----------|
| 浪漫主义 | 《浪漫主义的根源》(以赛亚·柏林) | 30天 |
| 宋元山水 | 《林泉高致》+ 《中国绘画三千年》 | 30天 |
| 存在主义 | 《存在与虚无》(萨特) | 60天 |
| 印象派 | 《印象派绘画史》 | 30天 |
| 文艺复兴 | 《意大利文艺复兴的艺术》 | 60天 |

---

## 使用示例

用户只需说：
> "帮我做一个关于浪漫主义的学习课程"

AI 即可自动完成：
1. 确认主题与经典著作
2. 设计 12 课大纲
3. 生成完整的 HTML 学习网站
4. 交付可直接打开使用的 `浪漫主义学习课程.html`

---

## 注意事项

1. **一本书主义**：始终选择 1 本经典著作作为学习主线，避免贪多
2. **学者深度**：目标是大专水平，不是科普水平
3. **原创内容**：不要复制现有课程，要基于经典著作原创讲解
4. **视觉质量**：图片使用博物馆/学术资源的高清版本
5. **互动设计**：思考练习是核心价值，每题都要有深度参考答案
