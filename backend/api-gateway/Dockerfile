FROM eclipse-temurin:21-jre
WORKDIR /app

# Vì ngữ cảnh (context) đã là thư mục của chính service này, 
# ta copy thẳng file .jar từ thư mục build/libs vào image và đổi tên thành app.jar cho gọn.
COPY build/libs/*.jar app.jar

# Khởi chạy ứng dụng
ENTRYPOINT ["java", "-jar", "app.jar"]
