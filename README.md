# 📊 Enterprise Fraud Data Analysis (2010–2019)

## 📌 Tổng quan dự án

Dự án tập trung vào **phân tích dữ liệu giao dịch quy mô lớn của doanh nghiệp**
trong giai đoạn **2010–2019**, nhằm khai thác insight về:

- Hành vi chi tiêu của khách hàng  
- Dòng tiền và phân bổ chi tiêu  
- Rủi ro gian lận (fraud) trong hệ thống giao dịch  

Dự án được thực hiện dưới góc nhìn của một **Data Analyst / Data Scientist**,
đóng vai trò hỗ trợ doanh nghiệp trong việc hiểu khách hàng và quản lý rủi ro dựa trên dữ liệu.

---

## 🎯 Mục tiêu phân tích

- Phân tích hành vi chi tiêu của khách hàng theo từng giao dịch  
- So sánh xu hướng giao dịch **trả trước** và **trả sau**  
- Xây dựng chân dung **khách hàng chi tiêu cao**  
- Phân tích **dòng tiền chủ yếu chảy về đâu**  
- Xác định **thời điểm rủi ro gian lận cao nhất**  
- Quan sát sự thay đổi của các yếu tố trên trong giai đoạn **2010–2019**

---

## 📂 Dữ liệu sử dụng

Dự án sử dụng nhiều bảng dữ liệu đại diện cho các thành phần khác nhau của hệ thống giao dịch:

- `users_data.csv` – Thông tin khách hàng  
- `cards_data.csv` – Thông tin thẻ thanh toán  
- `transactions_data.csv` – Dữ liệu giao dịch  
- `mcc_codes.csv` – Danh mục ngành nghề (Merchant Category Code)  
- `train_fraud_labels.csv` – Nhãn gian lận phục vụ phân tích

⚠️ Raw data files are not included in this repository due to file size limitations and data privacy considerations.

---

## ❓ Câu hỏi phân tích chính

- Khách hàng chi tiêu bao nhiêu trong mỗi giao dịch?  
- Khách hàng có xu hướng sử dụng giao dịch trả trước hay trả sau?  
- Chân dung khách hàng chi tiêu nhiều nhất là ai?  
- Dòng tiền của khách hàng chủ yếu chảy về đâu?  
- Thời điểm nào rủi ro bị tấn công gian lận (fraud) cao nhất?  
- Các đặc điểm trên thay đổi như thế nào theo thời gian (2010–2019)?

---

## 🧠 Phương pháp & kỹ thuật sử dụng

- Exploratory Data Analysis (EDA)  
- Thống kê mô tả  
- Trực quan hóa dữ liệu theo thời gian  
- Phân tích phân phối và xu hướng  
- So sánh nhóm khách hàng và loại giao dịch  

---

## 📈 Kết quả & Insight chính

- Xác định rõ **nhóm khách hàng chi tiêu cao** và đặc điểm hành vi của họ  
- Phát hiện sự khác biệt rõ ràng giữa **giao dịch trả trước và trả sau**  
- Dòng tiền tập trung vào một số **nhóm ngành cụ thể**  
- Rủi ro gian lận có xu hướng tăng cao tại một số **thời điểm và kịch bản nhất định**  
- Xu hướng chi tiêu và rủi ro thay đổi rõ rệt theo thời gian  

---

## 🛠️ Công cụ & công nghệ

- Python  
- Pandas, NumPy  
- Matplotlib / Seaborn  
- Jupyter Notebook  

---

## 📌 Trạng thái dự án

- Hoàn thành phân tích EDA  
- Phục vụ mục đích **học tập, nghiên cứu và xây dựng portfolio cá nhân**  
- Có thể mở rộng sang:
  - Machine Learning cho Fraud Detection  
  - Feature Engineering  
  - Dashboard giám sát gian lận  

---

## 👤 Tác giả

**Trịnh Ngọc Minh Nhật**  
*Data Analyst / Data Science Student*



