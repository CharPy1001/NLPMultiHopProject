# NLPMultiHopProject
This is a program of my NLP course project, using the Longformer model to generate Multi-Hop questions from certain paragraphs of text

#### 目录

- [自然语言处理课程项目](#自然语言处理课程项目)
  - [目录](#目录)
    - [上手指南](#上手指南)
          - [安装步骤](#安装步骤)
    - [文件目录说明](#文件目录说明)
    - [开发的架构](#开发的架构)
    - [使用到的资源](#使用到的资源)
    - [贡献者](#贡献者)
    - [版本控制](#版本控制)
    - [作者](#作者)
    - [版权说明](#版权说明)
    - [鸣谢](#鸣谢)

#### 上手指南

本项目在Kaggle平台上运行，请先[注册](https://www.kaggle.com/signup)一个Kaggle账号，并使用手机号绑定以便可以使用GPU。


#### 安装步骤

1. 下载ipynb文件并将其上传到Kaggle平台
2. 开启Internet选项
3. 使用时间为"2024-04-19"的运行环境
4. 运行代码


#### 文件目录说明

- Input
  - led-checkpoint1：存放权重文件
  - scnu-ai-challenge-5：存放本项目所需的数据集文件
  - scnu-ai-challenge-dataset-with-sorted-facts：存放分类好的数据集文件
  - transformers：存放模型文件
- Working
  - output.json：预测结果 

```
kaggle 
├── /input/
│  ├── /led-checkpoint1/
│  │  ├── checkpoint-best.pkl
│  ├── /scnu-ai-challenge-5/
│  │  ├── dev.json
│  │  ├── test.json
│  │  └── train.json
│  ├── /scnu-ai-challenge-dataset-with-sorted-facts/
│  │  ├── dev.json
│  │  └── test.json
│  ├── /transformers/
│  │  ├── /albert-large-v2/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /bert-base-uncased/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /bert-large-uncased/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /distilroberta-base-uncased/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /distilroberta-base/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /facebook-bart-base/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /facebook-bart-large/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /funnel-transformer-large/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /funnel-transformer-small/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /google-electra-base-discriminator/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /roberta-base/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /roberta-large/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /t5-base/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /t5-large/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /xlnet-base-cased/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
│  │  ├── /xlnet-large-cased/
│  │  │  ├── config.json
│  │  │  ├── python_model.bin
│  │  │  └── tokenizer_config.json
├── /working/
│  ├── output.json

```

#### 开发的架构

Longformer-Encoder-Decoder (LED)模型：一种用于处理长文本序列的transformer架构。其主要特点包括:
- 编码器:
  - 使用Longformer的稀疏注意力机制
  - 局部窗口注意力
  - 全局注意力

- 解码器:
  - 标准的transformer解码器结构
  - 使用交叉注意力连接编码器和解码器

- 位置编码:
  - 使用相对位置编码

- 预训练:
  - 使用掩码语言模型和文档旋转任务进行预训练

#### 使用到的资源

- [Longformer-Encoder-Decoder](https://huggingface.co/docs/transformers/v4.40.2/en/model_doc/led#led)
- [Kaggle](https://www.kaggle.com/)
- [HotpotQA](https://hotpotqa.github.io/)

#### 贡献者

- 彭鸿博：
- 林浩然：


#### 版本控制

该项目使用Kaggle内置的版本控制工具进行版本管理。

#### 作者

彭鸿博
Email:20214001001@m.scun.edu  &ensp; QQ:3130820157

林浩然
Email:3221312632@qq.com  &ensp; QQ:3221312632

#### 版权说明

该项目签署了MIT 授权许可，详情请参阅 [LICENSE.txt](https://github.com/shaojintian/Best_README_template/blob/master/LICENSE.txt)

#### 鸣谢

- [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
- [Img Shields](https://shields.io)
- [Choose an Open Source License](https://choosealicense.com)
- [GitHub Pages](https://pages.github.com)
- [Animate.css](https://daneden.github.io/animate.css)
- [xxxxxxxxxxxxxx](https://connoratherton.com/loaders)
