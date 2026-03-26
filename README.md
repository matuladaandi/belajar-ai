# Belajar-AI
Assalamulaikum semua, ini khusus dokumentasi belajar ai yang saya pelajari menggunakan deepseet ai ,youtube &amp; sumber lainnya
# Pastikan python 3. version ke atas
# saya menggunakan OS Zorin OS 17.3 x86_64
laptop 81H6 Lenovo ideapad 130-14IKB
CPU Intel i3-7020U (4) @ 2.300GHz 
GPU Intel HD Graphics 620
RAM 8GB


# Update Sistem & Install Dependencies, ketik pada Terminal
# 1. Update sistem
sudo apt update && sudo apt upgrade -y

# 2. Install tools dasar yang diperlukan
sudo apt install -y python3-pip python3-venv python3-dev build-essential git wget curl

# 3. Install pip terbaru
python3 -m pip install --upgrade pip

# 4. Install tools tambahan untuk AI
sudo apt install -y libatlas-base-dev libopenblas-dev liblapack-dev
sudo apt install -y libjpeg-dev zlib1g-dev libtiff-dev libfreetype6-dev


# Buat Virtual Environment pada terminal
# 1. Buat folder utama untuk belajar AI
mkdir ~/belajar-ai
cd ~/belajar-ai

# 2. Buat virtual environment
python3 -m venv ai_env

# 3. Aktifkan environment (lakukan ini setiap kali buka terminal baru)
source ai_env/bin/activate

# 4. Anda akan melihat (ai_env) muncul di depan prompt terminal
# Contoh: (ai_env) user@zorin:~/belajar-ai$

Ingat: Setiap kali buka terminal baru, Anda harus menjalankan:
cd ~/belajar-ai
source ai_env/bin/activate


# Install Library AI pada terminal
# Install library dasar yang ringan untuk RAM 8GB
pip install numpy pandas matplotlib seaborn scikit-learn

# Install Jupyter Lab (alternatif Google Colab di laptop Anda)
pip install jupyterlab

# Install TensorFlow (versi CPU-only lebih ringan untuk RAM 8GB)
pip install tensorflow-cpu

# Install PyTorch (opsional, pilih salah satu saja dulu)
# Untuk CPU-only lebih ringan:
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu

# Install tools tambahan
pip install tqdm pillow opencv-python



# Test Installasi
# Buat file test, pada folder yang tadi dibuat
nano test_ai.py

# test_ai.py
import sys
print(f"Python version: {sys.version}")

import numpy as np
print(f"NumPy version: {np.__version__}")

import pandas as pd
print(f"Pandas version: {pd.__version__}")

import sklearn
print(f"Scikit-learn version: {sklearn.__version__}")

import matplotlib
print(f"Matplotlib version: {matplotlib.__version__}")

# Test TensorFlow
import tensorflow as tf
print(f"TensorFlow version: {tf.__version__}")
print(f"TensorFlow dapat berjalan: {tf.executing_eagerly()}")

print("\n✅ SEMUA LIBRARY BERHASIL DIINSTALL!")

python test_ai.py



# Setup Jupyter Lab (IDE untuk AI)
# Jalankan Jupyter Lab pada terminal
jupyter lab

# Ini akan membuka browser otomatis. Jika tidak terbuka, buka browser dan ketik:
http://localhost:8888


# Struktur folder rekomend
~/belajar-ai/
├── ai_env/                 # Virtual environment (jangan diutak-atik)
├── notebooks/              # Tempat menyimpan file .ipynb
├── datasets/               # Tempat download dataset
├── projects/               # Project-project Anda
│   ├── 01_hello_world/
│   ├── 02_prediksi_harga/
│   └── ...
└── scripts/                # Script Python biasa


