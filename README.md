# SpringREST-API-File-Upload


Spring Boot REST API with  file upload using Ajax requests and components used in this project:

Spring Boot 1.4.3.RELEASE

Spring 4.3.5.RELEASE

Thymeleaf

jQuery (webjars)

Maven

Embedded Tomcat 8.5.6

Google Chrome Browser (Network Inspect)



_Testing File uploading  with cURL command_


1.Testing only  single file upload.

Terminal
$ curl -F file=@"f:\\data.txt" http://localhost:8080/api/upload/
Successfully uploaded - data.txt

2.Testing  with multiple file uploads 

Terminal
$ curl -F extraField="abc" -F files=@"f://data.txt" -F files=@"f://data2.txt"  http://localhost:8080/api/upload/multi/
Successfully uploaded - data.txt , data2.txt


3.Testing  multiples file upload, maps to Model.

Terminal
$ curl -F extraField="abc" -F files=@"f://data.txt" -F files=@"f://data2.txt"  http://localhost:8080/api/upload/multi/model
Successfully uploaded!

4.Testing  a large movie file (100MB), the following error message will be displayed.

Terminal
$ curl -F file=@"F://movies//300//Sample.mkv"  http://localhost:8080/api/upload/

Attachment size exceeds the allowable limit! (10MB)
