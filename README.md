# Phân tích dữ liệu thông minh - Đồ án thực hành

## Exploring Mental Health Data

Đồ án thực hiện pipeline xử lý dữ liệu và xây dựng mô hình dự đoán cho bài toán phân loại Depression.  
Bao gồm các bước: **EDA, tiền xử lý dữ liệu, feature engineering, model selection và đánh giá mô hình**.

- Notebook thực nghiệm: `./notebooks`  
- Dependencies: `requirements.txt`
- Link Kaggle: https://www.kaggle.com/competitions/playground-series-s4e11/data
- Link Dataset(drive): https://drive.google.com/drive/folders/1MeWVGiucfoF8xcig-vuOCk5ZDeXjif4y?usp=sharing
- Link github: https://github.com/quanpro147/Exploring-Mental-Health-Data.git

---

## 1. Thông tin nhóm

- Lê Hà Thanh Chương  
- Lê Thượng Đế  
- Mai Đức Minh Huy  
- Vũ Nguyễn Trung Hiếu  
- Nguyễn Trần Trung Kiên  
- Phan Ngọc Quân  

---

## 2. Phân công công việc

- **Lê Hà Thanh Chương**: EDA  
- **Lê Thượng Đế**: Tiền xử lý dữ liệu  
- **Mai Đức Minh Huy**: Xây dựng đặc trưng  
- **Vũ Nguyễn Trung Hiếu**: Encoding & Scaling  
- **Nguyễn Trần Trung Kiên**: Xây dựng mô hình  
- **Phan Ngọc Quân**: Thực nghiệm, đánh giá, viết report  

---

## 3. Cấu trúc project
```
EXPLORING-MENTAL-HEALTH-DATA/
├── artifacts/
│   ├── models/
│   ├── scalers/
│   ├── outputs/
│   └── images/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── EDA_preprocessing.ipynb
│   ├── feat_engineering.ipynb
│   └── model_selection.ipynb
├── requirements.txt
└── README.md
```
---

## 4. Pipeline xử lý dữ liệu

### 1. EDA & Preprocessing
- Phân tích phân phối dữ liệu  
- Xử lý missing values  
- Xử lý outliers  
- Chuẩn hóa dữ liệu  

### 2. Feature Engineering
- Feature selection 
- Encoding categorical features  
- Scaling numerical features  
 

### 3. Model Selection 
- Xử lý mất cân bằng (SMOTE)  
- Huấn luyện mô hình  
- Đánh giá mô hình

---


## 5. Hướng dẫn cài đặt môi trường
Yêu cầu: python = 3.13

### 5.1. Cách 1 - Conda

```bash
conda create -n ptdltm python=3.13 -y
conda activate ptdltm
pip install -r requirements.txt
python -m ipykernel install --user --name ptdltm --display-name "Python (ptdltm)"
```

### 5.2. Cách 2 - uv

```bash
# Cài uv (nếu máy chưa có)
pip install uv

# Tạo và kích hoạt môi trường
uv venv .venv
# Windows PowerShell
.\.venv\Scripts\Activate.ps1
# Linux/macOS
source .venv/bin/activate

# Cài dependencies
uv pip install -r requirements.txt

# Đăng ký kernel cho Jupyter
python -m ipykernel install --user --name ptdltm --display-name "Python (ptdltm)"
```

### 5.3. Cách 3 - venv

```bash
python -m venv .venv
# Windows PowerShell
.\.venv\Scripts\Activate.ps1
# Linux/macOS
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
python -m ipykernel install --user --name ptdltm --display-name "Python (ptdltm)"
```
---

## 6. Cách chạy project

### Bước 1: Clone repo
```bash
git clone https://github.com/quanpro147/Exploring-Mental-Health-Data.git
cd Exploring-Mental-Health-Data
```

### Bước 2: Tải dataset
Tải dataset theo link drive hoặc link kaggle ở trên, sau đó đặt 2 file train.csv và test.csv vào folder data/raw

### Bước 3: Tạo môi trường
python -m venv venv
source venv/bin/activate  # hoặc venv\Scripts\activate trên Windows

### Bước 4: Cài thư viện
pip install -r requirements.txt

### Bước 5: Chạy notebook
Mở thư mục notebooks/

Chạy lần lượt:

- EDA_preprocessing.ipynb
- feat_engineering.ipynb
- model_selection.ipynb
