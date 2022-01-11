- 👋 Hi, I’m @halong01- phpMyAdmin SQL Dump
- phiên bản 4.8.5
- https://www.phpmyadmin.net/
-
- Máy chủ: 127.0.0.1
- Time made: Th5 11, 2019 lúc 08:26 AM
- Server version: 10.1.38-MariaDB
- PHP version: 7.3.2

SET SQL_MODE =  " NO_AUTO_VALUE_ON_ZERO " ;
ĐẶT AUTOCOMMIT =  0 ;
BẮT ĐẦU GIAO DỊCH ;
SET time_zone =  " +00: 00 " ;


/ * ! 40101 SET @OLD_CHARACTER_SET_CLIENT = @@ CHARACTER_SET_CLIENT * / ;
/ * ! 40101 SET @OLD_CHARACTER_SET_RESULTS = @@ CHARACTER_SET_RESULTS * / ;
/ * ! 40101 SET @OLD_COLLATION_CONNECTION = @@ COLLATION_CONNECTION * / ;
/ * ! 40101 ĐẶT TÊN utf8mb4 * / ;

-
- Database: `quanlyacclienminh`
-

- ------------------------------------------------ --------

-
- Table structure for table `acc_lol_chitiet`
-

TẠO  BẢNG ` acc_lol_chitiet '(
  ' Id_nick_lol '  int ( 11 ) NOT NULL ,
  ' Ten_dang_nhap '  varchar ( 50 ) đối chiếu utf8_unicode_ci NOT NULL ,
  ' Mat_khau '  varchar ( 50 ) đối chiếu utf8_unicode_ci NOT NULL ,
  ' Ten_nhan_vat '  varchar ( 50 ) đối chiếu utf8_unicode_ci NOT NULL ,
  ' So_luong_tuong '  int ( 11 ) NOT NULL ,
  ' So_luong_trang_phuc '  int ( 11 ) NOT NULL ,
  ' Cấp bậc '  varchar ( 50 ) CHARACTER SET utf8 NOT NULL ,
  ' Gia_ban '  int ( 11 ) NOT NULL ,
  ' Trang_thai '  varchar ( 50 ) đối chiếu utf8_unicode_ci NOT NULL
) ENGINE = InnoDB DEFAULT CHARSET = utf8 COLLATE = utf8_unicode_ci;

-
- dump the data for table `acc_lol_chitiet`
-

INSERT INTO  ' acc_lol_chitiet ' ( ' id_nick_lol ' , ' ten_dang_nhap ' , ' mat_khau ' , ' ten_nhan_vat ' , ' so_luong_tuong ' , ' so_luong_trang_phuc ' , ' cấp bậc ' , ' gia_ban ' , ' trang_thai ' ) GIÁ TRỊ
( 1 , ' quanghehe123 ' , ' matkhau1 ' , ' SKTQuang_Quat ' , 15 , 20 , ' bạch kim ' , 75000 , ' chưa bán ' ),
( 2 , ' nick_lol_02 ' , ' matkhaulol02 ' , ' nhanvat02 ' , 10 , 20 , ' bạc ' , 30000 , ' chưa bán ' ),
( 3 , ' nick_lol_03 ' , ' matkhaulol03 ' , ' nhanvat03 ' , 30 , 50 , ' kim cương ' , 150000 , ' chưa bán ' ),
( 4 , ' nick_lol_04 ' , ' matkhaulol04 ' , ' nhanvat04 ' , 20 , 10 , ' bạc ' , 35000 , ' đã bán ' ),
( 5 , ' nick_lol_05 ' , ' matkhaulol05 ' , ' nhanvat05 ' , 10 , 0 , ' đồng ' , 10000 , ' have bán ' ),
( 6 , ' quangthitcho99 ' , ' quangquat123 ' , ' THIT_CHO_10B ' , 29 , 10 , ' kim cương ' , 100000 , ' chưa bán ' ),
( 7 , ' hello123 ' , ' goodbye456 ' , ' SuperSonicc ' , 4 , 5 , ' đồng ' , 50000 , ' chưa bán ' ),
( 9 , ' fdsa ' , ' fdsafdsa ' , ' fdsafdsafdsafdsafdsa ' , 500 , 32 , ' đồng ' , 50000 , ' chưa bán ' );

- ------------------------------------------------ --------

-
- Table structure for table 'admin`
-

TẠO  BẢNG ` admin '(
  ' Id_admin '  int ( 11 ) NOT NULL ,
  ' Tên truy nhập '  varchar ( 50 ) đối chiếu utf8_unicode_ci NOT NULL ,
  ' Mật khẩu '  varchar ( 50 ) đối chiếu utf8_unicode_ci NOT NULL ,
  ' SDT '  varchar ( 50 ) đối chiếu utf8_unicode_ci NOT NULL ,
  ' Email '  varchar ( 50 ) đối chiếu utf8_unicode_ci NOT NULL
) ENGINE = InnoDB DEFAULT CHARSET = utf8 COLLATE = utf8_unicode_ci;

-
- dump the data for table 'admin`
-

INSERT INTO  ' quản trị ' ( ' id_admin ' , ' username ' , ' password ' , ' SDT ' , ' Email ' ) GIÁ TRỊ
( 1 , ' admin01 ' , ' password_admin01 ' , ' 0384221001 ' , ' admin01@gmail.com ' ),
( 2 , ' admin02 ' , ' password_admin02 ' , ' 0384221002 ' , ' admin02@gmail.com ' );

- ------------------------------------------------ --------

-
- Table Architecture for table table `hoadon`
-

TẠO  BẢNG ` hoadon '(
  ' Id_hoa_don '  int ( 50 ) NOT NULL ,
  ' Id_admin '  int ( 11 ) NOT NULL ,
  ' Id_khach_hang '  int ( 11 ) NOT NULL ,
  ' Id_nicklol '  int ( 11 ) NOT NULL ,
  ' Ngay_lap_hoa_don '  ngày  NOT NULL ,
  ' Thanh_tien '  int ( 11 ) NOT NULL
) ENGINE = InnoDB DEFAULT CHARSET = utf8 COLLATE = utf8_unicode_ci;

-
- Đổ vỡ dữ liệu cho bảng `hoadon`
-

INSERT INTO  ' hoadon ' ( ' id_hoa_don ' , ' id_admin ' , ' id_khach_hang ' , ' id_nicklol ' , ' ngay_lap_hoa_don ' , ' thanh_tien ' ) GIÁ TRỊ
( 1 , 1 , 2 , 4 , ' 2019-05-03 ' , 35000 ),
( 2 , 2 , 3 , 5 , ' 2019-05-11 ' , 10000 );

- ------------------------------------------------ --------

-
- Table Structure for table `hoadon_nhapvao`
-

TẠO  BẢNG ` hoadon_nhapvao` (
  ' Id_hoa_don_nhap_vao '  int ( 50 ) NOT NULL ,
  ' Id_nick '  int ( 50 ) NOT NULL ,
  ' Id_admin_mua_vao '  int ( 50 ) NOT NULL ,
  ' Ngay_nhap_vao '  ngày  NOT NULL ,
  ' Gia_tien '  int ( 50 ) NOT NULL
) ENGINE = InnoDB DEFAULT CHARSET = utf8 COLLATE = utf8_unicode_ci;

- ------------------------------------------------ --------

-
- Table Architecture for table `khachhang`
-

TẠO  BẢNG ` khachhang` (
  ' Id_khach_hang '  int ( 11 ) NOT NULL ,
  ' Ten_tai_khoan_dang_nhap '  varchar ( 50 ) đối chiếu utf8_unicode_ci NOT NULL ,
  ' Mat_khau '  varchar ( 50 ) đối chiếu utf8_unicode_ci NOT NULL ,
  ' Ten_khach_hang '  varchar ( 50 ) đối chiếu utf8_unicode_ci NOT NULL ,
  ' SDT '  int ( 11 ) NOT NULL ,
  ' Email '  varchar ( 50 ) đối chiếu utf8_unicode_ci NOT NULL ,
  ' Sodu_TK '  int ( 11 ) NOT NULL
) ENGINE = InnoDB DEFAULT CHARSET = utf8 COLLATE = utf8_unicode_ci;

-
- dump the data for table `khachhang`
-

INSERT INTO  ' khachhang ' ( ' id_khach_hang ' , ' ten_tai_khoan_dang_nhap ' , ' mat_khau ' , ' ten_khach_hang ' , ' SDT ' , ' Email ' , ' Sodu_TK ' ) GIÁ TRỊ
( 2 , ' taikhoan02 ' , ' mk02 ' , ' khachhang02 ' , 2 , ' khachhang02@gmail.com ' , 150000 ),
( 3 , ' taikhoan03 ' , ' mk03 ' , ' khachhang03 ' , 3 , ' khachhang03@gmail.com ' , 100000 ),
( 4 , ' taikhoan04 ' , ' mk04 ' , ' khachhang04 ' , 4 , ' khachhang04@gmail.com ' , 500000 ),
( 5 , ' taikhoan05 ' , ' mk05 ' , ' khachhang05 ' , 5 , ' khachhang05@gmail.com ' , 200000 ),
( 9 , ' taikhoan06 ' , ' mk06 ' , ' khachhang06 ' , 6 , ' khachhang06@gmail.com ' , 250000 ),
( 11 , ' taikhoan08 ' , ' mk08 ' , ' khachhang08 ' , 8 , ' khachhang08@gmail.com ' , 135000 ),
( 16 , ' taikhoan09 ' , ' mk09 ' , ' khachhang09 ' , 9 , ' khachhang09@gmail.com ' , 20000 ),
( 17 , ' taikhoan10 ' , ' mk10 ' , ' khachhang10 ' , 10 , ' khachhang10@gmail.com ' , 0 ),
( 18 , ' taikhoan11 ' , ' mk11 ' , ' khachhang11 ' , 11 , ' khachhang11@gmail.com ' , 10000 ),
( 19 , ' fds ' , ' fdsa ' , ' fdsa ' , 16 , ' fdsa@gmail.com ' , 15615 ),
( 20 , ' taikhoan090 ' , ' fasfsa ' , ' khachvip1 ' , 6530150 , ' vip@gmail.com ' , 50000 );

-
- Chỉ mục cho đổ bảng
-

-
- Index for table `acc_lol_chitiet`
-
ALTER  TABLE  ' acc_lol_chitiet '
  ADD PRIMARY KEY ( ' id_nick_lol ' );

-
- Chỉ mục cho bảng `quản trị`
-
ALTER  TABLE  ` admin '
  ADD PRIMARY KEY ( ' id_admin ' );

-
- Chỉ mục cho bảng `hoadon`
-
 BẢNG  ALTER ` hoadon '
  ADD PRIMARY KEY ( ' id_hoa_don ' ),
  ADD KEY ' fk_id_admin ' ( ' id_admin ' ),
  THÊM TỪ KHÓA ` fk_id_khach_hang ' ( ` id_khach_hang ` ),
  ADD KEY ' fk_nicklol ' ( ' id_nicklol ' );

-
- Index for table `hoadon_nhapvao`
-
ALTER  TABLE  ' hoadon_nhapvao '
  ADD PRIMARY KEY ( ' id_hoa_don_nhap_vao ' );

-
- Index for table `khachhang`
-
 BẢNG  ALTER ` khachhang '
  ADD PRIMARY KEY ( ' id_khach_hang ' );

-
- AUTO_INCREMENT for dump table
-

-
- AUTO_INCREMENT cho bảng `acc_lol_chitiet`
-
ALTER  TABLE  ' acc_lol_chitiet '
  Sửa ' id_nick_lol '  int ( 11 ) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT = 10 ;

-
- AUTO_INCREMENT cho `admin` bảng
-
ALTER  TABLE  ` admin '
  Sửa ' id_admin '  int ( 11 ) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT = 3 ;

-
- AUTO_INCREMENT cho bảng `hoadon`
-
 BẢNG  ALTER ` hoadon '
  Sửa ' id_hoa_don '  int ( 50 ) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT = 4 ;

-
- AUTO_INCREMENT cho table `hoadon_nhapvao`
-
ALTER  TABLE  ' hoadon_nhapvao '
  Sửa ' id_hoa_don_nhap_vao '  int ( 50 ) NOT NULL AUTO_INCREMENT;

-
- AUTO_INCREMENT cho table `khachhang`
-
 BẢNG  ALTER ` khachhang '
  Sửa ' id_khach_hang '  int ( 11 ) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT = 22 ;

-
- Các ràng buộc cho việc đổ bảng
-

-
- Các ràng buộc cho bảng `hoadon`
-
 BẢNG  ALTER ` hoadon '
  ADD CONSTRAINT  ' fk_id_admin '  KEY NƯỚC NGOÀI ( ' id_admin ' ) Tài liệu tham khảo  ' quản trị ' ( ' id_admin ' ),
  ADD CONSTRAINT  ' fk_id_khach_hang '  FOREIGN KEY ( ' id_khach_hang ' ) Tài liệu tham khảo  ' khachhang ' ( ' id_khach_hang ' ),
  ADD CONSTRAINT  ' fk_nicklol '  KEY NƯỚC NGOÀI ( ' id_nicklol ' ) Tài liệu tham khảo  ' acc_lol_chitiet ' ( ' id_nick_lol ' );
CAM KẾT ;

/ * ! 40101 SET CHARACTER_SET_CLIENT = @ OLD_CHARACTER_SET_CLIENT * / ;
/ * ! 40101 SET CHARACTER_SET_RESULTS = @ OLD_CHARACTER_SET_RESULTS * / ;
/ * ! 40101 SET COLLATION_CONNECTION = @ OLD_COLLATION_CONNECTION * / ;
