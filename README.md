# nsis-gen
nsis install scripts generator. (zhcn: NSIS安装包脚本生成器)

- config.json 配置文件

  ```yaml
    {
      ; 产品名称
      "product_name": "TopDFM",
      ; 产品版本
      "product_version": "6.4",
      ; 发布者，通常为公司名称
      "product_publisher": "TopLinker, Inc.",
      ; 发布者主页
      "product_web_site": "http://www.topibd.com",
      ; 主程序的exe名称
      "exe_name": "top-dfm",
      ; 主程序的exe所在的相对路径，相对于source_dir
      "exe_path": "qt5.6.3-win32-msvc2015\\bin\\",
      ; 快捷方式
      ; 可配置多个
      ; shortcut_name为快捷方式的名称
      ; shortcut_exe_name为快捷方式指向的exe的名称
      "shortcut": [
          {
              "shortcut_name": "TopDFM",
              "shortcut_exe_name": "top-dfm"
          },
          {
              "shortcut_name": "TopCAM",
              "shortcut_exe_name": "pdm-workflow"
          }
      ],
      ; 需要打包的根目录
      "source_dir": "F:/svn/topdfm/dist/topikm",
      ; 包含的文件
      "include_files": [
          "./config/*.cfg",
          "./qt5.6.3-win32-msvc2015/bin/**/*",
          "./qt5.6.3-win32-msvc2015/language/**/*",
          "./qt5.6.3-win32-msvc2015/resource/**/*",
          "./template/*"
      ],
      ; 需要剔除掉的文件
      "exclude_files": [
          "./**/*.lib",
          "./**/*.pdb",
          "./**/*.exp"
      ]
  }
  ```

- license.txt 安装界面中的License页面显示的文字