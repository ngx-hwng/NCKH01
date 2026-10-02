# BẢN THUYẾT MINH Ý TƯỞNG NGHIÊN CỨU KHOA HỌC SINH VIÊN

---

## 1. THÔNG TIN CHUNG VỀ ĐỀ TÀI

* **Tên đề tài tiếng Việt:** Nghiên cứu và phát triển hệ thống phát hiện té ngã bảo vệ quyền riêng tư cho người cao tuổi dựa trên thông tin trạng thái kênh WiFi (WiFi CSI) và mô hình học máy tại biên.
* **Tên đề tài tiếng Anh:** Privacy-Preserving Fall Detection System for the Elderly Using WiFi Channel State Information (CSI) and Edge Machine Learning.
* **Lĩnh vực nghiên cứu:** Xử lý tín hiệu số, Trí tuệ nhân tạo (AI/TinyML), Mạng cảm biến không dây & IoT.
* **Đối tượng thụ hưởng:** Người cao tuổi sống độc thân, trung tâm dưỡng lão, bệnh viện điều trị và gia đình có người lớn tuổi.

---

## 2. TÍNH CẤP THIẾT & ĐẶT VẤN ĐỀ THỰC TIỄN

### 2.1. Bối cảnh xã hội và y tế
* **Té ngã là nguy cơ tử vong và tàn tật hàng đầu:** Theo Tổ chức Y tế Thế giới (WHO), té ngã là nguyên nhân đứng thứ hai gây tử vong do chấn thương không chủ ý ở người cao tuổi. Trên toàn cầu, hơn 32% người từ 65 tuổi trở lên ngã ít nhất 01 lần/năm, trong đó ~18% để lại chấn thương trung bình đến nặng và 26% số vụ ngã xảy ra khi nạn nhân đang ở một mình không có người trợ giúp. Thời gian nằm bất động trên sàn sau té ngã tỷ lệ thuận với tỷ lệ biến chứng nặng và tử vong ("giờ vàng" cấp cứu là dưới 1 giờ).
* **Khu vực nguy hiểm nhất lại là nơi nhạy cảm nhất:** Hơn 80% các ca té ngã xảy ra ở **nhà vệ sinh, phòng tắm và phòng ngủ** — nơi sàn trơn trượt, ánh sáng yếu hoặc khi người già thức dậy vào ban đêm. Đây cũng chính là nơi tuyệt đối không thể lắp camera.

### 2.2. Già hóa dân số Việt Nam: nhu cầu bùng nổ trong 10 năm tới
* **Hiện tại:** Cả nước có khoảng 16,1 triệu người cao tuổi, chiếm trên 16% dân số (Dữ liệu dân cư quốc gia 2025). Tỷ trọng dân số từ 65 tuổi trở lên đã đạt 9,3-9,5% năm 2024-2025 (Tổng cục Thống kê, World Bank).
* **Dự báo:** Đến 2030 có ~18 triệu người từ 60 tuổi trở lên (tăng gần 4 triệu so với 2024). Năm 2034 Việt Nam chính thức bước vào giai đoạn dân số già (tỷ lệ 65+ đạt 14%), năm 2036 kết thúc thời kỳ dân số vàng, năm 2050 bước vào giai đoạn siêu già (65+ trên 21%). Nhóm 80+ cần chăm sóc đặc biệt tăng gần 8 lần trong 50 năm tới.
* **Tốc độ già hóa nhanh nhất châu Á:** Thời gian chuyển từ già hóa sang già chỉ 17-20 năm, ngắn hơn nhiều so với Nhật, châu Âu. Trong khi đó tổng tỷ suất sinh đã giảm xuống 1,91-1,93 con/phụ nữ (dưới mức thay thế), con cái đi làm xa, mô hình ông bà sống một mình ở quê và thành phố ngày càng phổ biến. Gần 4 triệu người cao tuổi đã gặp khó khăn trong sinh hoạt hàng ngày, dự báo lên ~5 triệu vào 2025 và ~8 triệu vào 2039.
* **Chính sách hậu thuẫn:** Quyết định 383/QĐ-TTg (21/02/2025) phê duyệt Chiến lược quốc gia người cao tuổi đến 2035, tầm nhìn 2045, ưu tiên chăm sóc sức khỏe, phục hồi chức năng và trợ giúp xã hội tại cộng đồng và tại nhà.
* $\rightarrow$ Ý nghĩa: nhu cầu giám sát an toàn tại nhà, đặc biệt trong nhà tắm/phòng ngủ, sẽ tăng đột biến trong 5-10 năm tới, đúng thời điểm đề tài hoàn thiện.

### 2.3. Quy mô thị trường thiết bị phát hiện té ngã
* **Thị trường toàn cầu:** Quy mô hệ thống phát hiện té ngã ước đạt ~545 triệu USD năm 2025, dự báo đạt ~843-940 triệu USD vào 2033-2034 (CAGR 4,6-7,8% tùy báo cáo Grand View Research, Insight Partners, Persistence). Thị trường thiết bị đeo phát hiện ngã riêng đã đạt ~1,9 tỷ USD năm 2025, dự báo ~3,7 tỷ USD năm 2035 (CAGR 6,6%).
* **Phân khúc dẫn dắt:** Hệ thống tự động (không cần bấm nút) chiếm ~60-62% thị phần; công nghệ cảm biến chiếm ~43-55%; ứng dụng tại nhà (home care, aging-in-place) chiếm ~50-68% — 77% người cao tuổi muốn ở lại nhà riêng thay vì vào viện. Đây chính là phân khúc đề tài nhắm tới.
* **Xu hướng không tiếp xúc:** Thị trường radar phát hiện ngã tuy mới chỉ ~0,04-0,05 tỷ USD năm 2025-2026 nhưng tăng trưởng nhanh nhất với CAGR ~22,7% đến 2035, trong đó ~58% lắp đặt gắn với y tế và dưỡng lão, ~42% cơ sở chăm sóc người già tại Mỹ đã tích hợp radar. Minh chứng rõ cho dịch chuyển từ đeo tay sang giám sát không tiếp xúc, bảo vệ riêng tư.
* **Đối thủ hiện hữu:** Cảm biến mmWave Aqara FP2 (60-64 GHz, giá ~1,8-2,2 triệu VNĐ, hỗ trợ Apple Home/Google Home, quảng cáo phát hiện ngã bán kính 2m khi gắn trần) đã chứng minh có khách hàng trả tiền cho tính năng này, nhưng vẫn để lại khoảng trống về giá rẻ, chạy offline không phụ thuộc cloud, và tối ưu cho phòng nhỏ kiểu Việt Nam.

### 2.4. Chân dung người thực sự cần dùng (ai trả tiền)
Nhu cầu là thật nhưng không dàn đều. Người dùng và người trả tiền là hai nhóm khác nhau:
1. **Con cái 30-45 tuổi tại đô thị (khách hàng trả tiền chính):** Có bố/mẹ trên 70 tuổi sống một mình, không thể lắp camera trong nhà tắm, ông bà từ chối đeo vòng tay (nghiên cứu thị trường ghi nhận ~22% người già từ chối thiết bị đeo vì vướng víu, quên sạc). Sẵn sàng chi 600.000-900.000 VNĐ thiết bị + ~50.000 VNĐ/tháng phí cảnh báo qua app/gọi điện để mua sự an tâm.
2. **Viện dưỡng lão tư nhân, bệnh viện, trung tâm phục hồi chức năng:** 01 phòng tắm/phòng ngủ = 01 node giám sát, đúng phạm vi 1 người/phòng của đề tài. Nhu cầu giảm trực đêm, có bằng chứng cảnh báo và tuân thủ riêng tư.
3. **Chủ đầu tư chung cư cao cấp / nhà thông minh:** Tích hợp option "smart elder-care" không camera như một tiện ích bán nhà.
* **Mô hình thương mại phù hợp:** Không bán mỗi cục ESP32. Bán gói `thiết bị giá rẻ + dịch vụ cảnh báo` (còi tại chỗ + Telegram/app + gọi điện cho người thân). Tuyên bố rõ như Aqara: "thiết bị hỗ trợ cảnh báo, không phải thiết bị y tế", chấp nhận báo giả thấp và tuyệt đối giảm bỏ sót.

### 2.5. Hạn chế chí mạng của các công nghệ hiện hữu
Khi so sánh sòng phẳng với các giải pháp khác, các công nghệ hiện tại bộc lộ những rào cản rất lớn:
1. **Camera AI:** 
   * *Ưu điểm:* Độ chính xác thị giác cao.
   * *Nhược điểm chí mạng:* **Tuyệt đối không thể lắp đặt trong nhà tắm hay phòng ngủ** do vi phạm nghiêm trọng quyền riêng tư cá nhân và nguy cơ rò rỉ dữ liệu nhạy cảm.
2. **Thiết bị đeo (Smartwatch, vòng tay thông minh):**
   * *Nhược điểm chí mạng:* Phụ thuộc hoàn toàn vào ý thức người dùng (thường quên sạc, tháo ra khi tắm, đi ngủ hoặc cảm thấy vướng víu khó chịu).
3. **Nút bấm khẩn cấp (Panic button):**
   * *Nhược điểm chí mạng:* Hoàn toàn vô dụng nếu nạn nhân bị bất tỉnh, đột quỵ, chấn thương sọ não hoặc không thể với tới nút bấm.
4. **Cảm biến radar bước sóng milimét (mmWave Radar) / Thảm áp lực:**
   * *Nhược điểm:* Thảm áp lực đắt đỏ, khó lắp ráp; Radar mmWave chuyên dụng chi phí cao và dễ bị suy giảm tín hiệu mạnh trong môi trường phòng tắm nhiều hơi nước dày đặc.

$\rightarrow$ **Yêu cầu thực tiễn:** Cần một giải pháp **"không tiếp xúc" (contactless)**, **"bảo vệ tuyệt đối quyền riêng tư" (privacy-preserving)**, hoạt động **liên tục 24/7** với **chi phí triển khai tối thiểu**.

---

## 3. NGUYÊN LÝ KỸ THUẬT CỐT LÕI (CORE PRINCIPLES)

### 3.1. Hiện tượng phản xạ và tán xạ đa đường (Multipath Effect)
Trong một căn phòng, sóng vô tuyến WiFi (dải tần 2.4 GHz hoặc 5 GHz) phát từ nguồn phát (TX) đến nguồn thu (RX) theo nhiều đường phản xạ khác nhau qua tường, sàn, trần và vật thể trong phòng. 
Cơ thể con người chứa hơn 70% nước, là một vật thể phản xạ và tán xạ sóng điện từ rất mạnh. Bất kỳ cử động nào của cơ thể đều làm thay đổi độ dài đường truyền, góc tán xạ và tạo ra độ dịch pha Doppler trên sóng vô tuyến.

### 3.2. Bản chất thông tin trạng thái kênh (Channel State Information - CSI)
Khác với chỉ số cường độ tín hiệu nhận RSSI (Received Signal Strength Indicator) chỉ đo độ mạnh tổng thể ở tầng MAC và rất dễ nhiễu, CSI được trích xuất từ tầng vật lý (PHY) của chuẩn OFDM:

$$H(f, t) = |H(f, t)| e^{j \angle H(f, t)}$$

Trong đó:
* $|H(f, t)|$: Biên độ (Amplitude) của sóng con (*subcarrier*).
* $\angle H(f, t)$: Góc pha (Phase) của sóng con.

Một gói tin WiFi chuẩn 802.11n/ac có từ 52 đến hàng trăm sóng con hoạt động đồng thời. Ma trận CSI cung cấp thông tin đa chiều chi tiết về độ trễ, suy hao và dịch pha của từng sóng con. Khi con người té ngã, sự thay đổi độ cao và gia tốc cơ thể sẽ tạo ra một **dấu vết động học (Dynamic Signature)** rất đặc trưng trên toàn bộ ma trận CSI.

### 3.3. So sánh đặc trưng: Té ngã vs. Hành vi thông thường

| Đặc trưng quan sát | Cú té ngã (Fall) | Hành vi thông thường (Ngồi, Cúi, Nằm) |
| :--- | :--- | :--- |
| **Gia tốc chuyển động** | Cực đại theo phương thẳng đứng hướng xuống | Chậm, đều, có gia tốc kiểm soát |
| **Thời gian biến thiên** | Xảy ra đột ngột trong $0.3\text{s} - 0.8\text{s}$ | Diễn ra tuần tự trong $1.5\text{s} - 3.0\text{s}$ |
| **Trạng thái sau biến cố** | Nằm bất động trên sàn (năng lượng CSI giảm sâu đột ngột) | Vẫn có vi dao động (ngồi thở, đứng dậy ngay) |

---

## 4. KIẾN TRÚC HỆ THỐNG VÀ QUY TRÌNH XỬ LÝ DỮ LIỆU

Hệ thống được thiết kế theo mô hình 4 tầng xử lý liên hoàn:

```
+-------------------+                      +-------------------+
|  WiFi TX Node     | ~~~ Sóng vô tuyến ~~~>  WiFi RX Node     |
| (ESP32-S3 Beacon) |   (Phản xạ cơ thể)   | (ESP32-S3 Sniffer)|
+-------------------+                      +---------+---------+
                                                     | (Raw CSI Stream)
                                                     v
                                  +------------------------------------+
                                  | TẦNG 1: TIỀN XỬ LÝ TÍN HIỆU        |
                                  | - Phase Unwrapping & Sanitization  |
                                  | - Lọc thông dải Butterworth        |
                                  | - Giảm chiều dữ liệu (PCA/Wavelet) |
                                  +------------------+-----------------+
                                                     |
                                                     v
                                  +------------------------------------+
                                  | TẦNG 2: MÔ HÌNH HỌC MÁY NHẬN DẠNG  |
                                  | - Cửa sổ trượt (Sliding Window)    |
                                  | - Trích xuất đặc trưng Time-Freq   |
                                  | - Mô hình: 1D-CNN / Random Forest  |
                                  +------------------+-----------------+
                                                     |
                                                     v
                                  +------------------------------------+
                                  | TẦNG 3: MÁY TRẠNG THÁI CHỐNG BÁO GIẢ|
                                  | - Pha 1: Phát hiện xung rơi tự do  |
                                  | - Pha 2: Xác nhận bất động (> 5s)  |
                                  +------------------+-----------------+
                                                     |
                                                     v
                                  +------------------------------------+
                                  | TẦNG 4: CẢNH BÁO THỜI GIAN THỰC    |
                                  | - Còi hú khẩn cấp tại phòng        |
                                  | - Gửi tin nhắn Telegram / Ứng dụng |
                                  +------------------------------------+
```

### Chi tiết các tầng xử lý:

1. **Thu thập CSI thô (Data Collection):**
   * Sử dụng 2 module ESP32-S3 chạy firmware mã nguồn mở (ESP-CSI).
   * TX phát gói tin ping với tần số ổn định 100 Hz.
   * RX bắt các gói tin, bóc tách mảng subcarriers CSI và chuyển tiếp qua cổng Serial/LAN về máy trạm biên (Raspberry Pi hoặc mini PC).

2. **Tiền xử lý tín hiệu (Signal Preprocessing):**
   * **Hiệu chỉnh pha (Phase Sanitization):** Loại bỏ sai số xung nhịp đồng hồ (CFO - Carrier Frequency Offset và SFO - Sampling Frequency Offset) bằng phương pháp biến đổi tuyến tính góc pha.
   * **Lọc nhiễu dải thông (Bandpass Filtering):** Bộ lọc số Butterworth bậc 4 (tần số cắt $0.1\text{ Hz} - 10\text{ Hz}$) loại bỏ nhiễu rung giật tần số cao và thành phần tĩnh tần số thấp.
   * **Phân tích thành phần chính (PCA):** Chọn lọc 3–5 thành phần chủ yếu (Principal Components) mang tỷ lệ phương sai tín hiệu chuyển động cao nhất.

3. **Mô hình học máy (Machine Learning/Deep Learning):**
   * Dữ liệu được cắt theo cửa sổ trượt $2.5\text{ giây}$ (bước nhảy $0.2\text{ giây}$).
   * Áp dụng mạng **1D-CNN** nhỏ hoặc bộ phân loại **Random Forest/SVM** dựa trên các đặc trưng thống kê miền thời gian (Mean, Variance, Energy, Skewness, Kurtosis) và miền tần số (Wavelet energy).

4. **Máy trạng thái hữu hạn chống báo động giả (Finite State Machine - FSM):**
   * **State 0 (Bình thường):** Hoạt động thường nhật.
   * **State 1 (Nghi vấn):** Phát hiện biến thiên biên độ năng lượng vượt ngưỡng $Th_{fall}$.
   * **State 2 (Xác nhận):** Đếm thời gian nạn nhân nằm im trên sàn. Nếu sau $5\text{ giây}$ không có tín hiệu phục hồi độ cao (không đứng dậy) $\rightarrow$ Kích hoạt báo động té ngã thật sự. Nếu đứng dậy trong vòng $5\text{ giây}$ $\rightarrow$ Hủy sự kiện.

---

## 5. TÍNH KHẢ THI VÀ PHẠM VI NGHIÊN CỨU

### 5.1. Ngân sách phần cứng thực nghiệm
* 02 Bo mạch phát triển **ESP32-S3** (kèm ăng-ten rời): $\approx 350.000\text{ VNĐ}$.
* 01 Trạm xử lý biên (Laptop sẵn có hoặc bo Raspberry Pi): $0\text{ VNĐ}$ (tận dụng thiết bị có sẵn).
* Chi phí mô hình hóa, thiết bị phụ trợ (đệm mút an toàn khi thực nghiệm té ngã): $\approx 300.000\text{ VNĐ}$.
* **Tổng kinh phí dự kiến:** Dưới $1.000.000\text{ VNĐ}$ (hoàn toàn khả thi với nguồn kinh phí sinh viên).

### 5.2. Giới hạn phạm vi đề tài (Scoping)
Để đảm bảo đề tài có tính khoa học sâu sắc, tránh dàn trải và hạn chế nhược điểm đa đường phức tạp:
* **Không gian thử nghiệm:** Giới hạn trong phòng đơn khép kín diện tích từ $9\text{ m}^2$ đến $16\text{ m}^2$ (mô phỏng chính xác kích thước nhà tắm hoặc phòng ngủ tiêu chuẩn).
* **Đối tượng:** Giám sát 01 người duy nhất trong không gian tại một thời điểm (phù hợp tuyệt đối với ngữ cảnh sử dụng nhà vệ sinh/nhà tắm).

---

## 6. ĐÓNG GÓP KHOA HỌC CỦA ĐỀ TÀI (ĐIỂM ĐÁNH GIÁ CỦA HỘI ĐỒNG)

1. **Đóng góp về mặt dữ liệu:** Tự xây dựng bộ dữ liệu WiFi CSI thực nghiệm bao gồm nhiều tình huống vận động đa dạng (Đi lại, Ngồi xuống, Cúi nhặt đồ, Trượt chân ngã ngửa, Khụy gối ngã sấp) trong môi trường phòng khép kín.
2. **Đóng góp về giải thuật:** Đề xuất được chuỗi tiền xử lý tín hiệu CSI nhẹ tối ưu hóa trên phần cứng giá rẻ (ESP32-S3) thay vì phải phụ thuộc vào các card mạng đắt tiền/máy tính cấu hình cao.
3. **Đóng góp về tính ứng dụng:** Hiện thực hóa thành công một sản phẩm nguyên mẫu (prototype) có khả năng phát hiện té ngã với độ trễ dưới $2\text{ giây}$, đảm bảo 100% không ghi nhận hình ảnh/video, bảo vệ tuyệt đối dữ liệu riêng tư cá nhân.

---

## 7. BẢNG PHÂN TÍCH SWOT VÀ CHIẾN LƯỢC TRẢ LỜI PHẢN BIỆN

| Yếu tố | Phân tích thực tế | Chiến lược giải trình & Khắc phục |
| :--- | :--- | :--- |
| **Strengths (Điểm mạnh)** | Không xâm phạm riêng tư; Không cần đeo thiết bị; Phần cứng chi phí cực thấp; Hoạt động trong bóng tối hoặc có sương hơi nước. | Nhấn mạnh đây là giải pháp duy nhất khả thi thay thế camera trong nhà vệ sinh và phòng ngủ. |
| **Weaknesses (Điểm yếu)** | Tín hiệu CSI nhạy cảm với việc xáo trộn đồ đạc nội thất hoặc có người thứ hai cùng vào phòng. | Khống chế phạm vi đề tài vào khu vực riêng tư chỉ có 1 người (nhà tắm); Áp dụng chuẩn hóa tín hiệu thích nghi với môi trường nền. |
| **Opportunities (Cơ hội)** | Thị trường fall detection ~545 triệu USD (2025) lên ~900 triệu USD (2033, CAGR 5-8%), home-care chiếm 50-68%; VN có 16,1 triệu NCT, 2030 lên 18 triệu, 2034 thành XH già; làn sóng Silver Tech + Edge AI/TinyML. | Định vị giá rẻ <1tr vs mmWave ~2tr, chạy offline, đúng ngách nhà tắm 1 người; tiềm năng báo SV, khóa luận, gói thiết bị + phí thuê bao cảnh báo. |
| **Threats (Thách thức)** | Nhiễu tín hiệu từ thú cưng (chó, mèo) hoặc cửa lay động do gió. | Bổ sung ngưỡng lọc năng lượng (vật nuôi có khối lượng nhỏ tạo ra biến thiên biên độ thấp hơn nhiều so với người lớn). |
