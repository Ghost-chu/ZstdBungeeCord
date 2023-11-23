# ZstdBungeeCord

【不推荐使用，不值】Fabric Mod，将 MC 的网络包压缩算法更换为 Zstd 算法，需要配合 ZstdBungeeCord 使用。

## 不推荐使用

⚠本仓库仅用于代码存档。  
由于压缩率不佳，实际环境中不会产生很好的效果。

测试结果：
```plain
============================================
测试结果：
原始总大小：917.3 MiB
zlib：147.2 MiB
zstd(标准)：144.7 MiB
zstd(字典)：141.1 MiB
============================================
```

## 特性

* 添加对 Zstd 压缩算法的支持，需要配合 FabricZstdProtocol
* 仅在 FabricZstdProtocol 客户端上启用 Zstd 压缩算法，在接受正常客户端时时，仍然使用 zlib 默认压缩算法。
* 支持服务端下发压缩配置（压缩率，Zstd字典）
* 支持自定义 zlib 和 Zstd 的压缩率
* 支持配置和提供 Zstd 字典