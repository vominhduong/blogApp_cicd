FROM eclipse-temurin:21-jre
WORKDIR /app

ARG SERVICE_NAME
ENV SERVICE_NAME=${SERVICE_NAME}

COPY backend/${SERVICE_NAME}/build/libs/ /tmp/libs/

RUN JAR_FILE=$(find /tmp/libs -name "*.jar" ! -name "*plain.jar" | head -n 1) && \
    cp "$JAR_FILE" /app/${SERVICE_NAME}.jar && \
    rm -rf /tmp/libs

CMD ["sh", "-c", "java -jar /app/${SERVICE_NAME}.jar"]