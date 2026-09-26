# Kiểm kê thành phần bên thứ ba

Kho này gọn về mặt bên thứ ba: **ba mục**. Hai mục đầu là mã và bộ chữ, đều
theo giấy phép cho phép dùng lại, đều dùng **nguyên bản, không sửa một ký tự**,
và đều kèm toàn văn giấy phép ngay trong kho. Mục thứ ba là **một bản thu do
máy sinh**, khác hẳn hai mục kia về bản chất nên ghi riêng ở mục 3.

Đo trên tệp `index.html`, ngày 26/09/2026:

| | |
| --- | --- |
| `<script src>` / `<link href>` trỏ ra **ngoài kho** | **0** |
| Lời gọi mạng lúc chạy (`fetch`, `XMLHttpRequest`, `WebSocket`) | **0** |
| Mã phân tích lượt truy cập, quảng cáo, cookie bên thứ ba | **0** |

Đo bằng Chromium: sau khi trang nạp xong, **không một yêu cầu nào ra khỏi
máy khách**. Tệp nhạc ở mục 3 khai `preload="none"` nên nó **không** được tải
lúc nạp trang — đã đo: 0 yêu cầu `.mp3`. Khách bấm nút phát thì trình duyệt
mới tải tệp ấy, và tải **từ chính kho này**, không từ máy chủ của ai khác.

---

## 1. three.js r128

| | |
| --- | --- |
| Đường dẫn | `assets/vendor/three-r128.min.js` |
| Nguồn | <https://github.com/mrdoob/three.js> |
| Giấy phép | MIT — Copyright © 2010–2021 three.js authors |
| Toàn văn giấy phép | `assets/vendor/three-LICENSE.txt` |
| Đã sửa? | **Không.** Nguyên bản phát hành. |

Chép trong kho chứ không nạp từ CDN. Lý do là chủ ý, không phải tiện tay:
một thẻ `<script src="https://cdnjs…">` gửi địa chỉ IP của mọi khách ghé sang
máy chủ của bên thứ ba trước khi trang kịp vẽ khung hình đầu tiên. Trang này
không có máy chủ, không đặt cookie, không có gì để bên nào cần biết.

## 2. Hai bộ chữ

### Be Vietnam Pro

| | |
| --- | --- |
| Tác giả | Be Type (Việt Nam) — Copyright 2021 The Be Vietnam Pro Project Authors |
| Nguồn | <https://github.com/bettergui/BeVietnamPro>, lấy qua kho `google/fonts` (`ofl/bevietnampro`) |
| Trong kho | `assets/fonts/bevietnampro-{400,500,600,700}-vn.woff2` |
| Giấy phép | SIL Open Font Licence 1.1 — toàn văn ở `assets/fonts/OFL-BeVietnamPro.txt` |

### Baloo 2

| | |
| --- | --- |
| Tác giả | Ek Type (Ấn Độ) — Copyright 2019 The Baloo 2 Project Authors |
| Nguồn | <https://github.com/EkType/Baloo2>, lấy qua kho `google/fonts` (`ofl/baloo2`) |
| Trong kho | `assets/fonts/baloo2-vn.woff2` (phông biến thiên, trục `wght` 500–800) |
| Giấy phép | SIL Open Font Licence 1.1 — toàn văn ở `assets/fonts/OFL-Baloo2.txt` |

**Đã sửa? Có — chỉ cắt bớt bảng mã.** Cắt xuống dải Latin + Latin mở rộng +
tiếng Việt, giữ nguyên bảng `mark`/`mkmk` để dấu tiếng Việt vẫn chồng đúng chỗ.
Không đụng tới hình chữ. OFL cho phép sửa và phát hành lại; điều kiện duy nhất
là không dùng lại Tên Dành Riêng, và kho này không đổi tên bộ chữ.

Cả năm tệp cộng lại 200 KB. Cũng tự chứa vì đúng lý do nêu ở mục 1 — không gọi
`fonts.googleapis.com`.

---

## 3. Bản thu «Returning to Shore» — do máy sinh

`assets/audio/returning-to-shore.mp3` — 7,4 MB, 5:49. Bài nhạc đặt trên máy hát
ở bàn nhân vật Minh, «người giữ bến nhạc»; khách bấm mới phát, trang không tự
kêu.

**Lời là của tác giả. Bản thu thì không.** Chính tệp mp3 tự khai điều ấy: thẻ
ghi chú `COMM` trong phần ID3v2 của tệp ghi «made with suno» kèm mốc thời gian
sinh. Tức bản ghi âm do dịch vụ Suno sinh ra, theo điều khoản của Suno, **không
theo `LICENSE` của kho này**. Phần bảo lưu mọi quyền trong `LICENSE` áp cho lời
bài hát và cho phần dựng cảnh, không áp cho bản thu.

Ghi rõ ở đây vì đây là kho mang DOI, và vì hai thứ ấy khác chủ. Nếu sau này có
đăng ký quyền tác giả cho phần nhạc thì thứ đăng ký được là **lời**, không phải
bản thu.

Trang cũng nói thẳng điều này với khách: hỏi Minh «Bài đang có trên máy là bài
gì?» thì câu trả lời viết sẵn nêu đúng chuyện «made with suno». Không giấu
trong tệp kiểm kê.

Bản đầy đủ của bài — lời từng đoạn và ghi chú dàn dựng — nằm ở trang Âm nhạc
của kho `thuyhuongctu/Je-mappelle-Huong`, và mục tương ứng ở `THIRD-PARTY.md`
của kho ấy là mục **4c**.

---

## 4. Những thứ **không** có trong kho này

Mục này ghi ra để hồ sơ sở hữu trí tuệ khỏi phải đi đo lại.

**Không có gì lấy từ kho `thuyhuongctu/BizOn`.** Kho ấy là tài sản **đồng sở
hữu** — `LICENSE` của nó ghi «Bản quyền © 2026 Đỗ Thùy Hương *và Phan Anh Tú*»
và liệt kê «Tạo hình các nhân vật: Lumina…, Đội Demo 5 thành viên» trong phạm
vi bảo hộ. Ba thứ đã cân nhắc rồi **cố ý không lấy**:

1. **Tranh sáu nhân vật đã cắt nền.** Năm nhân vật ở đây là Mai, Linh, Tùng,
   An, Minh — nhân vật của cảnh «Trang viên tri thức» trong kho
   `thuyhuongctu/Je-mappelle-Huong`, tác phẩm một tác giả.
2. **Tên năm nhân vật đội demo** (Minh Long, Thu Hà, Lan Chi, Bảo Ngọc, Gia
   Hân). Đã thay hẳn.
3. **Bảng số liệu bảy thị trường của BizOn Go Global.** Bảng thang phương thức
   thâm nhập ở đây là **kiến thức giáo trình phổ thông** — Uppsala, chi phí
   giao dịch, lý thuyết đại diện, khung CAGE, quan điểm dựa trên nguồn lực,
   born-global, mô hình OLI. Cách trình bày là của tác giả; bản thân các lý
   thuyết thì không ai độc quyền.

**Không có mã do trình sinh mã của một hãng AI để lại.** Tác phẩm ban đầu có
một bản nháp do máy sinh; bản ấy **đã bỏ hẳn, dựng lại từ đầu**, và ba thứ
trong bản nháp bị loại bỏ chứ không phải sửa cho gọn: một lời gọi API của hãng
AI ngay trong trình duyệt khách, three.js nạp từ cdnjs, và tên của những người
có thật. Lịch sử đầy đủ ở kho gốc, `THIRD-PARTY.md` mục 4b.

**Không có ảnh, nhạc hay video của bên thứ ba.** Kho này không chứa tệp âm
thanh hay phim nào.
