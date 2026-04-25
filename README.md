*Dự án nghiên cứu và chế tạo Bảng điều khiển thông minh đa nhiệm (Smart Dashboard) tích hợp Cảnh báo điểm mù dành cho mô tô và xe máy. Hệ thống sử dụng vi điều khiển ESP32 để giải quyết các vấn đề về an toàn giao thông và hỗ trợ điều hướng rảnh tay.
*Các tính năng chính:
Dự án được thiết kế với cơ chế đa nhiệm, cho phép người dùng chuyển đổi linh hoạt qua 3 chế độ hoạt động bằng cảm biến chạm TTP223:

Mode 0 - Blind Spot Radar: Sử dụng cảm biến siêu âm kết hợp thuật toán lọc nhiễu trung bình (Moving Average) để giám sát vật cản trong vùng mù. Cảnh báo tức thời qua còi Buzzer và hệ thống đèn LED RGB (Fading hiệu ứng theo khoảng cách).

Mode 1 - Google Maps Navigation: Đồng bộ dữ liệu chỉ đường từ điện thoại qua Bluetooth BLE (sử dụng thư viện ChronosESP32). Hiển thị icon mũi tên rẽ và số mét thực tế từ Google Maps lên màn hình OLED.

Mode 2 - Internet Clock: Đồng bộ thời gian thực từ máy chủ NTP qua kết nối Wi-Fi, cung cấp giờ giấc chính xác tuyệt đối mà không cần module RTC phần cứng

*Linh kiện phần cứng
ESP32 C3:	Vi điều khiển trung tâm hỗ trợ Wi-Fi & Bluetooth BLE
OLED 0.96" SSD1306:	Màn hình hiển thị giao diện I2C
US-016 hoặc HC-SR04:	Cảm biến siêu âm đo khoảng cách vật cản
TTP223:	Cảm biến chạm
LED RGB & Buzzer:	Hệ thống cảnh báo quang/âm

*Yêu cầu phần mêm thư viện
Dự án được lập trình trên môi trường Arduino IDE. Các thư viện cần thiết bao gồm:

BlynkSimpleEsp32 (Kết nối IoT Dashboard)

ChronosESP32 (Giao tiếp Bluetooth BLE cho Navigation)

Adafruit_SSD1306 & Adafruit_GFX (Hiển thị OLED)

NTPClient & WiFiUdp (Đồng bộ thời gian)
