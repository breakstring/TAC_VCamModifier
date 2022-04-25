# GeneralTemplate

本模板库创建的工程中LFS文件默认不需要lock即可修改

## 注意事项
- 请注意修改 .gitignore 中的忽略文件定义。例如尤其是 obj([O]obj) 文件，3D类项目可能需要它，而某些项目可能不需要它。
- 请注意修改 .gitattributes 文件，如果你有什么二进制文件，请将其扩展名按照它来加进入，这样这些二进制文件就会使用Git LFS来存储，避免不必要的系统负担。