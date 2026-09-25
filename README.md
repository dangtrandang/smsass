# smsass (Fossify Messages Extended)

<img alt="Logo" src="graphics/icon.webp" width="120" />

An enhanced fork of [Fossify Messages](https://github.com/FossifyOrg/Messages) featuring a dedicated **Filtered / Spam Tab**, silent keyword & sender filtering, and false-positive recovery.

---

## 🌟 New Features in this Fork (`smsass`)

### 🛡️ Dedicated Filtered / Spam Tab (Tab Tin nhắn đã lọc)
* **Dual-Tab Interface:** Màn hình chính phân tách rõ ràng giữa **[ Hộp thư đến / Inbox ]** và **[ Đã lọc / Filtered ]**.
* **Badge đếm tin chưa đọc:** Tab "Đã lọc" hiển thị số lượng tin nhắn rác/chặn mới nhận được để tiện theo dõi.
* **Chặn trong im lặng (Silent Interception):** Các tin nhắn vi phạm từ khóa hoặc số chặn sẽ được âm thầm đưa vào tab Đã lọc — **hoàn toàn không rung, không chuông, không hiện thông báo popup**.
* **Không bị mất tin quan trọng (Anti-Drop / False Positive Safe):** Khắc phục triệt để nhược điểm drop/vứt bỏ tin nhắn của app gốc. Bạn có thể xem lại tin bất kỳ lúc nào nếu bị lọc nhầm (như mã OTP, biến động số dư ngân hàng).
* **Khôi phục về Hộp thư đến (Restore to Inbox):** 
  * Nút khôi phục ngay trên thanh công cụ khi đọc tin nhắn.
  * Hỗ trợ chọn nhiều tin ngoài danh sách để khôi phục hàng loạt.
* **Cài đặt bật/tắt linh hoạt:** Có công tắc bật/tắt tab lọc trong mục **Cài đặt (Settings)** -> *Bật tab Tin nhắn đã lọc / Spam*.

---

## 📱 Core Features (Tính năng cốt lõi)

* **Stay Connected with Ease:** Gửi nhận SMS/MMS nhanh chóng, hỗ trợ tin nhắn nhóm, hình ảnh, biểu tượng cảm xúc.
* **Block Unwanted Messages:** Chặn số điện thoại, chặn số lạ và lọc từ khóa nội dung linh hoạt.
* **Effortless SMS Backup:** Sao lưu và khôi phục tin nhắn dễ dàng (JSON/XML).
* **Lightweight & Fast:** Dung lượng nhẹ, mượt mà, tối ưu pin.
* **Enhanced Privacy:** Tùy chỉnh hiển thị thông báo trên màn hình khóa.
* **Modern Design:** Giao diện Material Design tự động đổi màu theo theme hệ thống hoặc màu tùy chỉnh.
* **100% Free & Open-Source:** Không quảng cáo, không theo dõi, bảo vệ quyền riêng tư người dùng.

---

## 🛠️ Build & Install

### Build từ mã nguồn
```bash
git clone https://github.com/dangtrandang/smsass.git
cd smsass
./gradlew assembleDebug
```

File APK sẽ được tạo tại:
`app/build/outputs/apk/foss/debug/messages-23-foss-debug.apk`

### Cài đặt qua ADB

**Máy thường:**
```bash
adb install -r app/build/outputs/apk/foss/debug/messages-23-foss-debug.apk
```

**Máy đã Root (bypass hạn chế bảo mật trên Xiaomi/MIUI/HyperOS):**
```bash
adb push app/build/outputs/apk/foss/debug/messages-23-foss-debug.apk /data/local/tmp/messages.apk
adb shell "su -c 'chmod 777 /data/local/tmp/messages.apk && pm install -r -d -g /data/local/tmp/messages.apk'"
```

---

## 📜 Giấy phép (License)
Dự án được phân phối dưới giấy phép **GNU General Public License v3.0 (GPLv3)**.  
Dựa trên nền tảng của [Fossify Messages](https://github.com/FossifyOrg/Messages) và [Simple SMS Messenger](https://github.com/SimpleMobileTools/Simple-SMS-Messenger).
