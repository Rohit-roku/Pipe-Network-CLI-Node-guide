# CLI Node Run Full Guide (PC)

## Official Documentation
🔗 [Pipe Network Devnet-2 Docs](https://docs.pipe.network/devnet-2)

---

## 1️⃣ Install Dependencies (Windows & Linux)
```bash
sudo apt update && sudo apt upgrade -y
```

## 2️⃣ Download Required Files
```bash
curl -L -o pop "https://dl.pipecdn.app/v0.2.8/pop"
chmod +x pop
```

## 3️⃣ Create a Directory for Cache
```bash
mkdir download_cache
```

## 4️⃣ Sign Up Your Account
```bash
./pop --signup-by-referral-route 782d869b0b544d9b
```

### Generate Your Referral Code
```bash
./pop --gen-referral-route
```

## 5️⃣ Start Your Node
```bash
sudo ./pop --ram 8 --max-disk 500 --cache-dir /data --pubKey <KEY>
```

> **Note:** Replace `<KEY>` with your Solana public key (from Phantom, Backpack, etc.)

## 📌 Save Node Info
```bash
nano ~/node_info.json
```

## 📊 Monitor Your Node Status & Points
```bash
./pop --status
./pop --points
```

📌 **Check Your Node Dashboard:** [Pipe Network Dashboard](https://dashboard.pipenetwork.com/node-lookup)

## 🔄 Restart Node Daily
```bash
sudo ./pop --ram 8 --max-disk 500 --cache-dir /data --pubKey <KEY>
```

## ⬆️ Upgrade Node to v0.2.8
```bash
curl -L -o pop "https://dl.pipecdn.app/v0.2.8/pop"
chmod +x pop
```

### Start Node After Upgrade
```bash
sudo ./pop --ram 8 --max-disk 500 --cache-dir /data --pubKey <KEY>
```

## 🔓 Free Port 8003 (If Needed)

### Check which process is using port 8003
```bash
sudo ss -tulpn | grep 8003
```
Example Output:
```bash
LISTEN  0  128  0.0.0.0:8003  0.0.0.0:*  users:("nginx",pid=1234,fd=6)
```

### Kill the process using the port
```bash
sudo kill -9 1234
```

### Kill all processes using port 8003
```bash
sudo fuser -k 8003/tcp
```

---

### ✅ Your Node is Now Set Up & Running!

If you found this guide helpful, consider giving it a ⭐ on GitHub!
