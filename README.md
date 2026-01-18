# D007 django+neo4j三维知识图谱医疗问答系统|3D+2D双知识图谱可视化+问答+寻医问药系统
> 文章结尾部分有CSDN官方提供的学长 联系方式名片
> 

完整项目收费，可联系QQ: 81040295 微信: mmdsj186011 注明从git来的，谢谢！
也可以关注我的B站： 麦麦大数据 https://space.bilibili.com/1583208775

编号:  D007

## 视频

[video(video-gi5ICBSK-1757645421985)(type-bilibili)(url-https://player.bilibili.com/player.html?aid=864829060)(image-https://i-blog.csdnimg.cn/img_convert/1eb2042040112100092ff366d24e90e7.jpeg)(title-Vue+Django 医疗疾病知识图谱问答neo4j KGQA系统)]

## 1 系统简介
系统简介：本系统是一个基于Vue.js前端框架和Django后端框架构建的智能医疗问答平台，旨在为用户提供疾病知识图谱的可视化展示与问答服务。系统采用neo4j图数据库存储并管理医疗疾病知识，构建了包含疾病、药物及其关联关系的知识图谱。系统集成了自然语言处理技术，支持通过关键词检索和问答交互，快速获取疾病相关信息。同时，系统提供2D和3D两种可视化方式，便于用户直观理解疾病知识表现。整体界面设计采用午夜蓝与赛博紫的配色方案，具有独特的视觉吸引力。系统还支持用户的基础功能，如注册登录、密码修改及个人信息管理，为用户提供了便捷的交互体验。。
## 2 功能设计
统主要包含知识图谱构建与可视化、智能问答、用户权限管理等核心功能。首先，在知识图谱构建模块中，系统能够将医疗疾病数据导入neo4j数据库，构建疾病与药物的关联关系，并存储包括病因、治愈率、预防方法、常用药物等详细的疾病知识。其次，智能问答模块通过LTP技术进行实体识别，结合图数据库中的知识进行检索，能够根据用户提供的症状或疾病名称，快速返回相关治疗药物、治愈率、治疗方法和预防措施等信息。在可视化方面，系统集成了echarts和三维可视化库，实现了疾病知识图谱的2D和3D展示，并支持关键词模糊搜索功能，满足不同用户的查阅需求。此外，系统还完善了用户的基本功能，包括注册、登录、密码修改、头像及个人信息管理等，确保了用户的使用体验和数据安全。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e1b760256c5c48f9b2d120747f66723f.png)
### 2.1系统架构图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ec44385213494d589bc24c78bb6f3184.png)
### 2.2 功能模块图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/543f0e904c0c487da49b2fa1f5a0cfbc.png)
## 3 功能展示
### 3.1 登录 & 注册
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d2f671717d3549f6b2452893bc11cb08.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/43fdb778f4444cd7aba1acab1472eadb.png)
### 3.2 生成知识图谱
医疗疾病知识图谱导入neo4j数据库，有疾病和药物的关系图、疾病包含的知识有病因、治愈率、预防的方法、常用药物等。
整个过程我们都可以看到图谱的生成进度的：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1806f494689b43c7b2b4858de8cb6b16.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2ce5ebaec89b4a7cb7e7491626724616.png)
通过neo4j 界面查看：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e96f236c2cc44a8cba9f35151092c8b5.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c5794ff950c14b029da4d6afa59ea320.png)

### 3.3 2D 知识图谱可视化
图谱的2D展示，支持关键词模糊搜索，通过echarts实现可视化。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/fbc2deb8a1a7414eb35873c2d8c214e4.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/37c7eb375c014cb98543b1f37f84d073.png)

### 3.4 3D 知识图谱可视化
图谱的3D三维展示，支持关键词模糊搜索，通过三维相关可视化库实现可视化。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9c04b17ce4594d76bfea64352f6ebece.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5769e0fde2874b03b27150ca01eda606.png)
### 3.5 问答系统
问答系统实现，后端利用LTP进行实体识别后根据关键词从图谱中检索内容进行展示，根据疾病可以返回治疗的常见药物、治愈率、治疗方法、预防方法等疾病相关知识。
基于Vuetify前端框架和后端的LTP（语言技术平台）命名实体识别结合Neo4j图数据库的关键词检索功能。整体上，这个系统的功能可以概括为以下几点：
智能问答：用户可以在输入框中输入与疾病或治疗相关的问题，系统通过LTP命名实体识别模块分析用户的提问，从中提取出关键信息（例如疾病、症状、药物等）。
根据提取出的关键数据，系统利用Neo4j进行知识图谱的检索，以获取与用户查询相关的信息。
信息展示：系统能够将关于疾病、治疗方法和药物的详细信息以对话的形式返回给用户。信息展示区域采用了卡片式设计，使得文本信息可读性强，用户能够快速获取所需信息。
关键信息反馈：系统能够提取并反馈疾病的病因、治疗建议及治愈率等信息，优化用户的经验，使得用户能更高效地获取健康信息。
“治疗药物应该可以使用”、“治愈率”等反馈能够直观地展示治疗方法的有效性。
用户交互：系统具备实时交互功能，用户的查询和系统的回答都能在单一的对话界面中进行展现，增强了用户体验。
可扩展性：由于采用了知识图谱和命名实体识别，系统具有较强的扩展性，可以轻松地加入更多的医学知识与数据源，提高回答的全面性和准确性。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/840e5d64847c41f0b06665c4b709e5dd.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b0c7758c9f124bf08058a13daa46c3dc.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/dad3d25190924de0b0a358fb4130979a.png)
### 3.6 修改个人信息 & 修改密码
修改密码、修改个人头像、个人信息。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/902da4581f35480d84d4f0ed103d28ea.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2efb3915bce3478daa9d50893702a1ca.png)
## 4程序代码
### 4.1 代码说明
代码介绍：该医疗知识问答系统基于LTP进行医疗相关问答。系统通过接收用户输入的问题或描述，利用LTP进行句法分析、实体识别和语义理解。系统首先对输入的文本进行分词和词性标注，识别出关键的医疗实体（如疾病、症状、药物等）。随后，系统通过分析句子的语义角色，理解用户的意图和所需的信息类型。系统将提取的实体与预先构建的医疗知识库进行匹配，筛选出相关的知识条目，并生成自然语言形式的回答。知识库包含疾病的定义、症状、治疗方法、用药建议等多方面内容。在匹配过程中，如果系统无法找到相关信息，会提示用户重新输入或提供更详细的描述。
### 4.2 流程图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/dd51995783a8412f862e38573aed936a.png)

### 4.3 代码实例
```python
import requests


# 假设LTP的API地址为http://localhost:8000
LTP_API = "http://localhost:8000/segment"
MEDICAL_KB = {
    "头痛": {
        "描述": "常见的症状，可能由感冒、紧张或偏头痛引起。",
        "治疗": "usual：对症治疗，如服用止痛药；严重时需就医。",
        "建议": "建议多休息，注意饮食。"
    },
    "发烧": {
        "描述": "体温升高，通常由感染引起。",
        "治疗": "usual：降温药物；严重时就医。",
        "建议": "多喝水，注意隔离。"
    }
    # 可以扩展更多的医疗知识
}

@app.route('/ask', methods=['POST'])
def answer_question():
    question = request.json.get('question', '')
    if not question:
        return jsonify({'error': '请提供问题'}), 400

    # 调用LTP进行分词和语义分析
    try:
        response = requests.post(LTP_API, json={'text': question})
        words = response.json()['words']
        print(f"分词结果：{words}")
    except Exception as e:
        return jsonify({'error': 'LTP服务不可用'}), 500

    # 简单的关键词匹配（开发者可以扩展为更复杂的语义分析）
    for entity in words:
        if entity in MEDICAL_KB:
            return jsonify({
                'result': f"关于{entity}的信息：",
                'description': MEDICAL_KB[entity]['描述'],
                'treatment': MEDICAL_KB[entity]['治疗'],
                'suggestion': MEDICAL_KB[entity]['建议']
            })
    
    return jsonify({'message': '没有找到相关信息，请重新描述问题'}), 404

if __name__ == "__main__":
    app.run(debug=True)

```
