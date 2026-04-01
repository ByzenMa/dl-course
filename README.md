# 深度学习与自然语言处理课程项目合集

## 1. 简介与目的

本仓库汇总了多个深度学习（Deep Learning）与自然语言处理（NLP）课程项目，主要包含：

- **CS224n NLP 作业实践**（词向量、情感分析、依存句法等）
- **Udacity ND101 深度学习项目**（图像分类、文本生成、翻译、GAN、人脸生成等）
- **若干专题教程**（Autoencoder、DCGAN、BatchNorm 等）

### 项目目标

1. 系统实践深度学习与 NLP 的核心方法与训练流程。  
2. 提供可复现的课程代码与实验结构，便于学习、复盘与二次开发。  
3. 形成按模块组织的项目导航，降低上手成本。

---

## 2. 项目主体（按模块说明）

### 2.1 顶层目录结构

```text
.
├── cs224n_nlp/
├── nd101_dl/
└── README.md
```

### 2.2 `cs224n_nlp` 模块（NLP 方向）

该模块主要是 Stanford CS224n 课程作业实现。

#### 子模块 A：`assignment1`

- 主要内容：
  - Softmax、Sigmoid、梯度检查
  - Word2Vec（Skip-gram / 相关训练逻辑）
  - 情感分类（含 Stanford Sentiment Treebank 数据）
- 关键文件示例：
  - `q1_softmax.py`
  - `q2_sigmoid.py` / `q2_gradcheck.py`
  - `q3_word2vec.py`
  - `q4_sentiment.py`

#### 子模块 B：`assignment2`

- 主要内容：
  - 分类器与模型初始化
  - 句法解析相关实现（parser transitions / parser model）
- 关键文件示例：
  - `q1_classifier.py`
  - `q2_initialization.py`
  - `q2_parser_transitions.py`
  - `q2_parser_model.py`

---

### 2.3 `nd101_dl` 模块（深度学习工程方向）

该模块主要是 Udacity ND101 项目与练习。

#### 子模块 A：`first-neural-network`

- 任务：构建并训练第一个前馈神经网络（Bike Sharing 数据集）。
- 常用入口：`Your_first_neural_network.ipynb`

#### 子模块 B：`image-classification`

- 任务：图像分类项目（含 Notebook 与测试文件）。
- 常用入口：`dlnd_image_classification.ipynb`

#### 子模块 C：`tv-script-generation`

- 任务：基于 RNN 进行电视剧对白文本生成。
- 常用入口：`dlnd_tv_script_generation.ipynb`

#### 子模块 D：`language-translation`

- 任务：序列到序列翻译实践。
- 常用入口：`dlnd_language_translation.ipynb`

#### 子模块 E：`face_generation`

- 任务：GAN 人脸生成项目。
- 常用入口：`dlnd_face_generation.ipynb`

#### 子模块 F：`tutorials`

- 专题教程：
  - Autoencoder
  - DCGAN-SVHN
  - Batch Normalization

---

## 3. 运行方式（分步骤）

> 建议使用 Python 3.8+，并在虚拟环境中运行。

### 3.1 环境准备

1. 克隆仓库并进入项目目录：

   ```bash
   git clone <your-repo-url>
   cd dl-course
   ```

2. 创建并激活虚拟环境：

   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```

3. 安装常用依赖（按模块补充）：

   ```bash
   pip install -U pip
   pip install numpy scipy matplotlib jupyter notebook
   ```

---

### 3.2 运行 `cs224n_nlp` 模块

1. 进入某个作业目录，例如：

   ```bash
   cd cs224n_nlp/assignment1
   ```

2. 安装该作业依赖（若存在 `requirements.txt`）：

   ```bash
   pip install -r requirements.txt
   ```

3. 运行脚本或验证文件，例如：

   ```bash
   python q1_softmax.py
   python q2_gradcheck.py
   ```

---

### 3.3 运行 `nd101_dl` Notebook 项目

1. 进入对应模块目录，例如图像分类：

   ```bash
   cd nd101_dl/image-classification
   ```

2. 启动 Jupyter：

   ```bash
   jupyter notebook
   ```

3. 在浏览器中打开对应 `.ipynb` 文件并按顺序执行单元格：
   - `dlnd_image_classification.ipynb`
   - 或其他模块的 Notebook

---

### 3.4 运行常见测试脚本（按模块）

在对应目录下可尝试执行：

```bash
python problem_unittests.py
```

若某些模块有单独测试文件（如 `test.py` 或 `my_test.py`），可直接运行：

```bash
python test.py
python my_test.py
```

---

## 4. 学习建议

1. **先跑通 Notebook，再读脚本实现**：先理解训练流程，再关注细节函数。  
2. **按模块逐步推进**：建议从 `first-neural-network` 和 `assignment1` 开始。  
3. **记录实验配置**：建议保存随机种子、超参数与结果，便于复现。

---

## 5. 说明

- 本仓库以课程实践为主，部分目录包含中间产物（如 `.pyc`、`.p`、图片或缓存文件）。
- 若你计划二次开发，建议为每个子项目单独维护依赖与运行日志。
