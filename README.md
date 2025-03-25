# 🚀 wasm-utils | 面向未来的高性能Web工具库

用Rust+WebAssembly重铸核心工具链，为现代Web开发注入原生级性能。通过编译为.wasm字节码，突破JavaScript的性能瓶颈，在加密计算、数据转换、数学运算等场景实现5-10倍性能跃升。

## 核心优势：
- ​原生级执行效率 - 基于Rust零成本抽象特性，关键路径代码媲美C++性能
- ​无GC内存安全 - 所有权系统保障内存安全，规避传统JS应用的泄漏风险
- ​跨平台即插即用 - 产出标准WebAssembly模块，支持浏览器/Node.js无缝对接
- ​轻量级封装 - 每个函数独立编译，Tree-shaking后平均体积小于20KB
- ​全类型支持 - 完备的TypeScript类型定义，智能提示开箱即用

## 为什么选择wasm-utils？
​- 双向互操作性：支持JS→Wasm内存共享，零拷贝数据交换
- ​渐进式采用：可按函数粒度替换性能瓶颈模块
- ​构建即优化：通过LLVM编译链实现自动SIMD优化
- ​安全沙箱：Wasm内存隔离机制防范供应链攻击

## 即刻体验性能飞跃
1 作为依赖安装到项目
  ```bash
npm install wasm-utils --save
  ```
2 使用示例
```typescript
import init, { Throttler, Debouncer } from 'wasm-utils';

const throttler = new Throttler(3000, true, true);
throttler.throttle(() => console.log("1st call:", Date.now()));
throttler.throttle(() => console.log("2nd call:", Date.now()));

const debouncer = new Debouncer(3000);
const args = new Array();
debouncer.run(() => {
  console.log('debouncer.run(args)');
}, args);
```
[查看完整文档] | [快速开始指南]
