# Tmux 配置

简洁高效的 tmux 配置，采用 minimal-tmux-status 主题，支持 vim 风格按键。

## 功能特性

- **Vim 模式**：复制模式使用 vi 按键
- **智能编号**：窗口和面板从 1 开始编号
- **极简主题**：显示 prefix 按键状态的极简状态栏
- **HJKL 分屏**：直观的 hjkl 分屏操作
- **Alt 切换**：无需 prefix 键即可切换面板

## 快捷键

### Prefix 键
- `Ctrl+b` - 前缀键

### 分屏操作
- `Ctrl+b h` - 垂直分屏（左右）
- `Ctrl+b l` - 垂直分屏（左右）
- `Ctrl+b j` - 水平分屏（上下）
- `Ctrl+b k` - 水平分屏（上下）

### 面板切换（无需 prefix）
- `Alt+h` - 切换到左边的面板
- `Alt+j` - 切换到下边的面板
- `Alt+k` - 切换到上边的面板
- `Alt+l` - 切换到右边的面板

### 调整面板大小（无需 prefix）
- `Shift+Alt+h` - 向左扩大 5 格
- `Shift+Alt+j` - 向下扩大 5 格
- `Shift+Alt+k` - 向上扩大 5 格
- `Shift+Alt+l` - 向右扩大 5 格

### 窗口切换
- `Alt+1~9` - 切换到指定窗口（无需 prefix）
- `Ctrl+b 1~9` - 切换到指定窗口

### 其他操作
- `Ctrl+b r` - 重载配置文件
- `Ctrl+b I` - 安装/更新插件

## 主题

使用 [niksingh710/minimal-tmux-status](https://github.com/niksingh710/minimal-tmux-status) 极简主题。

### 主题配置
- 蓝色主题 (#698DDA)
- 圆润箭头样式
- 显示 prefix 按键状态
- 显示全屏图标

## 安装

### 一键安装

```bash
# 备份现有配置（如果存在）
[ -d ~/.config/tmux ] && mv ~/.config/tmux ~/.config/tmux.backup
[ -f ~/.tmux.conf ] && mv ~/.tmux.conf ~/.tmux.conf.backup

# 克隆仓库
git clone https://github.com/jeffrey-dot/.tmux.git ~/.config/tmux

# 创建符号链接
ln -sf ~/.config/tmux/.tmux.conf ~/.tmux.conf
```

### 手动安装

1. 创建符号链接：
```bash
ln -s ~/.config/tmux/.tmux.conf ~/.tmux.conf
```

2. 重载配置（在 tmux 中）：
```
Ctrl+b r
```

3. 安装插件（自动）：
首次启动 tmux 时会自动安装 TPM 和插件，或手动执行：
```
Ctrl+b I
```

## 配置文件位置

- 配置文件：`~/.config/tmux/.tmux.conf`
- 符号链接：`~/.tmux.conf`

## 依赖

- [TPM](https://github.com/tmux-plugins/tpm) - Tmux Plugin Manager
- [minimal-tmux-status](https://github.com/niksingh710/minimal-tmux-status) - 极简主题
