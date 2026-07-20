# Danh Nhân Đất Việt (Viet Nam History Game)

**Danh Nhân Đất Việt** (Vietnam History Game) là một ứng dụng web full-stack toàn diện, được thiết kế theo phương pháp gamification (game hóa) nhằm giúp việc học lịch sử Việt Nam trở nên thú vị, tương tác cao và có tính cạnh tranh lành mạnh. Nền tảng này kết hợp các tài nguyên giáo dục phong phú (Thư viện tri thức, Thẻ ghi nhớ) với nhiều cơ chế trò chơi đa dạng (Đối kháng PvP, Mở rộng bản đồ, Sinh tồn và Giải đố) để khuyến khích người học tiếp thu và ghi nhớ kiến thức lịch sử.

---

## 🌟 Tính năng & Chế độ chơi

### 📚 Học tập
*   **Thư Viện Triều Đại (Timeline/Library):** Tìm hiểu về các triều đại và thời kỳ lịch sử khác nhau thông qua các trang tài liệu chi tiết (hỗ trợ định dạng Markdown).
*   **Thẻ Ghi Nhớ (Flashcards):** Các thẻ ghi nhớ lật tương tác giúp ghi nhớ nhanh các nhân vật lịch sử, mốc thời gian và sự kiện quan trọng.

### 🎮 Chế độ chơi (Game Modes)
1.  **Mở Mang Bờ Cõi (Territory Map):** Chế độ chiến thuật với bản đồ Việt Nam trực quan. Người chơi trả lời các câu hỏi gắn liền với các địa danh lịch sử (ví dụ: Điện Biên Phủ, Bạch Đằng) để chinh phục và mở khóa các vùng lãnh thổ, nhận điểm thưởng XP lớn.
2.  **Thách Đấu (PvP Asynchronous):** Người chơi tự tạo các thử thách gồm 10 câu hỏi và gửi tới đối thủ. Cả hai sẽ chơi cùng một bộ câu hỏi, hệ thống sẽ tự động xác định người chiến thắng dựa trên điểm số và thời gian hoàn thành.
3.  **Sinh Tồn (Survival):** Chế độ thử thách cao độ yêu cầu độ chính xác tuyệt đối. Trả lời sai sẽ bị trừ mạng, trò chơi kết thúc khi số mạng về 0.
4.  **Tốc Chiến (Time Attack):** Chế độ nhịp độ nhanh thử thách phản xạ và khả năng ghi nhớ nhanh dưới áp lực thời gian nghiêm ngặt. Phần thưởng XP cho mỗi câu trả lời đúng sẽ cao hơn.
5.  **Ai Là Triệu Phú (Millionaire):** Chế độ chơi cổ điển với hệ thống 15 câu hỏi có độ khó tăng dần.
6.  **Giải Đố & Logic (Puzzle Modes):**
    *   **Nối Cột (Matching):** Ghép nối các nhân vật lịch sử với triều đại hoặc thành tựu tương ứng của họ.
    *   **Dòng Thời Gian (Chronological):** Kéo thả các sự kiện lịch sử vào đúng thứ tự thời gian xuất hiện.
    *   **Đoán Nhân Vật (Guess Character):** Suy luận ra nhân vật lịch sử dựa trên các manh mối chữ viết và danh hiệu/bí danh.
    *   **Lật Mảnh Ghép (Reveal Picture):** Trả lời các câu hỏi để lật mở từng mảnh ghép của bức tranh lịch sử bị ẩn, sau đó đoán xem bức tranh đó vẽ gì.

### 🏆 Tính năng Game hóa & Phát triển người dùng
*   **Điểm kinh nghiệm (XP):** Nhận XP khi chơi game, trả lời đúng và chiến thắng các trận PvP.
*   **Bảng xếp hạng (Leaderboard):** Cạnh tranh toàn cầu với những người học khác để giành vị trí dẫn đầu dựa trên số XP tích lũy.
*   **Chuỗi ngày học tập (Streaks):** Khuyến khích đăng nhập hàng ngày và duy trì thói quen học tập.
*   **Xác thực tài khoản (Authentication):** Hỗ trợ đăng ký/đăng nhập bằng tài khoản thông thường hoặc đăng nhập nhanh bằng **Google OAuth 2.0 (One-Tap)**.

### 🛠️ Hệ thống quản trị (Admin CMS)
Trang quản trị bảo mật và trực quan (`/admin`) cho phép quản trị viên thực hiện các thao tác CRUD (Thêm, Đọc, Sửa, Xóa) trên:
*   Câu hỏi (Cơ bản, Sinh tồn, Tốc chiến, Triệu phú, Bờ cõi).
*   Bài học, Thư viện tri thức (Wikis) và Thẻ ghi nhớ (Flashcards).
*   Nội dung của tất cả các mini-game (Nối cột, Dòng thời gian, Đoán nhân vật, Lật mảnh ghép).

---

## 💻 Công nghệ sử dụng

**Frontend:**
*   **React.js** (v19)
*   **React Router Dom** để điều hướng trang và thiết lập bảo vệ tuyến đường (Route Guards).
*   **Tailwind CSS** (qua classNames) & CSS tùy chỉnh để thiết kế giao diện responsive và hỗ trợ đổi chủ đề (themes).
*   **@react-oauth/google** phục vụ tính năng đăng nhập qua tài khoản Google.

**Backend:**
*   **Node.js & Express.js**
*   **MongoDB & Mongoose** (v9) giúp thiết lập mô hình dữ liệu linh hoạt.
*   **JSON Web Tokens (JWT)** phục vụ cơ chế xác thực không lưu trạng thái (stateless).
*   **Bcrypt** để mã hóa bảo mật mật khẩu.
*   **Multer** dùng để quản lý việc tải ảnh đại diện lên bộ nhớ local.

---

## 📂 Cấu trúc dự án

```text
History-Game-Web/
├── backend/                  # Server Node.js/Express
│   ├── config/               # Kết nối cơ sở dữ liệu (db.js)
│   ├── controller/           # Logic xử lý game chính và tính điểm XP
│   ├── middleware/           # Middleware xác thực JWT & tải file Multer
│   ├── models/               # MongoDB Schemas (User, Question, Challenge, Matching, v.v.)
│   ├── routes/               # Các tuyến API của Express
│   ├── scripts/              # Tập lệnh nạp dữ liệu mẫu (Seeding) & tạo Admin ban đầu
│   ├── uploads/              # Lưu trữ ảnh đại diện của người dùng cục bộ
│   └── server.js             # File khởi chạy Backend
│
├── frontend/                 # Client React
│   ├── public/               # Tài nguyên tĩnh & index.html
│   └── src/
│       ├── assets/           # Hình ảnh tĩnh (ví dụ: Bản đồ Việt Nam)
│       ├── components/       # Các thành phần giao diện tái sử dụng (Navbar, RouteGuards, Streak, Mạng)
│       ├── config/           # Cấu hình API kết nối (api.js)
│       ├── pages/            # Các trang hiển thị chính (Đăng nhập, Chọn chế độ, Admin, Bảng xếp hạng)
│       └── App.js            # Cấu hình chính của React App & Router
```

---

## 🚀 Cài đặt & Chạy ứng dụng

### Yêu cầu hệ thống
*   Node.js (Khuyên dùng v18 trở lên)
*   MongoDB (Bản cài cục bộ hoặc cụm MongoDB Atlas trên đám mây)

### 1. Cấu hình Backend
Di chuyển vào thư mục backend và cài đặt các thư viện:
```bash
cd backend
npm install
```

Tạo một file `.env` nằm trong thư mục `backend/` với các biến môi trường sau:
```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/history_game   # Hoặc đường dẫn kết nối Atlas của bạn
JWT_SECRET=your_super_secret_jwt_key
GOOGLE_CLIENT_ID=your_google_oauth_client_id
ADMIN_SECRET_CODE=HISTORY_ADMIN_2026               # Mã bảo mật để đăng ký tài khoản admin
```

Chạy server backend ở chế độ phát triển:
```bash
npm run dev
# Server sẽ khởi chạy tại địa chỉ http://localhost:5000
```

*(Tùy chọn)* Khởi tạo các tài khoản admin mặc định:
```bash
node scripts/create_admins.js
```

### 2. Cấu hình Frontend
Di chuyển vào thư mục frontend và cài đặt các thư viện:
```bash
cd frontend
npm install
```

Tạo một file `.env` nằm trong thư mục `frontend/` với nội dung:
```env
REACT_APP_GOOGLE_CLIENT_ID=your_google_oauth_client_id
REACT_APP_API_URL=http://localhost:5000
```

*Lưu ý: Nếu nền tảng triển khai của bạn hỗ trợ biến `GOOGLE_CLIENT_ID`, mã nguồn build frontend trong dự án này sẽ tự động map nó sang `REACT_APP_GOOGLE_CLIENT_ID`.*

Khởi chạy server React ở chế độ phát triển:
```bash
npm start
# Ứng dụng sẽ tự động mở tại http://localhost:3000
```

---

## 🔑 Đăng nhập Admin mặc định

Nếu bạn đã chạy tập lệnh `create_admins.js`, bạn có thể đăng nhập vào bảng quản trị với thông tin sau:
*   **Tên tài khoản (Username):** `admin1` (hoặc `admin2`, `admin3`)
*   **Mật khẩu (Password):** `adminPassword123`

Ngoài ra, bạn cũng có thể đăng ký một tài khoản mới tại trang Đăng ký và điền mã `ADMIN_SECRET_CODE` bạn đã thiết lập vào ô "Mã Admin" để tự động cấp quyền quản trị viên ngay lập tức.

---

## 📜 Bản quyền & Liên hệ

Dự án này được phát triển như một sáng kiến Nghiên Cứu Khoa Học (NCKH) nhằm bảo tồn và quảng bá Lịch sử Việt Nam thông qua ứng dụng công nghệ web hiện đại.
