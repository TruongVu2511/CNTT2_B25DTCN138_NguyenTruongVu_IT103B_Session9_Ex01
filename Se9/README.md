1. Phân tích lỗi
Dòng bookingReservation.priceKey sai vì JavaScript tìm thuộc tính tên priceKey, không tìm thấy nên trả về undefined, khiến tổng tiền thành NaN.

Cách sửa:
const basePrice = bookingReservation[priceKey];
Bracket Notation (obj[key]) cho phép truy cập thuộc tính bằng giá trị của biến key.

2. Bảng Test Cases
Trường hợp kiểm thử	Dữ liệu đầu vào	Kết quả sai thực tế	Kết quả đúng mong đợi
TC01: Nhận phòng trước 12 giờ	roomPrice = 1500000, checkInHour = 9, priceKey = "roomPrice"	basePrice = undefined, phụ thu và tổng tiền là NaN	Giá phòng: 1.500.000 VNĐ; phụ thu: 450.000 VNĐ; tổng tiền: 1.950.000 VNĐ
TC02: Nhận phòng từ 12 giờ trở đi	roomPrice = 1500000, checkInHour = 14, priceKey = "roomPrice"	basePrice = undefined, tổng tiền là NaN	Giá phòng: 1.500.000 VNĐ; phụ thu: 0 VNĐ; tổng tiền: 1.500.000 VNĐ
