```
saga-security-microservices/
├── api-gateway/          (Cổng vào, check JWT Token)
├── order-service/        (Nhạc trưởng - Tạo đơn & Chứa Temporal Workflow)
├── payment-service/      (Thành viên - Xử lý tiền tệ)
├── notification-service/ (Thành viên - Gửi thông báo)
└── shared-dtos/          (Thư viện chung chứa các Class DTO)
```

```
saga-security-microservices/
├── buildSrc/                      <-- Nơi chứa cấu hình Gradle tập trung (Convention Plugins)
│   ├── build.gradle.kts
│   └── src/main/kotlin/spring-boot-common.gradle.kts
├── auth-service/                  <-- Service nhỏ số 1
│   └── build.gradle.kts
├── order-service/                 <-- Service nhỏ số 2
│   └── build.gradle.kts
├── shared-library/                <-- Thư viện dùng chung (DTO, Utils...)
│   └── build.gradle.kts
├── build.gradle.kts               <-- File build của root (thường để trống)
├── settings.gradle.kts            <-- Khai báo danh sách các service
└── gradle.properties              <-- Định nghĩa phiên bản Spring Boot, Java

```
