# kaspa# Kaspa KRC20 工具集

## 安装依赖
```bash
bun install
```

## 主要脚本使用方法

### 1. 密钥生成
```bash
# 生成新助记词和私钥
bun run src/keyGeneratorCli.ts generate

# 从私钥获取地址
bun run src/keyGeneratorCli.ts address <privateKey>
```

### 2. KRC20 操作
```bash
# 铸币
bun run mint.ts --privKey <your-priv-key>

# 部署
bun run deploy.ts --privKey <your-priv-key>

# 转账
bun run transfer.ts --privKey <your-priv-key>
```

### 3. 批量转账
```bash
# 远程节点批量转账
bun run batch-transfer.ts --privKey <your-priv-key> --addresses <address-file> --amount <amount>

# 本地节点批量转账
bun run batch-transfer-localnode.ts --privKey <your-priv-key> --addresses <address-file> --amount <amount>
```

### 4. 单笔转账
```bash
bun run src/sendKaspa.ts --privKey <privateKey> --destination <address> --amount <amount>
```

### 免责声明
本项目仅供学习和研究使用，开发者不对使用本项目造成的任何损失负责。使用前请确保遵守当地法律法规。
