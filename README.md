# Android ConstraintLayout 约束布局演示

## 简介

本 Demo 演示 Android ConstraintLayout 的各种约束方式，包括相对约束、尺寸约束、链式约束等。

## 基本原理

### 什么是 ConstraintLayout？

ConstraintLayout 是 Android 中最强大的布局管理器，通过约束来定位子 View，可以实现复杂的 UI 布局而无需嵌套多层布局。

### 核心概念

1. **相对约束**: 使用 app:layout_constraintXXX_toYYYOf 属性
2. **尺寸约束**: 设置 width=0dp 配合 match_constraint
3. **链式约束**: 多个 View 互相约束形成链
4. **引导线**: Guideline 用于辅助定位

## 启动和使用

### 环境要求
- Android Studio

### 安装运行
使用 Android Studio 打开项目并运行

## 教程

### 1. 相对约束

```xml
<TextView
    app:layout_constraintTop_toBottomOf="@id/title"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintEnd_toEndOf="parent" />
```

### 2. 居中约束

```xml
<Button
    app:layout_constraintTop_toTopOf="parent"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintEnd_toEndOf="parent" />
```

### 3. 宽度约束

```xml
<TextView
    android:layout_width="0dp"
    app:layout_constraintWidth_default="percent"
    app:layout_constraintWidth_percent="0.8" />
```

### 4. 链式约束

```xml
<Button
    app:layout_constraintHorizontal_chainStyle="spread" />
```

## 注意事项

1. 使用 0dp 配合约束实现响应式布局
2. 避免使用 match_parent，使用 0dp + constraints
3. ConstraintLayout 可以显著减少布局层级
