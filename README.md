# BT6_Lenh_Select
# PHƯƠNG THỊ ÁNH NGUYỆT - K225480106098
Yêu cầu bài tập: 
Cho file sv_tnut.sql 
1. Hãy nêu các bước để import được dữ liệu trong sv_tnut.sql vào sql server của em
2. Dữ liệu đầu vào là tên của sv; sđt; ngày, tháng, năm sinh của sinh viên (của sv đang làm bài tập này)
3. Nhập sql để tìm xem có những sv nào trùng hoàn toàn ngày/tháng/năm với em?
4. Nhập sql để tìm xem có những sv nào trùng ngày và tháng sinh với em?
5. Nhập sql để tìm xem có những sv nào trùng tháng và năm sinh với em?
6. Nhập sql để tìm xem có những sv nào trùng tên với em?
7. Nhập sql để tìm xem có những sv nào trùng họ và tên đệm với em.
8. Nhập sql để tìm xem có những sv nào có sđt sai khác chỉ 1 số so với sđt của em.
9. BẢNG SV CÓ HƠN 9000 ROWS, HÃY LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG  VIỆT, GIẢI THÍCH.
10. HÃY NHẬP SQL ĐỂ LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV (TRÌNH BÀY QUÁ TRÌNH SUY NGHĨ VÀ GIẢI NHỮNG VỨNG MẮC)

DEADLINE: 23H59:59 NGÀY 25/4/2025

Ghi chú: Giải thích tại sao lại có SQL như vậy.

# BÀI LÀM.
1. Các bước để impost được dữ liệu
- Tạo 1 data base mới đặt tên là SV_TNUT.
  
   ![image](https://github.com/user-attachments/assets/86448a22-4cfa-449b-a839-2423655efbb7)
  
- Trên thanh công cụ → Chọn File → Open 
- Duyệt đến file sv_tnut.sql → Open

  ![image](https://github.com/user-attachments/assets/d9e4936a-a24c-469e-b47e-dd26e09e0244)

  - Kết quả sau khi import.

  ![image](https://github.com/user-attachments/assets/2049da72-2593-47b2-8fbf-331d76e0bf3a)
  
2. Dữ liệu đầu vào là thông tin của cá nhân em.
   
  ![image](https://github.com/user-attachments/assets/8f21dd98-e8aa-46c2-973f-5211d5d8f2bc)

3. Nhập ngày sinh 07-01-2004 thì có từng này người trùng hoàn toàn ngày sinh với em.

  ![image](https://github.com/user-attachments/assets/bdc2e5ee-0ecb-486a-90d6-ea377b5a014d)

4. Nhập sql để tìm xem có những sv nào trùng ngày 07 và tháng sinh 01 với em.
   
  ![image](https://github.com/user-attachments/assets/cea5cbc0-ea4d-434b-9032-daf878efc894)
  
5. Nhập sql để tìm xem có những sv nào trùng tháng 01 và năm sinh 2004 với em.
   
  ![image](https://github.com/user-attachments/assets/ec2d0d94-6e80-4a03-96ca-a3e340d334a6)

6. Nhập sql để tìm xem có những sv nào trùng tên Nguyệt với em.

  ![image](https://github.com/user-attachments/assets/e97723ea-b290-4e18-84e1-fb5ff8721ba0)

7. Nhập sql để tìm xem có những sv nào trùng họ và tên đệm với em.

   ![image](https://github.com/user-attachments/assets/03cd0d6f-5bbf-43d2-8c65-819c0b9a54ca)

8. Nhập sql để tìm xem có những sv nào có sđt sai khác chỉ 1 số so với sđt của em.

  ![image](https://github.com/user-attachments/assets/7c23307b-8b06-42f8-8d34-3a69125a9f44)

9. BẢNG SV CÓ HƠN 9000 ROWS, HÃY LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG  VIỆT, GIẢI THÍCH.

   ![image](https://github.com/user-attachments/assets/adfa33a7-1cae-4e59-8b29-4384ad195a23)


- Giải thích:
  
+ Lop LIKE 'K%KMT%'	chọn các lớp có chứa mã ngành KMT (ví dụ: K60KMT.K01)
  
+ ORDER BY ten, hodem: sắp xếp theo tên trước rồi mới thêm họ đệm
  
+ COLLATE Vietnamese_CI_AS: đảm bảo sắp xếp kiểu tiếng Việt có phân biệt dấu (collation chuẩn)
  
+ "Vietnamese_CI_AS" cho phép sắp xếp đúng theo thứ tự tiếng Việt.

10. HÃY NHẬP SQL ĐỂ LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV (TRÌNH BÀY QUÁ TRÌNH SUY NGHĨ VÀ GIẢI NHỮNG KHÚC MẮC)

  ![image](https://github.com/user-attachments/assets/af26a4b5-55eb-4049-a777-7abc38a42923)

- Nếu áp dụng theo cách này thì độ chính xác không thể chuẩn chỉnh 100% vì ngay từ dữ liệu ban đầu chưa cho cột giới tính. Vì vậy em đã tìm kiếm tên đệm của người có chữ "Thị" thuộc ngành "KMT" vì một phần nữ giới Việt Nam khi đặt tên thường hay có chữ này. Tuy nhiên đây cũng chỉ là một cách phổ thông nhưng chỉ hiệu quả 1 phần.

  ![image](https://github.com/user-attachments/assets/487b336a-ea13-43a3-8e81-96071f46f4a6)

  
- Em có thêm một cách nữa là liệt kê nhiều họ đệm và tên nữ tính phổ biến hơn ở Việt Nam để tìm kiếm thì kết quả vẫn không nhỉnh hơn là bao và không thể triệt để 😀😀😀

==> Vậy cách tốt nhất để không phí thời gian và công sức mà kết quả chuẩn 100% ta nên thêm trường giới tính vào ngay từ khi bắt đầu làm bài. 
