> Bluelm-Shopguard购物反诈智能助手是由SIGAI39团队基于vivo蓝心大模型和其矩阵api开发的专业购物反诈服务。前端优雅精美，拥有快应用、Webapp(前两者可直接云端访问)和本地部署三种部署方式，采用拟人化交互设计。后端集成多模态处理、RAG检索增强、智能查询改写等核心技术，提供多维度欺诈分析，涵盖价格合理性、平台可信度、商品真实性和支付安全等关键风险点。通过智能联网验证和专业知识库检索，系统能够精准识别各类购物诈骗行为，并通过0-10星级评分直观展示风险等级。该产品不仅帮助消费者快速识别虚假宣传、降低受骗风险，同时为电商平台提供违规内容审核支持，助力监管部门构建安全、透明的数字消费生态。

## files

策划文档
PPT
视频
快应用rpk

## links

> 项目网站
> [https://bluelm-shopguard.github.io/bluelm-shopguard/](https://bluelm-shopguard.github.io/bluelm-shopguard/)
>
> 团队主页
> [https://github.com/bluelm-shopguard](https://github.com/bluelm-shopguard)

> 后端仓库
> [https://github.com/bluelm-shopguard/shopguard-backend](https://github.com/bluelm-shopguard/shopguard-backend)
>
> 后端在线文档
> [https://shopguard-backend.readthedocs.io/en/latest/](https://shopguard-backend.readthedocs.io/en/latest/)

> 前端仓库
> [https://github.com/bluelm-shopguard/shopguard-chatbot](https://github.com/bluelm-shopguard/shopguard-chatbot)
>
> 前端在线文档
> [https://shopguard-chatbot.readthedocs.io/en/latest/](https://shopguard-chatbot.readthedocs.io/en/latest/)

## quick-start

### quickapp

在兼容快应用的设备上安装rpk，即可直接运行bluelm shopguard前端

### webapp

前端可以部署为webapp

```bash
git clone https://github.com/bluelm-shopguard/shopguard-chatbot
cd shopguard-chatbot
npm install
npm run serve
```

注意如果（CORS）报错，尝试运行代理服务器

```bash
node server.js
# open at http://localhost:8080/src/homepage.html
```

### backend

在阿里云上部署了docker服务，快应用利用自带的凭据访问服务器

#### 本地部署后端

```bash
https://github.com/bluelm-shopguard/shopguard-backend
cd shopguard-backend

cp .env.example
# fill VIVO_APP_ID and VIVO_APP_KEY in .env

conda create backend python-3.10 pip 
# or use other tools like venv
conda activate backend
pip install requirements.txt
python newserver.py
```

