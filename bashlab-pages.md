# BashLab — Danh sách trang và chức năng

Cập nhật: 12/09/2026.

Tài liệu tổng hợp **17 trang hiện có trên Stitch**, thuộc dự án `Markdown Requirements Analyzer` (`16169667383747869366`). STT được đánh liên tục từ 01–17; mã Screen giữ nguyên để đối chiếu với thiết kế và ảnh đã xuất.

Phạm vi: mô tả chức năng thể hiện trong bản thiết kế và HTML xuất từ Stitch, không xác nhận backend đã triển khai. Giữ nguyên bộ chức năng hiện tại.

## Phân nhóm chức năng

| Nhóm | Mục đích | STT trang | Screen Stitch |
| --- | --- | --- | --- |
| A — Giới thiệu sản phẩm | Giới thiệu BashLab và dẫn vào khóa học | 01 | 01 |
| B — Xác thực tài khoản | Đăng nhập, đăng ký, xác minh email và khôi phục mật khẩu | 02–06 | 02–06 |
| C — Khám phá khóa học | Duyệt khóa học, xem giáo trình và tiến độ trong từng khóa | 07–08 | 07–08 |
| D — Học tập và thực hành | Theo dõi học tập cá nhân, tiếp tục bài và thực hành Bash | 09–10 | 09–10 |
| E — Tài khoản cá nhân | Xem thông tin tài khoản, yêu cầu đổi mật khẩu và đăng xuất | 11 | 12 |
| F — Quản trị nội dung | Quản lý khóa học, chương và soạn bài học | 12–13 | 14, 16 |
| G — Quản trị vận hành | Quản lý người dùng, phiên thực hành và nhật ký quản trị | 14–15 | 17–18 |
| H — Trang hệ thống | Thông báo truy cập không đủ quyền hoặc trang không tồn tại | 16–17 | 20–21 |

Các nhóm dùng để tổ chức tài liệu, không tạo thêm trang hay chức năng. Nhóm F và G dành cho quản trị viên; nhóm H dùng chung theo tình huống truy cập.

## Danh mục

| STT | Screen Stitch | Trang | Vai trò chính |
| --- | --- | --- | --- |
| 01 | 01 | Landing | Giới thiệu sản phẩm, thử lệnh mô phỏng, khám phá khóa học |
| 02 | 02 | Login | Đăng nhập tài khoản |
| 03 | 03 | Register | Tạo tài khoản |
| 04 | 04 | Verify Email | Xác minh địa chỉ email |
| 05 | 05 | Forgot Password | Yêu cầu liên kết đặt lại mật khẩu |
| 06 | 06 | Reset Password | Đặt mật khẩu mới từ liên kết xác thực |
| 07 | 07 | Course Catalog | Duyệt danh sách khóa học |
| 08 | 08 | Course Overview | Xem nội dung, tiến độ và mở bài học |
| 09 | 09 | My Learning | Xem tổng quan học tập cá nhân và tiếp tục học |
| 10 | 10 | Interactive Lesson Workspace | Đọc bài, thực hành Bash và kiểm tra kết quả |
| 11 | 12 | Account | Xem thông tin tài khoản và quản lý truy cập |
| 12 | 14 | Content | Quản lý cấu trúc khóa học, chương và bài |
| 13 | 16 | Lesson Editor | Soạn nội dung, mục tiêu và mẫu kiểm tra bài tập |
| 14 | 17 | Users | Quản lý vai trò và trạng thái người dùng |
| 15 | 18 | Activity | Theo dõi phiên thực hành và nhật ký quản trị |
| 16 | 20 | Access Denied | Thông báo không đủ quyền truy cập |
| 17 | 21 | Page Not Found | Thông báo không tìm thấy trang |

## Nhóm A — Giới thiệu sản phẩm

### 01. Landing — Trang chủ

**Screen:** `01_Landing_Desktop` · **Đối tượng:** khách truy cập.

- Giới thiệu BashLab và cách học Bash qua hướng dẫn, thực hành và phản hồi.
- Cho thử các lệnh `pwd`, `ls`, `whoami`, `help` trong demo mô phỏng; có thao tác chạy lệnh và xóa đầu ra.
- Giới thiệu khóa Shell 101, các chương và nội dung cơ bản.
- Dẫn đến danh sách khóa học, chi tiết khóa học và đăng nhập.
- Hiển thị câu hỏi thường gặp về cài đặt, lưu tiến độ và vòng đời phiên thực hành.

Demo tại Landing không phải phiên Bash thật. Không gian thực hành chính nằm ở Screen 10.

[Ảnh trang chủ](exports/stitch-2026-09-12/images/01_Landing_Desktop.png)

## Nhóm B — Xác thực tài khoản

### 02. Login — Đăng nhập

**Screen:** `02_Login_Desktop` · **Đối tượng:** người đã có tài khoản.

- Nhập email và mật khẩu để đăng nhập.
- Bật/tắt hiển thị mật khẩu và chọn ghi nhớ thiết bị.
- Hiển thị trạng thái đang xử lý và lỗi thông tin đăng nhập không hợp lệ.
- Chuyển đến đăng ký hoặc quên mật khẩu.

[Ảnh đăng nhập](exports/stitch-2026-09-12/images/02_Login_Desktop.png)

### 03. Register — Đăng ký

**Screen:** `03_Register_Desktop` · **Đối tượng:** người dùng mới.

- Nhập email, mật khẩu và xác nhận mật khẩu.
- Hiển thị yêu cầu mật khẩu; kiểm tra email, độ dài mật khẩu và hai mật khẩu có khớp nhau hay không.
- Gửi yêu cầu tạo tài khoản; thể hiện trạng thái nhập liệu, đang gửi và lỗi từng trường.
- Có liên kết quay về đăng nhập.

[Ảnh đăng ký](exports/stitch-2026-09-12/images/03_Register_Desktop.png)

### 04. Verify Email — Xác minh email

**Screen:** `04_VerifyEmail_Desktop` · **Đối tượng:** người cần xác minh email.

- Hiển thị địa chỉ email nhận liên kết và hướng dẫn kiểm tra hộp thư.
- Cho gửi lại email xác minh, có thời gian chờ giữa các lần gửi.
- Hiển thị xác minh thành công và hành động tiếp tục đến khóa học.
- Hiển thị liên kết không hợp lệ hoặc hết hạn, cho yêu cầu liên kết mới.
- Có lối quay lại đăng nhập.

[Ảnh xác minh email](exports/stitch-2026-09-12/images/04_VerifyEmail_Desktop.png)

### 05. Forgot Password — Quên mật khẩu

**Screen:** `05_ForgotPassword_Desktop` · **Đối tượng:** người không nhớ mật khẩu.

- Nhập email để yêu cầu liên kết đặt lại mật khẩu.
- Hiển thị trạng thái đang gửi và thông báo kiểm tra hộp thư.
- Dùng thông báo trung lập: nếu tài khoản tồn tại thì hướng dẫn sẽ được gửi.
- Cho gửi lại email hoặc thử lại khi có lỗi kết nối.
- Có lối trở về biểu mẫu và đăng nhập.

[Ảnh quên mật khẩu](exports/stitch-2026-09-12/images/05_ForgotPassword_Desktop.png)

### 06. Reset Password — Đặt lại mật khẩu

**Screen:** `06_ResetPassword_Desktop` · **Đối tượng:** người mở liên kết đặt lại mật khẩu.

- Nhập mật khẩu mới và xác nhận mật khẩu.
- Bật/tắt hiển thị mật khẩu; hiển thị yêu cầu mật khẩu và trạng thái khớp nhau.
- Gửi yêu cầu cập nhật mật khẩu, hiển thị trạng thái đang xử lý và thành công.
- Chuyển về đăng nhập sau khi cập nhật thành công.
- Khi liên kết hết hạn hoặc không hợp lệ, cho yêu cầu liên kết mới.

[Ảnh đặt lại mật khẩu](exports/stitch-2026-09-12/images/06_ResetPassword_Desktop.png)

## Nhóm C — Khám phá khóa học

### 07. Course Catalog — Danh sách khóa học

**Screen:** `07_CourseCatalog_Desktop` · **Đối tượng:** người khám phá khóa học; bản xuất minh họa người đã đăng nhập.

- Hiển thị các khóa học cùng cấp độ, mô tả, số chương, số bài và thời lượng ước tính.
- Lọc danh sách theo nhóm `All`, `Core Tracks`, `Security`.
- Hiển thị tiến độ khóa đang học hoặc trạng thái chưa bắt đầu.
- Phân biệt khóa sẵn có với khóa sắp ra mắt.
- Mở tổng quan khóa học hoặc bản xem trước tương ứng.
- Truy cập My Learning, tài khoản và đăng xuất qua điều hướng.

Trang này không có terminal thực hành.

[Ảnh danh sách khóa học](exports/stitch-2026-09-12/images/07_CourseCatalog_Desktop.png)

### 08. Course Overview — Tổng quan khóa học

**Screen:** `08_CourseOverview_Desktop` · **Đối tượng:** người tìm hiểu hoặc đang học một khóa.

- Hiển thị giới thiệu, cấp độ, thời lượng, kết quả học tập và yêu cầu đầu vào.
- Hiển thị tiến độ theo số bài hoàn thành và phần trăm.
- Có nút tiếp tục bài học và thông tin bài tiếp theo.
- Trình bày giáo trình theo chương, hỗ trợ mở/thu gọn danh sách bài.
- Phân biệt chương/bài đã hoàn thành, đang học và đang khóa.
- Mở bài học tương ứng trong Workspace.

Trang này không có terminal thực hành.

[Ảnh tổng quan khóa học](exports/stitch-2026-09-12/images/08_CourseOverview_Desktop.png)

## Nhóm D — Học tập và thực hành

### 09. My Learning — Tổng quan học tập cá nhân

**Screen:** `09_MyLearning_Desktop` · **Đối tượng:** người học đã đăng nhập.

- Hiển thị tổng quan tiến độ và bài học đang tiếp tục.
- Có hành động tiếp tục bài học hiện tại.
- Hiển thị thời gian học, chuỗi phiên thực hành và số lệnh đã thực hiện.
- Tổng hợp mức độ hoàn thành các nhóm kỹ năng lệnh.
- Hiển thị biểu đồ hoạt động và các mục tiêu gần đây đã hoàn thành.

**Ghi chú đối chiếu:** trang này vẫn có trên Stitch và trong bộ ảnh hiện tại. Tài liệu prompt trước đó ghi nhận đã loại dashboard 09 và gộp My Learning vào Screen 08. Tài liệu này ghi lại đúng bản Stitch hiện có, không tự xóa hoặc gộp trang.

[Ảnh My Learning](exports/stitch-2026-09-12/images/09_MyLearning_Desktop.png)

### 10. Interactive Lesson Workspace — Không gian học và thực hành

**Screen:** `10_InteractiveLessonWorkspace_Desktop` · **Đối tượng:** người học đang thực hiện một bài.

- Điều hướng theo khóa học, chương, bài; chuyển bài trước/sau và xem giáo trình.
- Đọc phần giải thích, cú pháp lệnh và sao chép ví dụ.
- Theo dõi danh sách mục tiêu cùng trạng thái hoàn thành từng mục.
- Mở gợi ý khi cần hỗ trợ.
- Nhập lệnh và xem đầu ra trong khu vực terminal; có thao tác xóa đầu ra, sao chép và lệnh nhanh.
- Hiển thị trạng thái sandbox.
- Gửi kiểm tra kết quả bằng `Check Solution` hoặc `Ctrl+Enter` và xem phản hồi hoàn thành.

Thiết kế dành cho thực hành Bash thật trong sandbox; ảnh và HTML mẫu không chứng minh môi trường thực thi đã được kết nối.

[Ảnh không gian thực hành](exports/stitch-2026-09-12/images/10_InteractiveLessonWorkspace_Desktop.png)

## Nhóm E — Tài khoản cá nhân

### 11. Account — Tài khoản

**Screen:** `12_Account_Desktop` · **Đối tượng:** người dùng đã đăng nhập.

- Xem thông tin tài khoản, email, trạng thái xác minh và mã người dùng.
- Xem vai trò hiện tại ở chế độ chỉ đọc.
- Yêu cầu gửi email đặt lại mật khẩu và xem trạng thái đã gửi.
- Đăng xuất khỏi phiên hiện tại.

[Ảnh tài khoản](exports/stitch-2026-09-12/images/12_Account_Desktop.png)

## Nhóm F — Quản trị nội dung

### 12. Content — Quản lý nội dung

**Screen:** `14_Content_Desktop` · **Đối tượng:** quản trị viên.

- Xem cây khóa học → chương → bài học.
- Thêm khóa học, chỉnh sửa thông tin khóa học và thay đổi trạng thái nháp/xuất bản/ẩn.
- Thêm chương, đổi tên và sắp xếp thứ tự chương.
- Thêm bài, sắp xếp thứ tự bài và mở Lesson Editor để chỉnh sửa.
- Hiển thị trạng thái xuất bản của từng bài.
- Sửa tiêu đề, slug và mô tả khóa học bằng form tại chỗ; lưu/hủy và cảnh báo thay đổi chưa lưu.

[Ảnh quản lý nội dung](exports/stitch-2026-09-12/images/14_Content_Desktop.png)

### 13. Lesson Editor — Soạn bài học

**Screen:** `16_LessonEditor_Desktop` · **Đối tượng:** quản trị viên.

- Chỉnh sửa tiêu đề, chương chứa bài, thứ tự bài và slug.
- Chọn trạng thái nháp hoặc xuất bản.
- Soạn nội dung Markdown, dùng công cụ định dạng và xem trước nội dung.
- Thêm, sửa và xóa mục tiêu bài học.
- Chọn mẫu kiểm tra bài tập có sẵn, gồm mẫu thao tác tệp/thư mục và các nhóm bài tập khác.
- Xem trạng thái lưu, lưu thay đổi, hủy hoặc quay lại Content.

[Ảnh soạn bài học](exports/stitch-2026-09-12/images/16_LessonEditor_Desktop.png)

## Nhóm G — Quản trị vận hành

### 14. Users — Quản lý người dùng

**Screen:** `17_Users_Desktop` · **Đối tượng:** quản trị viên.

- Xem danh sách tài khoản, email, vai trò, trạng thái hoạt động và xác minh email.
- Tìm tài khoản và chuyển trang danh sách.
- Đổi vai trò giữa Learner và Admin qua hộp thoại xác nhận.
- Khóa hoặc mở khóa tài khoản qua thao tác xác nhận.
- Nhập lý do thay đổi vai trò/trạng thái để ghi vào nhật ký quản trị.
- Thể hiện quy tắc bảo vệ quản trị viên hoạt động cuối cùng.

[Ảnh quản lý người dùng](exports/stitch-2026-09-12/images/17_Users_Desktop.png)

### 15. Activity — Phiên thực hành và nhật ký quản trị

**Screen:** `18_Activity_Desktop` · **Đối tượng:** quản trị viên.

#### Tab Sessions

- Hiển thị số phiên, sức chứa và trạng thái sử dụng.
- Xem người học, bài đang thực hành, trạng thái phiên và thời điểm hoạt động gần nhất.
- Làm mới dữ liệu và chuyển trang danh sách.
- Dừng phiên bằng hộp thoại xác nhận có lý do bắt buộc.
- Hiển thị trạng thái đang dừng, đã dừng và thông báo kết quả.

#### Tab Admin log

- Xem thời gian, người thực hiện, hành động, đối tượng và kết quả.
- Lọc theo hành động và chuyển trang nhật ký.
- Mở chi tiết để xem lý do và thông tin liên quan đến sự kiện.

Hai tab nằm trong cùng một trang Activity.

[Ảnh hoạt động](exports/stitch-2026-09-12/images/18_Activity_Desktop.png)

## Nhóm H — Trang hệ thống

### 16. Access Denied — Không đủ quyền

**Screen:** `20_AccessDenied_Desktop` · **Đối tượng:** người truy cập tài nguyên không được phép.

- Hiển thị mã `403`.
- Thông báo người dùng không có quyền truy cập trang.

Bản xuất hiện tại chỉ thể hiện thông báo, chưa có nút quay lại hoặc điều hướng khác.

[Ảnh không đủ quyền](exports/stitch-2026-09-12/images/20_AccessDenied_Desktop.png)

### 17. Page Not Found — Không tìm thấy trang

**Screen:** `21_PageNotFound_Desktop` · **Đối tượng:** người truy cập địa chỉ không tồn tại.

- Hiển thị mã `404`.
- Thông báo không tìm thấy trang được yêu cầu.

Bản xuất hiện tại chỉ thể hiện thông báo, chưa có nút quay lại hoặc điều hướng khác.

[Ảnh không tìm thấy trang](exports/stitch-2026-09-12/images/21_PageNotFound_Desktop.png)

## Luồng sử dụng chính

- **Khám phá và học:** Landing → Course Catalog → Course Overview → xác thực khi cần → Lesson Workspace.
- **Tạo tài khoản:** Register → Verify Email → truy cập khóa học.
- **Khôi phục truy cập:** Login → Forgot Password → liên kết trong email → Reset Password → Login.
- **Tiếp tục học theo bản Stitch:** My Learning hoặc Course Overview → Lesson Workspace.
- **Quản lý nội dung:** Content → Lesson Editor → lưu → Content.
- **Vận hành:** Users để quản lý tài khoản; Activity để xử lý phiên và xem nhật ký.

## Ghi chú đồng bộ thiết kế

- **Số trang:** bản Stitch hiện có 17 trang, trong khi README prompt cũ ghi 16 trang do đã loại Screen 09. Các mã 11, 13, 15, 19 không có trang riêng trong bộ ảnh này.
- **Nội dung bài học:** tên/nội dung một số bài giữa Course Overview, Workspace và Lesson Editor chưa trùng nhau. Ví dụ Workspace dùng `practice/notes.txt`, còn Lesson Editor minh họa `projects/main.sh`.
- **Dữ liệu minh họa:** Users hiển thị hai admin hoạt động nhưng đồng thời có nhãn “last active admin”; thời gian thu hồi phiên trên Landing và nhật ký Activity cũng chưa thống nhất. Đây là các điểm dữ liệu mẫu cần đối chiếu, không phải chức năng mới.
- **Nhãn kỹ thuật:** các chuỗi như thông tin cluster, MFA, nhánh/revision hoặc chữ ký trong màn hình mẫu không được xem là bằng chứng hệ thống đã hỗ trợ những chức năng đó.
- **Giới hạn kiểm tra:** tài liệu này mô tả bản thiết kế; chưa kiểm thử đăng nhập, gửi email, phân quyền, lưu dữ liệu hoặc chạy Bash trên backend.

## Nguồn đối chiếu

- [Manifest xuất từ Stitch](exports/stitch-2026-09-12/manifest.json).
- [Bộ 17 ảnh gốc](exports/stitch-2026-09-12/BashLab-Stitch-17-screens.zip).
- [Danh mục prompt trước đó](stitch-prompts/README.md).
