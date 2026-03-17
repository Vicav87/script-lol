# 💻 Setup Linux WSL (Windows 10 e 11)

Guia para instalar e rodar o **Linux com interface gráfica (desktop)** dentro do Windows usando WSL.

---

# 🟦 Windows 11 (Recomendado)

## 🚀 1️⃣ Instalar WSL + Ubuntu

⚡ **Execute no CMD como administrador:**

```bash
wsl --install -d Ubuntu
```

🧠 Esse comando:
- Ativa o WSL
- Instala o Ubuntu
- Configura automaticamente

🔁 Depois, reinicie o computador.

---

## 🔄 2️⃣ Atualizar o sistema

```bash
sudo apt update && sudo apt upgrade -y
```

📌 Mantém tudo atualizado e evita erros.

---

## 🖥️ 3️⃣ Instalar interface gráfica (XFCE)

```bash
sudo apt install xfce4 xfce4-goodies -y
```

📌 XFCE é leve, estável e ideal para WSL.

---

## ▶️ 4️⃣ Iniciar o desktop

```bash
startxfce4
```

💥 Abre:
- Área de trabalho
- Janelas
- Mouse funcionando
- Ambiente gráfico completo

---

# 🟨 Windows 10 (Modo Compatível)

## ⚙️ 1️⃣ Ativar recursos do sistema

⚡ **Execute no CMD como administrador:**

```bash
dism /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

```bash
dism /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

🔁 Reinicie o computador após executar.

---

## 📦 2️⃣ Instalar WSL 2 + Ubuntu

```bash
wsl --set-default-version 2
```

```bash
wsl --install -d Ubuntu
```

---

## 🔄 3️⃣ Atualizar o sistema

```bash
sudo apt update && sudo apt upgrade -y
```

---

## 🖥️ 4️⃣ Instalar interface gráfica

```bash
sudo apt install xfce4 xfce4-goodies -y
```

---

## 🧩 5️⃣ Servidor gráfico (obrigatório no Windows 10)

Instale no Windows:

👉 VcXsrv (X Server para Windows)

Configuração recomendada:
- Multiple windows
- Start no client
- Disable access control

---

## ⚙️ 6️⃣ Configurar display

Dentro do Ubuntu:

```bash
export DISPLAY=localhost:0
```

---

## ▶️ 7️⃣ Iniciar o desktop

```bash
startxfce4
```

---

# 🧠 Comandos Úteis

Atualizar sistema:

```bash
sudo apt update && sudo apt upgrade -y
```

Sair do Linux:

```bash
exit
```

---

# ⚠️ Observações

- Windows 11 possui suporte gráfico nativo.
- Windows 10 pode exigir servidor gráfico externo.
- XFCE foi escolhido por ser leve e estável.