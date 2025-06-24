
# 🚀 Nexus CLI Node Setup Guide

---

# 📁 Create Directory & Enter
```bash
mkdir nexus-cli
cd nexus-cli
```
---

# 🦀 Install Rust
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
```
---


# 🎯 Add RISC-V Target
```bash
rustup target add riscv32i-unknown-none-elf
```
---

# 🔧 Install Required Dependencies
```bash
sudo apt update
sudo apt install -y pkg-config libssl-dev
sudo apt install -y protobuf-compiler
```
---


 🌐 Install Nexus CLI
curl https://cli.nexus.xyz/ | sh

🔍 Get your Node ID
 Go to 👉 https://beta.nexus.xyz/
 Then check the "Node" section and click ➕ Add CLI Node
 
---

# 🔁 To Restart Nexus CLI
```bash
curl https://cli.nexus.xyz/ | sh
```

----

# ⚠️ Error 1 Fix: proto — experimental_allow_proto3_optional orchestrator.proto
If you see this error, run the following commands one by one:
```bash
sudo apt-get remove -y protobuf-compiler
wget https://github.com/protocolbuffers/protobuf/releases/download/v30.0-rc1/protoc-30.0-rc-1-linux-x86_64.zip
sudo apt install unzip
sudo unzip protoc-30.0-rc-1-linux-x86_64.zip -d /usr/local/
sudo chmod +x /usr/local/bin/protoc
```


# ⚠️ Error 2 Fix: Memory Allocation or "Killed" Error
If you see memory allocation error like "Killed" or "Aborted (core dumped)", run:
```bash
sudo fallocate -l 10G /swapfile && \
sudo chmod 600 /swapfile && \
sudo mkswap /swapfile && \
sudo swapon /swapfile && \
echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab
```

---

📱 TIP: You can use multiple devices with your node!
`For any Error/Feedback dm me @Shinosuka_eth on Telegram, Twitter and Discord.`

