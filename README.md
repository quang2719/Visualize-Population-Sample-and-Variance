# Visualize Population, Sample and Variance

## 📊 Giới thiệu

Trang web này được tạo ra nhằm minh họa và giải thích một trong những vấn đề cốt lõi trong thống kê: **tại sao trong công thức tính phương sai mẫu, chúng ta lại chia cho (n-1) thay vì n?**

## 🎯 Mục đích

Dự án này cung cấp một trải nghiệm trực quan và tương tác để hiểu:

- Sự khác biệt giữa **tổng thể (population)** và **mẫu (sample)**
- Khái niệm **ước lượng không chệch** trong thống kê
- Lý do toán học đằng sau việc sử dụng **bậc tự do (n-1)** trong công thức phương sai mẫu
- Tác động của việc sử dụng trung bình mẫu thay vì trung bình tổng thể

## 🔬 Bối cảnh thống kê

### Vấn đề cơ bản

Trong thống kê ứng dụng, chúng ta thường gặp tình huống:
- **Tổng thể**: Toàn bộ đối tượng nghiên cứu (ví dụ: 200,000 con chuột trong phòng thí nghiệm)
- **Mẫu**: Một tập con được chọn từ tổng thể (ví dụ: 5 con chuột được chọn ngẫu nhiên)

### Thách thức trong ước lượng

Khi tính phương sai từ mẫu để ước lượng phương sai tổng thể, việc sử dụng công thức đơn giản:

```
Phương sai = (1/n) × Σ(xi - x̄)²
```

sẽ tạo ra **ước lượng chệch** - có xu hướng ước lượng thấp hơn giá trị thực.

### Giải pháp: Hiệu chỉnh Bessel

Công thức đúng để có ước lượng không chệch:

```
s² = (1/(n-1)) × Σ(xi - x̄)²
```

Việc chia cho (n-1) thay vì n được gọi là **hiệu chỉnh Bessel**.

## 🧮 Nguyên lý toán học

### Bậc tự do (Degrees of Freedom)

- Trong mẫu n quan sát, ban đầu có n giá trị độc lập
- Khi tính trung bình mẫu x̄, ta tạo ra một ràng buộc
- Chỉ còn lại (n-1) thông tin độc lập về sự biến thiên
- Do đó, phải chia cho (n-1) để có ước lượng chính xác

### Tính chất tối ưu của trung bình mẫu

Trung bình mẫu x̄ có tính chất đặc biệt:
- Là giá trị tối thiểu hóa tổng bình phương độ lệch: `Σ(xi - z)²`
- Do đó: `Σ(xi - x̄)² ≤ Σ(xi - μ)²`
- Điều này dẫn đến xu hướng ước lượng thấp nếu không hiệu chỉnh

## 💡 Ý nghĩa của trang web

Trang web này giúp người dùng:

1. **Trực quan hóa** sự khác biệt giữa tổng thể và mẫu
2. **Thực nghiệm** với các kích thước mẫu khác nhau
3. **So sánh** kết quả của công thức chia cho n và n-1
4. **Hiểu rõ** tại sao hiệu chỉnh Bessel là cần thiết
5. **Áp dụng** kiến thức vào thực tế nghiên cứu

## 🎨 Tính năng

- Tạo tổng thể với các tham số tùy chỉnh
- Lấy mẫu ngẫu nhiên với kích thước khác nhau
- Hiển thị trực quan phân phối dữ liệu
- So sánh phương sai được tính bằng hai phương pháp
- Mô phỏng nhiều lần lấy mẫu để thấy xu hướng

## 📚 Tài liệu tham khảo

Nội dung được phát triển dựa trên:
- Bài giảng về "Phân Tích Về Trung Bình Tổng Thể, Trung Bình Mẫu và Vấn Đề Ước Lượng Phương Sai"
- Lý thuyết thống kê suy luận cơ bản
- Khái niệm bậc tự do và ước lượng không chệch

## 🚀 Cách sử dụng

1. Mở file `index.html` trong trình duyệt
2. Điều chỉnh các tham số tổng thể
3. Thực hiện lấy mẫu
4. Quan sát sự khác biệt giữa hai phương pháp tính phương sai
5. Thử nghiệm với nhiều kích thước mẫu khác nhau

---

*Dự án này nhằm làm rõ một trong những khái niệm quan trọng nhất trong thống kê ứng dụng, giúp người học hiểu sâu sắc hơn về bản chất của ước lượng thống kê.*
