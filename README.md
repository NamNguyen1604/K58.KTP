# K58.KTP -Bài tập 03: - Môn Hệ quản trị CSDL - Nguyễn Phương Nam 
# Bài toán:
 Sửa bài 2 để có csdl như sau:

 SinhVien(#masv,hoten,NgaySinh)
 Lop(#maLop,tenLop)
 GVCN(#@maLop,#@magv,#HK)
 LopSV(#@maLop,#@maSV,ChucVu)
 GiaoVien(#magv,hoten,NgaySinh,@maBM)
 BoMon(#MaBM,tenBM,@maKhoa)
 Khoa(#maKhoa,tenKhoa)
 MonHoc(#mamon,Tenmon,STC)
 LopHP(#maLopHP,TenLopHP,HK,@maMon,@maGV)
 DKMH(#id_dk, @maLopHP,@maSV,DiemThi,PhanTramThi)
 Diem(#id, @id_dk, diem)
# Yêu cầu:
 Sửa bảng DKMH và bảng Điểm từ bài tập 2 để có các bảng như yêu cầu.
 Nhập dữ liệu demo cho các bảng (nhập có kiểm soát từ tính năng Edit trên UI của mssm)
 Viết lệnh truy vấn để: Tính được điểm thành phần của 1 sinh viên đang học tại 1 lớp học phần.
# Bài làm:
# Bước 1. Sửa bảng DKMH và thêm bảng điểm vào Databases QLSV
 Bảng DKMH sau khi sửa: Thêm cột id_dk và đặt id_dk làm khóa chính trong bảng:

![image](https://github.com/user-attachments/assets/0dbd0569-a687-4c94-a79b-099ba794dbe0)
 
 Thêm bảng Diem vào databaese :

![image](https://github.com/user-attachments/assets/972c9433-ef3e-4498-9399-a6e78f27f3b5)

 Tạo khóa ràng buộc (CK) cho cột Diem :

 ![image](https://github.com/user-attachments/assets/a6238766-d0c0-4c52-934f-97e1881f2315)

 Tạo khóa ngoại (FK) cho bảng điểm: 

 ![image](https://github.com/user-attachments/assets/cfc3b4d8-32b6-406a-a97d-9a59166a1607)

 # Bước 2 : Tạo Diagrams
 Diagrams của csdl QLSV
 ![image](https://github.com/user-attachments/assets/f55c74e5-8797-4b06-afb2-6496339c82e1)
 ![image](https://github.com/user-attachments/assets/44628782-0769-425e-a5af-721307137302)
 
 # Nhập dữ liệu demo cho bảng 
-Nhập dữ liệu demo cho các bảng (nhập có kiểm soát từ tính năng Edit trên UI của mssm).
-Nhập dữ liệu cho một số bảng như SinhVien, MonHoc, LopHP, DKMH, Diem để phục vụ quá trình tính điểm thành phần sau này.
![image](https://github.com/user-attachments/assets/c52c4809-a9d0-45fb-80e9-555463f0611c)

![image](https://github.com/user-attachments/assets/b2dd561c-bb59-431a-a40e-42fb3e9b46b5)

![image](https://github.com/user-attachments/assets/9e749f1f-116a-41a7-b8f0-3d0103d19820)

![image](https://github.com/user-attachments/assets/4ff6df74-ead8-4f8e-94a7-8346fe163e00)

![image](https://github.com/user-attachments/assets/92fcaac2-9028-416f-9443-648f1c65153c)

![image](https://github.com/user-attachments/assets/9be49788-d27f-4da3-96c0-8926b3366a4b)

![image](https://github.com/user-attachments/assets/57517569-9682-4221-b5ca-8cabc3324ce5)

![image](https://github.com/user-attachments/assets/fd4a82c7-cc52-4ff2-bece-6ec2dbf7903f)

# Bước 3 : Lệnh truy vấn để tính điểm thành phần của sinh viên
-Click chuột phải vào database QLSV sau đó nhấn New Query tạo trang truy vấn mới để nhập code.
![image](https://github.com/user-attachments/assets/890eae2e-f9af-4823-9c2d-654ab77f13b2)
