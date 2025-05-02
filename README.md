# Medical-chatbot_v3_Llama
# 🩺 AIMO MED - Sağlık Chatbotu

Bu proje, Türkçe ve İngilizce tıbbi sorulara yanıt verebilen bir **sağlık asistanı chatbot** uygulamasıdır.  
Streamlit + Hugging Face Llama3 tabanlıdır.

## 📦 Gereksinimler

Bu projeyi çalıştırmadan önce aşağıdaki paketleri yüklemeniz gerekir:

```bash
!pip install transformers accelerate bitsandbytes peft --quiet streamlit
!pip install python-dotenv
!pip install PyPDF2 faiss-cpu sentence-transformers langchain
!pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118 --quiet
!pip install --upgrade langchain langchain-community faiss-cpu PyPDF2 sentence-transformers
!npm install -g localtunnel
```

Google Drive erişimi gerekiyorsa:

```python
from google.colab import drive
drive.mount('/content/drive')
https://drive.google.com/file/d/1jTZNq9NCANJn3Rs-z3hI69GcRlosbY-0/view?usp=drive_link
```

Hugging Face girişi:

```python
from huggingface_hub import login
login("your_huggingface_token")
```

---

## 🛠️ Kullanım

Colab ortamında veya kendi bilgisayarınızda aşağıdaki adımları takip ederek çalıştırabilirsiniz:

### 1. Modeli ve kodları hazırlayın

`app.py` dosyasını oluşturun (bu dosyada chatbot arayüzü ve model entegrasyonu vardır).

### 2. Streamlit sunucusunu başlatın

```bash
!curl https://loca.lt/mytunnelpassword
!streamlit run app.py & npx localtunnel --port 8501
```

Bu komut:
- `streamlit` sunucusunu başlatır.
- `localtunnel` ile size bir internet bağlantı adresi (URL) sağlar.
- Bu URL üzerinden chatbotunuza her yerden erişebilirsiniz!

---

## 📸 Ekran Görüntüsü
![WhatsApp Görsel 2025-04-26 saat 02 19 48_ff3c0a6a](https://github.com/user-attachments/assets/1ceaf071-8f25-4d20-9739-e36eb4414f2f)

![WhatsApp Görsel 2025-04-26 saat 02 30 06_a9ce5ebb](https://github.com/user-attachments/assets/c0c0ab7c-142b-4f50-a9d1-51cd212e427a)

📎 RAG (Retrieval-Augmented Generation) Özelliği
![WhatsApp Görsel 2025-05-03 saat 00 51 30_9beb3c53](https://github.com/user-attachments/assets/b8f03b7e-e608-4d98-a287-b729e733be3e)

---

## 📑 Notlar

- Model Adı: **OnurYantira/llama3-8b-turkish-english-medical-merged**
- Token veya model erişimi için Hugging Face hesabınız olmalıdır.
  
