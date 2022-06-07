# 安装

## 1.安装Anaconda

安装略.

1.1 更新pip

```bash
pip3 install --upgrade pip
```

1.2 更新conda

```bash
conda update conda
```

## 2.配置虚拟环境

2.1 建立虚拟环境

<img src="..\_static\1.png" alt="1" style="zoom:40%;" />

```bash
conda create -n deeplearning python=3.7
```

2.2 激活虚拟环境

```bash
activate deeplearning
```

2.3 退出虚拟环境

```bash
conda deactivate
```

## 3.配置Jupyter notebook

3.1 激活虚拟环境

```bash
activate deeplearning
```

3.2 加入虚拟环境内核

```bash
conda install nb_conda
conda install ipykernel
conda install -n deeplearning ipykernel
python -m ipykernel install --user --name deeplearning
```

3.3 启动jupyter notebook

```bash
jupyter notebook
```

3.4 添加插件

```bash
pip install jupyter_contrib_nbextensions -i https://pypi.tuna.tsinghua.edu.cn/simple
jupyter contrib nbextension install --user
pip install jupyter_nbextensions_configurator -i 
```

## 4.安装深度学习框架

4.1 安装Pytorch

可以参考[深入浅出PyTorch](https://datawhalechina.github.io/thorough-pytorch/第一章/index.html)

①查看是否有GPU

<img src="..\_static\2.png" alt="1" style="zoom:40%;" />

②查看CUDA版本

<img src="..\_static\3.png" alt="1" style="zoom:40%;" />

③获取Pytorch安装命令

<img src="..\_static\4.png" alt="1" style="zoom:40%;" />

```bash
% 以网页为准！这里只是个例子！
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch
```

④激活虚拟环境进行安装

```bash
activate deeplearning
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch
```

如果下载CPU版本的Pytorch，可以跳过上述步骤，使用如下步骤下载（使用了临时清华源！）

```bash
activate deeplearning
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple torch
```

⑤验证Pytorch是否支持CUDA

```bash
python
import torch
torch.cuda.is_available()
```

4.2 安装Tensorflow

```bash
activate deeplearning
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple tensorflow
```

