# PyTorch实现LeNet（非常基础）

使用此仓库，可以初步了解PyTorch的用法，也可以自己试着去训练模型。适合入门用户使用。

网络结构代码是自己照着教程写的

训练代码是用https://github.com/ChawDoe/LeNet5-MNIST-PyTorch改的

测试代码是自己写的

## 注意

1. 如果您需要下载数据集，请将

   ```python
   train_dataset = MNIST(root='./train', train=True, transform=ToTensor())
   test_dataset = MNIST(root='./test', train=False, transform=ToTensor())
   ```

这两行代码加入参数 download = 'True' ！

2. models文件夹里是50轮的训练参数！根目录下面的model.pkl是test准确率最高的参数文件！
3. 原本的LeNet是32\*32的输入，但是这个数据集是28\*28，所以我在第一层网络上加了padding，这样的网络才地道！

## 训练

运行train.py，默认训练100轮。每轮都测试。每轮保存测试文件

## 测试

运行test.py，加载模型并且测试。

会显示一个batch的预测结果。

## 第三方库需求
PyTorch、torchvision（任意版本）





