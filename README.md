# GPA Calculator Pro

Ứng dụng tính GPA đa học kỳ với Goal Seeking - chạy offline hoàn toàn.

## 🚀 Cách chạy

Chỉ cần mở file `index.html` trong trình duyệt web (Chrome, Firefox, Edge...).

**Không cần cài đặt gì thêm!**

## ✨ Tính năng

### 📚 Quản lý học kỳ
- Thêm / đổi tên / xóa / nhân bản học kỳ
- Tick chọn học kỳ để đưa vào GPA tích lũy

### 📝 Quản lý môn học
- Nhập điểm 4 thành phần: BTL, Quiz, Giữa kỳ, Cuối kỳ
- Tùy chỉnh trọng số % cho từng thành phần
- Template trọng số sẵn có (20/10/30/40, 0/10/30/60...)

### 📊 Tính GPA
- GPA thang 10 và thang 4
- GPA học kỳ và GPA tích lũy
- 2 chế độ: STRICT (tổng %=100) và AUTO-NORMALIZE

### 🎯 Goal Seeking
- Tính GPA học kỳ cần để đạt mục tiêu GPA tích lũy
- Tính điểm thành phần cần để đạt điểm môn mong muốn

### 💾 Lưu trữ
- Tự động lưu vào LocalStorage
- Export/Import file JSON
- Dark Mode

## 📐 Công thức tính

**Điểm môn (STRICT):**
```
score = (BTL×%BTL + Quiz×%Quiz + GK×%GK + CK×%CK) / 100
```

**Điểm môn (AUTO-NORMALIZE):**
```
score = (BTL×%BTL + Quiz×%Quiz + GK×%GK + CK×%CK) / sumW
(sumW = %BTL + %Quiz + %GK + %CK)
```

**GPA học kỳ:**
```
GPA = Σ(score × tín chỉ) / Σ(tín chỉ)
```

**Quy đổi GPA 4 (mặc định):**
| Thang 10 | Xếp loại | GPA 4 |
|----------|----------|-------|
| 8.5-10.0 | A | 4.0 |
| 7.0-8.49 | B | 3.0 |
| 5.5-6.99 | C | 2.0 |
| 4.0-5.49 | D | 1.0 |
| < 4.0 | F | 0.0 |

## 🧪 Chạy Tests

Nhấn nút 🧪 ở góc trên bên phải để chạy tất cả test vectors:
- TV1: STRICT course score = 7.0
- TV2: Semester GPA = 7.8
- TV3: AUTO-NORMALIZE = 6.75
- TV4: Goal seek CK = 8.67
- TV5: Required semester GPA = 8.4

## ⌨️ Phím tắt

- `Tab`: Di chuyển giữa các ô nhập
- `Enter`: Xác nhận giá trị

## 📱 Tương thích

- ✅ Chrome, Firefox, Edge, Safari
- ✅ Desktop và Mobile (responsive)
- ✅ Chạy offline
