# 🐛 DEUTSCHFUNS.COM - BUG REPORT & TESTING PORTFOLIO

## 1. Project Overview
- **Project Name:** Deutschfuns Web Application
- **Role:** Fresher Tester / QA
- **Key Responsibilities:**
  - Designed and executed manual test cases for the German learning platform.
  - Performed UI and end-to-end functional testing for the learning material tree and the German learning chatbox.
  - Developed automated test scripts for the user authentication (login) process using **Playwright**.
  - Conducted API load and stress testing using **JMeter** to evaluate system limits and ensure stability.
  - Logged, tracked, and managed bugs using **Trello**.

---

## 2. Bug Report Log (Sample)

> *Note: Below is a snippet of the most critical bugs (P0 - P2) found during the testing phase. For the full list, please refer to the raw data files.*

| ID | Tiêu đề | Mức độ | Cách thực hiện | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **BUG-001** | Lỗi hiển thị điều kiện người học có thể thi kết thúc khóa | P0 | 1. Truy cập vào bài học có yêu cầu làm bài tập<br>2. Thực hiện làm bài tập<br>3. Hoàn thành đúng hết tất cả các câu hỏi, ở câu cuối thay vì chọn nút qua bài kế tiếp, bấm vào nút hiển thị video hoặc chờ vài giây | Hệ thống vẫn bình thường và người dùng có thể qua bài học kế tiếp | Sau khi bấm xem video hoặc để màn hình chờ vài giây thì hệ thống hiển thị thông báo đủ điều kiện thi dù chưa xem hết tất cả các video | Closed |
| **BUG-002** | Khóa học: Lỗi không tua được video dù đã hoàn thành | P0 | 1. Truy cập vào 1 video đã hoàn thành<br>2. Truy cập vào dev tool và xóa đi phần local storage trong mục application<br>3. load lại trang | Có thể xem lại và tua video tùy ý, ngoài ra còn xuất hiện nút làm bài tập hoặc bài học kế tiếp | sau khi xóa local storage thì video không thể tua được, và cũng không xuất hiện nút làm bài tập hoặc bài học kế tiếp | Open |
| **BUG-003** | Lỗi ghi nhận trạng thái pass của câu hỏi | P0 | | Hệ thống sẽ chuyển trạng thái bài học thành công và không bị mất trạng thái đã hoàn thành bài học | Hệ thống chưa chuyển trạng thái của giá trị “passed” thành “true” nên bài học có làm bài tập vẫn bị hệ thống reset trạng thái về chưa hoàn thành | Open |
| **BUG-004** | Lỗi xử lý Voucher có mức 100% | P0 | 1. Truy cập vào trang học phí và chọn 1 mức giá<br>2. Chọn voucher có mức giảm 100% và tiến hành thanh toán | Trang thanh toán sẽ trừ đúng số tiền mà hệ thống trừ là 0đ hoặc không cho thanh toán và trả message số tiền thanh toán phải lớn hơn 0 | Trang thanh toán đang giữ nguyên mức giá của gói dù đã áp dụng | Open |
| **BUG-005** | Sau khi xem được 4 video thì không thể quay lại video cũ để xem lại | P0 | 1. Xem tuần tự các video 1 -> 4<br>2. Sau khi xem xong video thứ 4 thì quay trở lại màn hình chọn | Người học vẫn xem lại được bài học cũ đã hoàn thành | Không thể xem lại bài học cũ vì bị hệ thống chặn, trả thông báo cần hoàn thành bài học trước đó | Closed |
| **BUG-006** | Lỗi Navigator của chức năng thanh toán (trường hợp hủy thanh toán) | P1 | 1. Truy cập vào trang học phí và chọn 1 mức giá<br>2. Tiến hành thanh toán<br>3. Sau khi hệ thống chuyển hướng đến trang thanh toán thì hủy thanh toán | Hệ thống sẽ chuyển hướng về lại trang web và màn hình hiển thị thông báo thất bại | Hệ thống không được chuyển hướng về lại trang web mà thay vào đó lại bị chuyển hướng sang trang đăng nhập của bên dịch vụ thanh toán | Open |
| **BUG-007** | Server: Chưa setup phần permissions-policy của micro cho hệ thống web | P2 | | User có thể truy cập được micro để ghi âm lại bài nói | Hệ thống chặn hoàn toàn quyền truy cập micro của trình duyệt | Closed |
| **BUG-008** | Lỗi kiểm tra đáp án viết của bài tập dạng viết | P2 | Lỗi này có thể tìm thấy ở câu số 6, 7, 10, 12 và 15 của bài đầu tiên trong chương trình A2.1 | Hệ thống sẽ kiểm tra tính đúng sai của đáp án từ input user | Hệ thống đang trả lỗi: “Có lỗi xảy ra” khi bấm kiểm tra đáp án do lỗi từ API model Claude. | Closed |
| **BUG-009** | Lỗi ghi nhận tiến trình học tại trang chủ | P2 | 1. Đăng nhập vào hệ thống<br>2. Tiến hành học 1 bài học<br>3. quay về trang chủ để kiểm tra tiến độ | Hệ thống sẽ ghi nhận đúng tiến trình của người học dựa trên số lượng bài học đã hoàn thành | Hệ thống chưa ghi nhận bất kỳ sự thay đổi nào trong quá trình học của người học | Open |

---

## 3. Test Environments & Tools
- **Testing Types:** Manual Testing, Automation Testing, API Testing, Performance Testing
- **Tools/Frameworks:** Playwright, JMeter, Trello
- **Browsers:** Google Chrome, Microsoft Edge, Mozilla Firefox

## 4. Contact Information
- **Name:** Nguyen Nhat Huy
- **Email:** huy090603huy@gmail.com
- **GitHub:** [https://github.com/huy090603huy123](https://github.com/huy090603huy123)
