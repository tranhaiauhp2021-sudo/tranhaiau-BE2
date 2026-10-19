# Web BE - Phần 1 + Phần 2 (Admin Site)

Mở `MyStoreMVC5.sln` bằng **Visual Studio có ASP.NET / .NET Framework 4.8**. Restore NuGet, sau đó chạy script `Database/01_Create_MyStore.sql` trong SQL Server và chỉnh `MyStoreConnection` ở `Web.config` theo tên SQL Server thực tế.

Đây là bản code mẫu dành cho học tập. **EF6 DbContext và entity mapping được viết thủ công để chạy với schema MyStore**, KHÔNG phải file EDMX tự sinh theo DB First trong slide. Nếu giáo viên yêu cầu đúng DB First, chị cần thực hiện bước `Models > Add > New Item > ADO.NET Entity Data Model > EF Designer from Database` trên máy và đồng bộ controller với tên context/model sinh ra.

## Đã bổ sung
- `_AdminLayout.cshtml` với menu.
- Danh mục: danh sách / chi tiết / thêm / sửa / xóa và partial view chung.
- Sản phẩm: CRUD, danh mục từ DB, upload ảnh (giới hạn 3MB và đuôi file), tìm theo từ khóa / khoảng giá, sắp xếp và phân trang; partial views.
- Khách hàng: tìm kiếm, phân trang, xem đơn hàng của khách.
- Đơn hàng: danh sách và chi tiết sản phẩm đã mua.
- Tài khoản admin: tra cứu chỉ đọc, không hiển thị mật khẩu.

## Chưa hoàn thiện
- Chưa có đăng nhập / đăng xuất / phân quyền admin, chưa quản lý CRUD tài khoản; **không đưa website lên Internet**.
- Khách hàng và đơn hàng ở bản này chỉ có chức năng xem.
- Upload chỉ kiểm tra phần mở rộng và dung lượng (chưa kiểm tra nội dung ảnh), do đó chỉ dùng localhost.
- Chưa chạy được IIS Express/SQL Server trong môi trường tạo file; chị cần Build và kiểm tra trong Visual Studio.

## Nộp Git
Sau khi kiểm tra: Git > Create Git Repository (hoặc Git Changes) > Commit All > Push. Không commit mật khẩu / connection strings thật. `.gitignore` bỏ qua bin, obj, .vs.
