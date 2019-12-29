Created By: Yinzuo Jiang
Last Edited: Dec 29, 2019 8:34 PM
Tags: DevOps, Docker

[ChiangYintso/springboot-learning1](https://github.com/ChiangYintso/springboot-learning1)



{% asset_img Docker运行Springboot%20Application/Untitled.png This is an example image %}

将打包后的jar包和DockerFile放在同一目录下。

    # From java image, version : 11
    FROM java:latest
    
    # 挂载app目录
    VOLUME /app
    
    # COPY or ADD to image
    ADD app.jar /app/
    
    EXPOSE 8081
    ENTRYPOINT ["java",  "-Dserver.port=8081", "-jar", "/app/app.jar"]

编写DockerFile

{% asset_img Docker运行Springboot%20Application/Untitled1.png This is an example image %}

设置Run Configuration

{% asset_img Docker运行Springboot%20Application/Untitled2.png This is an example image %}

设置容器

{% asset_img Docker运行Springboot%20Application/Untitled3.png This is an example image %}

运行