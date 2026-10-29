


# Phần 1: Phân tích bài toán (I/O) : 
1. **xác định đầu vào & đầu ra** :
- đầu vào : 
   + 4 nhóm người dùng
   + 4 loại tài liệu chính 
   + Các ràng buộc bảo mật
 - đầu ra  : 
   + Cấu trúc thư mục Google Drive 2 cấp tối ưu phân quyền
   + phân quyền chi tiết
   + Phương án xử lý cụ thể cho 3 bẫy dữ liệu
  2. **đề xuất giải pháp** : 
  - **Expiration Date** (cấp dự án)
    + Ban_Ky_Thuật
    + Ban_Thiet_Ke
    + Ban_Kinh_Doanh
    + nha-dau-tu-tiem-nang 
   
    3. **thiết kế các bước** : 
    - **bước 1 :** tạo thư mục và đặt tên 
    - **bước 2 :** cài đặt bảo mật 
    - **bước 3 :** cấp quyền 
    - **bước 4 :** kiểm tra và vận hành 
     # Phần 2: Triển khai & Chống lỗi : 
     **1. bảng phân quyền hoàn chỉnh**
    |Loại tài liệu|Ban KT|Ban TK|Ban KD|Nhà đầu tư|Ghi chú bảo mật|
    |-|-|-|-|-|-| 
    |Mã nguồn|Editor|No Access|No Access|No Access|Restricted tuyệt đối|
    |Tài liệu Thiết kế|Viewer|Editor|No Access|No Access|Chia sẻ chéo giữa KT và TK|
    |Business Plan gốc|Viewer|No Access|Editor|No Access|Cấm tải xuống|
    |Slide Pitch|Viewer|Viewer|Editor|Viewer|Dùng chung để họp nhóm|
    |Thư mục Nhà đầu tư|No Access|No Access|Editor|Viewer|Cài đặt expiration date|
    **2. Trả lời 3 bẫy dữ liệu :**  
    - muốn chia sẻ Business Plan cho Kỹ thuật xem context nhưng không cho sửa -> cấp quyền **viewer** 
    - muốn tải PDF Slide Pitch để xem offline nhưng tránh bị chỉnh sửa -> cấp quyền **Viewer**
    - Thành viên nghỉ việc — cần ngắt quyền truy cập ngay lập tức -> **Xóa trực tiếp email của nhân sự đó**
    
  
