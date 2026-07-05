# OPA Characterization

基于 MATLAB 的光学相控阵（Optical Phased Array, OPA）表征工具集，用于光学系统测量与光束质量评估。

A MATLAB toolkit for optical phased array characterization, optical-system measurement, and beam-quality evaluation.

## 功能 | Features

| 模块 | 功能 |
| --- | --- |
| `powerTest` | 采集输入/输出功率，计算链路损耗与损伤阈值 |
| `caliAngle` | 根据相机像元尺寸、分辨率与焦距计算光束角度偏差 |
| `caliMerit` | 计算积分峰值比（IPR）与峰值旁瓣比（PSLR） |
| `spotMerit` | 计算光斑发散角与基于能量分布的质量指标 |

## 环境要求 | Requirements

- MATLAB R2020b 或更高版本
- Image Processing Toolbox（`spotMerit` 使用）

## 目录结构 | Project Structure

```text
opa-characterization/
├── main.m          # 运行入口与测试参数
├── Module/         # 测试与评估模块
├── Tools/          # 数据导入和图像处理工具
└── Result/         # 生成的图像与测试结果
```

## 使用方法 | Usage

```bash
git clone https://github.com/Wonham/opa-characterization.git
cd opa-characterization
```

1. 在 MATLAB 中打开项目目录。
2. 将相机导出的测试数据命名为 `I0.txt`，放在项目根目录。
3. 在 `main.m` 中调整相机参数、阈值，并注释不需要运行的模块。
4. 运行 `main.m`。图像与文本结果会写入 `Result/`。

```matlab
run('main.m')
```

原始输入数据和生成结果默认不纳入版本控制。

## License

This project is licensed under the [MIT License](./LICENSE).
