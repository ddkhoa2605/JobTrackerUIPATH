# Job Tracker – UiPath Automation  
Robotic automation project built on **UiPath REFramework** to process job data, generate reports, and manage workflow information.

---

## Project Structure
- **Documentation/** – Tài liệu mô tả chi tiết quy trình và cách triển khai  
- **Data/Input/** – Chứa file Excel đầu vào  
- **Data/Input/TemplateHTML/** – Chứa file template HTML  
- **UIForm/** – Các form giao diện nếu cần sử dụng  
- **Trigger/** – Các workflow trigger  
- **Main.xaml** – Entry point của toàn bộ automation

---

## REFramework Overview
Dự án được xây dựng dựa trên **Robotic Enterprise Framework**, bao gồm:

### **1. Initialize Process**
- `InitiAllSettings.xaml` – Load Config.xlsx và Orchestrator assets  
- `GetAppCredential.xaml` – Lấy credential từ Orchestrator hoặc Windows Credential Manager  
- `InitiAllApplications.xaml` – Mở ứng dụng và đăng nhập (nếu có)

### **2. Get Transaction Data**
- `GetTransactionData.xaml` – Lấy transaction từ Orchestrator Queue hoặc nguồn dữ liệu đã cấu hình

### **3. Process Transaction**
- `Process.xaml` – Thực hiện logic xử lý transaction  
- `SetTransactionStatus.xaml` – Cập nhật trạng thái: **Success**, **Business Rule Exception**, **System Exception**

### **4. End Process**
- `CloseAllApplications.xaml` – Đóng ứng dụng, logout và cleanup

---

## Usage Instructions

### **1. Chuẩn bị dữ liệu**
- Đặt file Excel vào thư mục: Data/Input


- Đặt file HTML template vào: Data/Input/TemplateHTML

- 
### **2. Chạy bot**
- Mở **Main.xaml** trong UiPath Studio  
- Bấm **Run** để chạy workflow

### **3. Tùy chỉnh (nếu cần)**
- Chỉnh sửa form trong thư mục **UIForm/**  
- Thay đổi trigger trong thư mục **Trigger/**  
- Cập nhật file **Config.xlsx** nếu cần thêm biến, setting hoặc đường dẫn

---

## Notes
- Đảm bảo file Excel và HTML template được đặt đúng thư mục để bot có thể đọc và xử lý.  
- Khi tạo dự án mới dựa trên REFramework:
1. Xem và chỉnh sửa Config.xlsx  
2. Tùy chỉnh InitiAllApplications.xaml & CloseAllApplications.xaml  
3. Cấu hình GetTransactionData.xaml & SetTransactionStatus.xaml  
4. Xây dựng logic xử lý trong Process.xaml

---

## Documentation
Tất cả tài liệu mô tả chi tiết nằm trong thư mục:


