## 内核 out-of-tree modules 支持rust智能提示
### 修改工程文件
```
修改 cicv-r4l-cnwzhu/linux/rust/Makefile
修改 cicv-r4l-cnwzhu/linux/Makefile
修改 cicv-r4l-cnwzhu/linux/scripts/generate_rust_analyzer.py

内核中的rust模块执行 make LLVM=1 O=build rust-analyzer
外部的rust模块执行 make LLVM=1 -C ../linux/build M=$PWD rust-analyzer

修改 vscode配置文件
.vscode/settings.json
    "rust-analyzer.linkedProjects": [
        "${workspaceFolder}/src_e1000/rust-project.json",
        "${workspaceFolder}/linux/build/rust-project.json"
    ]


```
