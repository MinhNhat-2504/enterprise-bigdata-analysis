# Phân tích giao dịch & gian lận doanh nghiệp (2010–2019)

Project phân tích khoảng **13,3 triệu giao dịch thẻ** của một doanh nghiệp trong giai đoạn 2010–2019. Mình đặt mình vào vai một Data Analyst của công ty và cố gắng trả lời mấy câu hỏi mà bất kỳ doanh nghiệp nào cũng quan tâm: khách hàng đang chi tiêu như thế nào, tiền chảy về đâu, ai là nhóm khách đáng giá nhất, và kẻ gian thường ra tay vào lúc nào.

Toàn bộ quá trình phân tích nằm trong notebook [enterprise_fraud_analysis.ipynb](enterprise_fraud_analysis.ipynb), kèm nhận xét và đề xuất giải pháp sau mỗi biểu đồ.

## Dữ liệu

Bộ dữ liệu gồm 5 bảng mô phỏng hệ thống giao dịch của một doanh nghiệp:

| File | Nội dung | Quy mô |
|---|---|---|
| `transactions_data.csv` | Lịch sử giao dịch | ~13,3 triệu dòng (hơn 1GB) |
| `users_data.csv` | Thông tin khách hàng | ~2.000 khách |
| `cards_data.csv` | Thông tin thẻ | ~6.100 thẻ |
| `mcc_codes.csv` | Danh mục ngành nghề (MCC) | ~110 mã |
| `train_fraud_labels.csv` | Nhãn gian lận | — |

Dữ liệu gốc không được đưa lên repo vì dung lượng quá lớn (riêng bảng giao dịch đã hơn 1GB). Muốn chạy lại notebook thì cần tải dữ liệu về và đặt vào thư mục `data/`.

## Cách làm

Vì dữ liệu khá nặng so với việc xử lý bằng pandas trên máy cá nhân, bước đầu tiên là làm sạch và tối ưu bộ nhớ: strip ký hiệu `$` ở các cột tiền tệ, ép kiểu (downcast) toàn bộ cột số để giảm RAM, và chủ động `del` + `gc.collect()` sau mỗi lần merge. Sau đó ghép cả 5 bảng lại thành một bảng lớn duy nhất rồi khai thác bằng EDA — thống kê mô tả, phân tích phân phối và trực quan hóa theo thời gian với matplotlib/seaborn.

## Một vài phát hiện chính

- Phần lớn giao dịch có giá trị nhỏ. Doanh thu của công ty phụ thuộc vào **số lượng đơn** chứ không phải giá trị mỗi đơn — khách khá nhạy cảm về giá.
- Khách nghiêng hẳn về thẻ **debit (trả trước)**: tâm lý có bao nhiêu tiêu bấy nhiêu thay vì vay mượn trả sau.
- Chi tiêu theo độ tuổi có hình chữ U: nhóm trung niên 35–55 dè dặt nhất, trong khi nhóm trẻ và nhóm lớn tuổi lại sẵn sàng chi nhiều hơn trên mỗi đơn.
- Doanh thu tăng đều gần cả thập kỷ nhưng **sụt mạnh vào năm 2019** — dấu hiệu đáng lo cần điều tra thêm.
- Điều bất ngờ nhất: gian lận không diễn ra lén lút lúc nửa đêm như mình nghĩ, mà **dồn vào giờ hành chính** — kẻ gian trà trộn vào lúc lượng giao dịch thật cao nhất để qua mặt hệ thống kiểm soát.

Chi tiết từng phân tích kèm biểu đồ và đề xuất giải pháp đều có trong notebook.

## Công cụ

Python (pandas, numpy, matplotlib, seaborn), chạy trên Jupyter Notebook.

## Hướng phát triển

Hiện tại project mới dừng ở EDA. Nếu có thời gian mình muốn thử xây model phát hiện gian lận (dữ liệu đã có sẵn nhãn) và làm một dashboard theo dõi giao dịch bất thường.

---

**Trịnh Ngọc Minh Nhật** — Data Analyst / Data Science Student
