# Project demo triển khai kiến trúc microservice bằng .NET/C#, reactjs
## Description
  Dự án này sẽ xây dựng một web bán hàng cơ bản dùng kiến trúc microservice.
## Các microservice dự định sẽ dựng:
- User service: Chịu trách nhiệm xác thực, phân quyền, định danh người dùng.
- Product service: Quản lý các sản phẩm mua bán.
- Order service: Quản lý đơn hàng.
- Checkout service: Thanh toán đơn hàng.
- Report service: Thông kê báo cáo doanh thu / lợi nhuận / chi phí sản phẩm.
- **Gateway service**: Gọi các service khác để trả về web client.
- Storage service: Chịu tránh nhiệm lưu trữ file.
## Những công nghệ dự định sẽ sử dụng:
- Sử dụng RabitMQ làm message queue giúp giao tiếp giữa các service.
- .NET/C# để xây dựng các service.
- Docker để deploy và chạy các service độc lập.
- ReactJS xây dựng front-end: Chỉ dựng UI đơn giản để demo kiến trúc microservice, không làm phức tạp để tiết kiệm thời gian.
- Azure Virtual Machine để làm server triển khai CI/CD.
## Sử dụng chung database cho các service hay mỗi service sẽ sử dụng database khác nhau?
Việc sử dụng chung một database có ưu điểm là giúp tiết kiểm thời gian thiết kế db,
dễ dàng nhận thấy mỗi quan hệ giữa các thực thể, tuy nhiên để giảm sự phụ thuộc / tăng khả năng bảo trì và phát triển
một service thì mỗi service có một db riêng là sự lựa chọn tốt. Tuy nhiên tách db cho mỗi service là 
một việc không hề đơn giản. Với dự án này thì database không quá phức tạp nên mỗi service sẽ có db riêng. Còn
trong dự án thực tế thì sẽ tùy tình hình mà có lựa chọn phù hợp.
