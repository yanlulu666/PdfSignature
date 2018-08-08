# PdfSignature
itextpdf5.5.1对pdf进行生成签名的操作

# 步骤详情
一。用jdk自带的keytool生成一个p12的证书，生成过程如下（参考：https://www.cnblogs.com/zhangzb/p/5200418.html）
1.
方便复制版：
keytool -genkey -alias tomcat -keypass 123456 -keyalg RSA -keysize 1024 -validity 365 -keystore
D:/keys/tomcat.keystore -storepass 123456

2.
方便复制版：
keytool -genkey -alias client1 -keypass 123456 -keyalg RSA -keysize 1024 -validity 365 -storetype
PKCS12 -keystore D:/keys/client1.p12 -storepass 123456

注意：
①D:/keys/ 目录需要提前手动创建好，否则会生成失败
②提示输入域名的时候不能输入IP地址

二。准备一个签章的图片和一个pdf文档
