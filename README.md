<div align="center">

# Windows Liquid Glass

**Windows 桌面端液态玻璃 Qt 组件**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.7+-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![PySide](https://img.shields.io/badge/PySide-2%20%7C%206-41CD52?logo=qt&logoColor=white)](https://doc.qt.io/qtforpython/)
[![Windows](https://img.shields.io/badge/Windows-10%2F11-0078D6?logo=windows&logoColor=white)](https://www.microsoft.com/windows)

[Bilibili](https://www.bilibili.com/video/BV1eBfiBuEyK/) · [YouTube](https://youtu.be/x7mPpVKJA7Q)

</div>

---

## 该项目不再更新，由于纯在各种限制，开发独立引擎中...

---

## 效果预览

<div align="center">
  <img src="WLG.gif" alt="液态玻璃效果" width="100%"/>
</div>

---

## 环境要求

| 依赖 | 版本 |
|------|------|
| 操作系统 | Windows 10 / 11 |
| Python | 3.7+ |
| Qt 绑定 | PySide2 / PySide6 |
| 数值计算 | NumPy |

---

## 快速开始

**1. 克隆仓库**

```bash
git clone https://github.com/yourname/WindowsLiquidGlass.git
```

**2. 安装依赖**

```bash
# 使用 PySide6（推荐）
pip install PySide6 numpy

# 或使用 PySide2
pip install PySide2 numpy
```

**3. 运行示例**

```python
import sys
sys.path.append('path/WindowsLiquidGlass')
import SettingUI

if __name__ == "__main__":
    try:
        from PySide2.QtWidgets import QApplication
        PYSIDE_VERSION = 2
    except ImportError:
        from PySide6.QtWidgets import QApplication
        PYSIDE_VERSION = 6

    app = QApplication(sys.argv)
    ui = SettingUI.SettingUI(qt_move=False) # 如果拖动不了或卡顿尝试切换 qt_move 参数
    ui.show()

    if PYSIDE_VERSION == 2:
        sys.exit(app.exec_())
    else:
        sys.exit(app.exec())
```

---

## API 文档

| 模块 | 描述 |
|------|------|
| [GPU 设备管理器](src/GPUDeviceManager/README.md) | 管理 GPU 设备与上下文 |
| [SDF 生成器](src/SDFGenerator/README.md) | 有向距离场生成 |
| [特效渲染器](src/GPUEffectRenderer/README.md) | GPU 加速特效渲染 |
| [Qt 组件基类](src/GPUSharderWidget/README.md) | 液态玻璃 Qt 组件基础类 |

---

## 许可证

本项目基于 [MIT License](LICENSE) 开源，欢迎自由使用与贡献。

<div align="center">
  <sub>Made with ❤️ for Windows Desktop</sub>
</div>
