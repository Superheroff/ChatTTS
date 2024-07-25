# 所需工具
- git
- PyCharm
-  [下载源](https://mirrors.bfsu.edu.cn/pypi/web/simple/)
- 请勿在markdown直接运行命令，须在根目录执行，他的markdown不在根目录，直接运行会报错

# 所需命令
```shell
git clone git@github.com:2noise/ChatTTS.git
```

# 下载模型
- [打开魔塔社区](https://modelscope.cn/models/pzc163/chatTTS)
- git需要退出chattts目录
- ```shell
  git lfs install
  git clone https://www.modelscope.cn/pzc163/chatTTS.git
    ```
- 把`asset`文件夹复制到chattts目录

# 运行方式
- 方式一：运行`webui.py`
- ```shell
    python examples/web/webui.py
    ```
- 方式二：直接命令行生成
- ```shell
    python examples/cmd/run.py "Your text 1." "Your text 2."
    ```
- 方式三：运行`webapi`，通过接口生成
- ```shell
    fastapi dev examples/api/main.py --host 0.0.0.0 --port 8080
    ```

- 首次运行会自动下载`DVAE_full.pt `这个模型
