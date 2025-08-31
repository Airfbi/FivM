<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Air 控制台 - GitHub 项目介绍</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            line-height: 1.6;
            color: #24292f;
            background: #ffffff;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .header {
            background: linear-gradient(135deg, #0d1117 0%, #21262d 100%);
            color: white;
            padding: 60px 0;
            text-align: center;
        }
        
        .header h1 {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #58a6ff, #79c0ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .header p {
            font-size: 1.3rem;
            color: #8b949e;
            margin-bottom: 30px;
        }
        
        .badges {
            display: flex;
            justify-content: center;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        .badge {
            background: #238636;
            color: white;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 500;
        }
        
        .badge.version { background: #0969da; }
        .badge.license { background: #6f42c1; }
        .badge.downloads { background: #d1242f; }
        
        .main-content {
            padding: 60px 0;
        }
        
        .section {
            margin-bottom: 60px;
        }
        
        .section h2 {
            font-size: 2.2rem;
            font-weight: 600;
            margin-bottom: 20px;
            color: #0d1117;
            border-bottom: 3px solid #fd7e14;
            padding-bottom: 10px;
        }
        
        .section h3 {
            font-size: 1.5rem;
            font-weight: 600;
            margin: 30px 0 15px 0;
            color: #0969da;
        }
        
        .section p {
            font-size: 1.1rem;
            margin-bottom: 15px;
            color: #656d76;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 30px 0;
        }
        
        .feature-card {
            background: #f6f8fa;
            border: 1px solid #d0d7de;
            border-radius: 12px;
            padding: 30px;
            transition: all 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            border-color: #0969da;
        }
        
        .feature-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }
        
        .feature-card h4 {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 10px;
            color: #0d1117;
        }
        
        .code-block {
            background: #0d1117;
            color: #f0f6fc;
            padding: 20px;
            border-radius: 8px;
            font-family: 'Monaco', 'Menlo', monospace;
            font-size: 0.9rem;
            overflow-x: auto;
            margin: 20px 0;
            border-left: 4px solid #58a6ff;
        }
        
        .code-block .comment {
            color: #8b949e;
        }
        
        .code-block .keyword {
            color: #ff7b72;
        }
        
        .code-block .string {
            color: #a5d6ff;
        }
        
        .installation-steps {
            background: #f6f8fa;
            border-radius: 12px;
            padding: 30px;
            margin: 20px 0;
        }
        
        .step {
            display: flex;
            align-items: flex-start;
            margin-bottom: 20px;
        }
        
        .step-number {
            background: #0969da;
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 600;
            margin-right: 15px;
            flex-shrink: 0;
        }
        
        .step-content h4 {
            font-weight: 600;
            margin-bottom: 5px;
            color: #0d1117;
        }
        
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin: 20px 0;
        }
        
        .tech-item {
            background: #0969da;
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
            font-weight: 500;
            font-size: 0.9rem;
        }
        
        .screenshot {
            width: 100%;
            max-width: 800px;
            height: 400px;
            background: linear-gradient(135deg, #f6f8fa 0%, #e1e7ed 100%);
            border: 2px solid #d0d7de;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 30px auto;
            color: #656d76;
            font-size: 1.2rem;
        }
        
        .contributors {
            display: flex;
            gap: 15px;
            margin: 20px 0;
        }
        
        .contributor {
            width: 60px;
            height: 60px;
            background: linear-gradient(45deg, #58a6ff, #79c0ff);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 600;
            font-size: 1.2rem;
        }
        
        .footer {
            background: #f6f8fa;
            border-top: 1px solid #d0d7de;
            padding: 40px 0;
            text-align: center;
            color: #656d76;
        }
        
        .footer a {
            color: #0969da;
            text-decoration: none;
        }
        
        .footer a:hover {
            text-decoration: underline;
        }
        
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5rem;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
            
            .badges {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <div class="container">
            <h1>🚀 Air 控制台</h1>
            <p>现代化的 FiveM ESX 服务器管理面板</p>
            <div class="badges">
                <span class="badge version">v2.1.0</span>
                <span class="badge">⭐ 1.2k Stars</span>
                <span class="badge license">MIT License</span>
                <span class="badge downloads">📥 5k+ Downloads</span>
            </div>
        </div>
    </div>

    <div class="main-content">
        <div class="container">
            <!-- 项目简介 -->
            <div class="section">
                <h2>📋 项目简介</h2>
                <p>Air 控制台是一个专为 FiveM ESX 服务器设计的现代化管理面板。它提供了直观的用户界面和强大的管理功能，让服务器管理员能够轻松监控和管理他们的游戏服务器。</p>
                
                <div class="screenshot">
                    🖼️ 项目截图预览区域
                </div>
            </div>

            <!-- 核心功能 -->
            <div class="section">
                <h2>✨ 核心功能</h2>
                <div class="features-grid">
                    <div class="feature-card">
                        <div class="feature-icon">👥</div>
                        <h4>玩家管理</h4>
                        <p>实时查看在线玩家，支持踢出、封禁、发送消息等操作</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">🖥️</div>
                        <h4>服务器监控</h4>
                        <p>监控服务器状态、CPU使用率、内存占用等关键指标</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">🔧</div>
                        <h4>插件管理</h4>
                        <p>管理服务器插件，支持启用、禁用和配置插件</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">📊</div>
                        <h4>数据统计</h4>
                        <p>详细的服务器数据统计和可视化图表</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">🔒</div>
                        <h4>权限控制</h4>
                        <p>多级权限管理，确保服务器安全</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">📱</div>
                        <h4>响应式设计</h4>
                        <p>完美适配桌面和移动设备</p>
                    </div>
                </div>
            </div>

            <!-- 技术栈 -->
            <div class="section">
                <h2>🛠️ 技术栈</h2>
                <div class="tech-stack">
                    <span class="tech-item">HTML5</span>
                    <span class="tech-item">CSS3</span>
                    <span class="tech-item">JavaScript ES6+</span>
                    <span class="tech-item">Node.js</span>
                    <span class="tech-item">Express.js</span>
                    <span class="tech-item">MySQL</span>
                    <span class="tech-item">Socket.io</span>
                </div>
            </div>

            <!-- 安装指南 -->
            <div class="section">
                <h2>📦 安装指南</h2>
                <div class="installation-steps">
                    <div class="step">
                        <div class="step-number">1</div>
                        <div class="step-content">
                            <h4>克隆项目</h4>
                            <p>从 GitHub 克隆项目到本地</p>
                        </div>
                    </div>
                    <div class="step">
                        <div class="step-number">2</div>
                        <div class="step-content">
                            <h4>安装依赖</h4>
                            <p>使用 npm 或 yarn 安装项目依赖</p>
                        </div>
                    </div>
                    <div class="step">
                        <div class="step-number">3</div>
                        <div class="step-content">
                            <h4>配置数据库</h4>
                            <p>配置 MySQL 数据库连接信息</p>
                        </div>
                    </div>
                    <div class="step">
                        <div class="step-number">4</div>
                        <div class="step-content">
                            <h4>启动服务</h4>
                            <p>运行项目并访问管理面板</p>
                        </div>
                    </div>
                </div>

                <div class="code-block">
<span class="comment"># 克隆项目</span>
<span class="keyword">git</span> clone https://github.com/username/air-console.git

<span class="comment"># 进入项目目录</span>
<span class="keyword">cd</span> air-console

<span class="comment"># 安装依赖</span>
<span class="keyword">npm</span> install

<span class="comment"># 配置环境变量</span>
<span class="keyword">cp</span> .env.example .env

<span class="comment"># 启动项目</span>
<span class="keyword">npm</span> start
                </div>
            </div>

            <!-- 配置说明 -->
            <div class="section">
                <h2>⚙️ 配置说明</h2>
                <h3>环境变量配置</h3>
                <div class="code-block">
<span class="comment"># 数据库配置</span>
<span class="string">DB_HOST</span>=localhost
<span class="string">DB_PORT</span>=3306
<span class="string">DB_USER</span>=root
<span class="string">DB_PASS</span>=password
<span class="string">DB_NAME</span>=esx_database

<span class="comment"># 服务器配置</span>
<span class="string">PORT</span>=3000
<span class="string">SECRET_KEY</span>=your_secret_key

<span class="comment"># FiveM 服务器配置</span>
<span class="string">FIVEM_SERVER_IP</span>=127.0.0.1
<span class="string">FIVEM_SERVER_PORT</span>=30120
                </div>

                <h3>权限配置</h3>
                <p>系统支持多级权限管理，包括：</p>
                <ul style="margin-left: 20px; color: #656d76;">
                    <li><strong>超级管理员</strong> - 拥有所有权限</li>
                    <li><strong>管理员</strong> - 玩家管理、服务器监控</li>
                    <li><strong>版主</strong> - 基础玩家管理权限</li>
                </ul>
            </div>

            <!-- API 文档 -->
            <div class="section">
                <h2>📚 API 文档</h2>
                <h3>玩家管理 API</h3>
                <div class="code-block">
<span class="comment">// 获取在线玩家列表</span>
<span class="keyword">GET</span> <span class="string">/api/players</span>

<span class="comment">// 踢出玩家</span>
<span class="keyword">POST</span> <span class="string">/api/players/:id/kick</span>
{
  <span class="string">"reason"</span>: <span class="string">"违反服务器规则"</span>
}

<span class="comment">// 封禁玩家</span>
<span class="keyword">POST</span> <span class="string">/api/players/:id/ban</span>
{
  <span class="string">"reason"</span>: <span class="string">"作弊行为"</span>,
  <span class="string">"duration"</span>: <span class="string">"7d"</span>
}
                </div>
            </div>

            <!-- 贡献指南 -->
            <div class="section">
                <h2>🤝 贡献指南</h2>
                <p>我们欢迎所有形式的贡献！如果你想为项目做出贡献，请遵循以下步骤：</p>
                
                <div class="installation-steps">
                    <div class="step">
                        <div class="step-number">1</div>
                        <div class="step-content">
                            <h4>Fork 项目</h4>
                            <p>在 GitHub 上 fork 这个项目</p>
                        </div>
                    </div>
                    <div class="step">
                        <div class="step-number">2</div>
                        <div class="step-content">
                            <h4>创建分支</h4>
                            <p>创建一个新的功能分支</p>
                        </div>
                    </div>
                    <div class="step">
                        <div class="step-number">3</div>
                        <div class="step-content">
                            <h4>提交更改</h4>
                            <p>提交你的更改并推送到分支</p>
                        </div>
                    </div>
                    <div class="step">
                        <div class="step-number">4</div>
                        <div class="step-content">
                            <h4>创建 PR</h4>
                            <p>创建 Pull Request 并描述你的更改</p>
                        </div>
                    </div>
                </div>

                <h3>👨‍💻 贡献者</h3>
                <div class="contributors">
                    <div class="contributor">A</div>
                    <div class="contributor">B</div>
                    <div class="contributor">C</div>
                    <div class="contributor">D</div>
                    <div class="contributor">+</div>
                </div>
            </div>

            <!-- 更新日志 -->
            <div class="section">
                <h2>📝 更新日志</h2>
                <h3>v2.1.0 (2024-01-15)</h3>
                <ul style="margin-left: 20px; color: #656d76;">
                    <li>✨ 新增插件管理功能</li>
                    <li>🐛 修复玩家搜索bug</li>
                    <li>💄 优化界面设计</li>
                    <li>⚡ 提升性能表现</li>
                </ul>

                <h3>v2.0.0 (2023-12-20)</h3>
                <ul style="margin-left: 20px; color: #656d76;">
                    <li>🎉 全新的用户界面</li>
                    <li>🔒 增强安全性</li>
                    <li>📊 新增数据统计功能</li>
                    <li>🌐 支持多语言</li>
                </ul>
            </div>

            <!-- 许可证 -->
            <div class="section">
                <h2>📄 许可证</h2>
                <p>本项目基于 MIT 许可证开源。详细信息请查看 <a href="#" style="color: #0969da;">LICENSE</a> 文件。</p>
            </div>

            <!-- 支持 -->
            <div class="section">
                <h2>💬 支持与反馈</h2>
                <p>如果你在使用过程中遇到问题或有任何建议，请通过以下方式联系我们：</p>
                <ul style="margin-left: 20px; color: #656d76;">
                    <li>📧 邮箱：support@airconsole.com</li>
                    <li>💬 Discord：Air Console Community</li>
                    <li>🐛 Issues：<a href="#" style="color: #0969da;">GitHub Issues</a></li>
                    <li>📖 文档：<a href="#" style="color: #0969da;">在线文档</a></li>
                </ul>
            </div>
        </div>
    </div>

    <div class="footer">
        <div class="container">
            <p>© 2024 Air Console. Made with ❤️ by the community.</p>
            <p>
                <a href="#">GitHub</a> • 
                <a href="#">Documentation</a> • 
                <a href="#">Discord</a> • 
                <a href="#">Support</a>
            </p>
        </div>
    </div>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'977eedbf105b04cb',t:'MTc1NjY2ODQ4Mi4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
