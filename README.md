# Final_Project_DSP501
# DSP501 Final Project - AEC App

## Giới thiệu
AEC App là ứng dụng Python được xây dựng bằng [Toga](https://toga.readthedocs.io/) và [Briefcase](https://briefcase.readthedocs.io/).  
Ứng dụng có thể chạy trên Desktop (Windows/macOS/Linux) và Android.

---

## Yêu cầu

### 1. Python
- Python 3.11 trở lên
- Pip

### 2. Java
- **JDK 17** (cần cho Android)
- Set biến môi trường `JAVA_HOME` trỏ tới JDK 17
powershell
# Windows
setx JAVA_HOME "C:\Program Files\Java\jdk-17"
setx PATH "%JAVA_HOME%\bin;%PATH%"

### 3. Android
- Android Studio + SDK
- Emulator hoặc thiết bị thật với **USB Debugging**
- Biến môi trường ANDROID_HOME trỏ tới SDK (nếu cần)

### 4. Các thư viện Python
- Briefcase, Toga, NumPy, Pyaec, Pytest
- Cài đặt bằng:

pip install -r requirements.txt

## Cấu trúc project
DSP501_Final_Project/
├── pyproject.toml         # cấu hình Briefcase
├── src/
│   └── aec/
│       ├── __init__.py
│       └── app.py         # file chính
├── tests/                 # test code
├── requirements.txt       # dependency Python
└── LICENSE

## Hướng dẫn chạy app

### 1. Desktop (Windows/macOS/Linux)
# Cài các dependencies
pip install -r requirements.txt

# Tạo môi trường Briefcase
briefcase create

# Build app
briefcase build

# Chạy app
briefcase run

### 2. Android
1. Kết nối thiết bị Android hoặc chạy emulator
2. Tạo môi trường Android và build APK

briefcase create android
briefcase build android

3. Cài và chạy app trên thiết bị/emulator

briefcase run android
> Lưu ý: Nếu gặp lỗi liên quan đến JDK hoặc `JAVA_HOME`, hãy kiểm tra phiên bản JDK phải là 17.  

## Chạy test

pytest tests/
## Ghi chú
- Mọi code Python chính viết trong `src/aec/app.py`
- Các module phụ có thể tạo thêm trong `src/aec/`
- Nếu thêm dependency, cập nhật `requirements.txt` và chạy lại:
- 
pip install -r requirements.txt
briefcase build
