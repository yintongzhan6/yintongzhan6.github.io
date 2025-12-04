<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>殷统占 - 个人简历</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Microsoft Yahei", "PingFang SC", sans-serif;
        }

        body {
            background-color: #f8f9fa;
            padding: 30px 20px;
            line-height: 1.6;
        }

        .resume-container {
            max-width: 850px;
            margin: 0 auto;
            background-color: #fff;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 2px 20px rgba(0,0,0,0.08);
        }

        /* 头部样式优化 */
        .header {
            text-align: center;
            margin-bottom: 40px;
            padding-bottom: 25px;
            border-bottom: 2px solid #f0f2f5;
            position: relative;
        }

        .header::after {
            content: "";
            display: block;
            width: 80px;
            height: 3px;
            background-color: #2c6ecb;
            margin: 15px auto 0;
            border-radius: 3px;
        }

        .header h1 {
            font-size: 32px;
            color: #2d3748;
            margin-bottom: 12px;
            font-weight: 600;
        }

        .header .basic-info {
            font-size: 16px;
            color: #4a5568;
            letter-spacing: 0.5px;
        }

        /* 板块样式优化 */
        .section {
            margin-bottom: 35px;
        }

        .section h2 {
            font-size: 22px;
            color: #2d3748;
            margin-bottom: 20px;
            padding-left: 12px;
            border-left: 4px solid #2c6ecb;
            font-weight: 600;
            display: flex;
            align-items: center;
        }

        .section h2::before {
            content: "";
            display: inline-block;
            width: 6px;
            height: 6px;
            background-color: #2c6ecb;
            border-radius: 50%;
            margin-right: 8px;
        }

        .section .content {
            color: #4a5568;
            font-size: 16px;
            padding-left: 20px;
        }

        /* 教育经历样式 */
        .education-list {
            list-style: none;
        }

        .education-list li {
            margin-bottom: 15px;
            padding: 12px 15px;
            border-bottom: 1px dashed #e2e8f0;
            display: flex;
            align-items: center;
            transition: background-color 0.3s ease;
        }

        .education-list li:hover {
            background-color: #f8f9fa;
            border-radius: 6px;
        }

        .education-list li span {
            font-weight: 600;
            color: #2d3748;
            min-width: 60px;
            display: inline-block;
        }

        /* 个人特质样式 */
        .personal-trait {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 15px;
        }

        .trait-item {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            border-left: 3px solid #2c6ecb;
        }

        .trait-item p {
            margin: 0;
            display: flex;
            align-items: flex-start;
        }

        .trait-item p::before {
            content: "●";
            color: #2c6ecb;
            margin-right: 8px;
            font-size: 14px;
            margin-top: 4px;
        }

        /* 联系方式样式 */
        .contact-list {
            list-style: none;
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }

        .contact-list li {
            display: flex;
            align-items: center;
            padding: 8px 15px;
            background-color: #f8f9fa;
            border-radius: 6px;
            transition: all 0.3s ease;
        }

        .contact-list li:hover {
            background-color: #e8f0fe;
            transform: translateY(-2px);
        }

        .contact-list li::before {
            content: "";
            display: inline-block;
            width: 20px;
            height: 20px;
            margin-right: 8px;
            background-size: contain;
            background-repeat: no-repeat;
        }

        .contact-list li:first-child::before {
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='%232c6ecb'%3E%3Cpath d='M20 2H4c-1.1 0-1.99.9-1.99 2L2 22l4-4h14c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2zm-2 12H6v-2h12v2zm0-3H6V9h12v2zm0-3H6V6h12v2z'/%3E%3C/svg%3E");
        }

        .contact-list li:last-child::before {
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='%232c6ecb'%3E%3Cpath d='M18 2H6c-1.1 0-2 .9-2 2v16c0 1.1.9 2 2 2h12c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2zM6 4h5v8l-2.5-1.5L6 12V4z'/%3E%3C/svg%3E");
        }

        .contact-list li a {
            color: #2c6ecb;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .contact-list li a:hover {
            color: #1a4b94;
            text-decoration: underline;
        }

        /* 响应式优化 */
        @media (max-width: 768px) {
            .resume-container {
                padding: 25px;
            }

            .header h1 {
                font-size: 28px;
            }

            .section h2 {
                font-size: 20px;
            }

            .section .content {
                font-size: 15px;
                padding-left: 10px;
            }

            .contact-list {
                flex-direction: column;
                gap: 12px;
            }

            .personal-trait {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            .resume-container {
                padding: 20px 15px;
            }

            .header h1 {
                font-size: 24px;
            }

            .education-list li {
                padding: 10px;
            }
        }
    </style>
</head>
<body>
    <div class="resume-container">
        <!-- 头部信息 -->
        <div class="header">
            <h1>殷统占</h1>
            <div class="basic-info">
                出生年月：2005年12月23日 | 出生地：山东省济宁市泗水县
            </div>
        </div>

        <!-- 教育经历 -->
        <div class="section">
            <h2>教育背景</h2>
            <div class="content">
                <ul class="education-list">
                    <li><span>小学：</span>曲阜实验小学（2011年入学，完成六年制小学教育）</li>
                    <li><span>初中：</span>田家炳中学（完成三年制初中阶段学习）</li>
                    <li><span>高中：</span>曲阜市第一中学（就读期间担任小组组长，具备基础的组织协调能力）</li>
                    <li><span>大学：</span>山东建筑大学 | 工业设计专业（在读，系统学习工业设计相关理论与实践技能）</li>
                </ul>
            </div>
        </div>

        <!-- 个人特质 -->
        <div class="section">
            <h2>个人特质</h2>
            <div class="content personal-trait">
                <div class="trait-item">
                    <p>兴趣爱好：热衷于三角洲系列游戏，享受策略与操作结合的体验；乐于探索和尝试各类新奇美食，保持对生活的好奇心。</p>
                </div>
                <div class="trait-item">
                    <p>性格特点：性格温和友善，具备良好的人际交往能力，易与他人建立和谐的相处关系；做事专注执着，偶尔会因追求细节而略显较真，具备较强的钻研精神。</p>
                </div>
            </div>
        </div>

        <!-- 联系方式 -->
        <div class="section">
            <h2>联系方式</h2>
            <div class="content">
                <ul class="contact-list">
                    <li>手机号码：19508605826</li>
                    <li>QQ号码：<a href="tencent://AddContact/?fromId=45&fromSubId=1&subcmd=all&uin=2441201745" target="_blank">2441201745</a>（点击可直接添加）</li>
                </ul>
            </div>
        </div>
    </div>
</body>
</html>
