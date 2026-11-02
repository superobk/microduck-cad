# microduck-cad

分享 Microduck 周边及其他有意思的 3D 打印项目：可直接下载的 STL、可编辑的 3MF 打印准备工程，以及打印和使用说明。

## 项目目录

| 项目 | 版本 / 状态 | 文件与说明 |
| --- | --- | --- |
| Microduck Stand / JIG-190 静态支承与校准工装 | R5.0-rc1，待切片与实物试配 | [使用说明、PDF、STL、3MF](projects/microduck-stand/r5-compact-full15/README.md) |

3MF 的实际状态以各项目 README 为准；文件名中的 `PREPARE` 表示打印准备工程，需自行切片检查。

## 文件摆放准则

```text
projects/
  <project-slug>/                 # 一个独立打印项目，使用稳定的英文小写短横线名称
    README.md                    # 用途、版本入口与兼容关系
    <revision>/                  # 一套相互配套的文件，如 r5-compact-full15
      README.md                  # 下载入口、状态、物料、打印、装配和使用说明
      stl/                       # 单件打印网格，统一按 mm 导出，说明打印数量
      printing/                  # 3MF、必要的参数文件；在说明中标明机型/材料/喷嘴
      docs/                      # PDF 图册、补充尺寸或装配资料
      images/                    # 实物照片或渲染图，明确区分二者
      cad/                       # 可选：可维护的 CAD 参数源、STEP、生成脚本
      validation/                # 可选：检查结果，区分数字检查/切片/实物验证
      NOTICE.md                  # 来源、作者、许可与修改说明
      MANIFEST.json              # 版本及导入文件的来源、大小与 SHA-256
      CHECKSUMS.sha256           # 本版本文件的下载完整性校验
```

1. **一项目一目录，一套兼容件一版本目录。** 后续支架版本放在 `projects/microduck-stand/` 下；无关打印件另建项目，不混入 Stand。旧版本被引用后保留原路径。
2. **README 是使用入口。** 新增项目同时更新本首页目录和项目版本入口；写明用途、尺寸/单位、数量、五金、机型、材料、朝向、支撑、装配步骤、兼容限制、验证状态与来源许可。缺少的实测数据写“未验证”。
3. **STL 与 3MF 配套。** 文件名保留零件编号和版本含义；3MF 名称建议 `<project>_<revision>_<printer>_<material>_PREPARE.3mf`。更换几何后同步更新打印工程、说明与哈希；需要改变配合关系时新建版本，避免混装。
4. **源文件可跟踪。** 用户可在本地 `repo/microduck-cad/projects/<project-slug>/` 持续开发，CAD 放版本目录的 `cad/`。本地 `repo/` 是工作区容器，不再提交一个嵌套的 `repo/` 或 `.git/`。
5. **只提交分享必需内容。** 不提交缓存、虚拟环境、临时切片输出、个人机器路径、凭据或设备配置。G-code 通常不入库；如确需分享，单独注明确切机器、材料、固件与验证状态。大型发布包可使用 GitHub Releases；单文件接近 GitHub 限制前先规划 LFS / Releases。
6. **可追溯而不混淆验收。** 新版记录变更和来源，更新 manifest / 校验清单。渲染图标“CAD 渲染”；数字检查、成功切片、实际打印、装配及承重精度分别记录。
7. **许可按来源保留。** 根目录 [LICENSE](LICENSE) 为 MIT；第三方模型、图片及派生材料的原许可与署名见对应项目 NOTICE，根目录许可不替代这些条款。

校验某版本时，先进入该版本目录，再执行：

```bash
shasum -a 256 -c CHECKSUMS.sha256
```
