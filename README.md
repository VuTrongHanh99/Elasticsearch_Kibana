"# Elasticsearch_Kibana" <br/>
<b>Link download</b>:<br/>
https://drive.google.com/drive/folders/1j9tODzSWUX33zm8-qrgaJJOzfXtDqnk-
<br/>
http://localhost:9200/
$	elasticsearch-reset-password -u elastic
=>e1JFYsn3D1vzYrlbdE9y
$	elasticsearch-users useradd admin -p pass123 -r network,monitoring,admins

====================Kibana
Tạo token: 
$	elasticsearch-service-tokens create elastic/kibana my-token
=>SERVICE_TOKEN elastic/kibana/my-token = AAEAAWVsYXN0aWMva2liYW5hL215LXRva2VuOjdpWWo1QkV0VFZpVV8tbEpvaXhLX1E


=============================================================================================================
--server.host: "http://localhost"
--elasticsearch.hosts: ["http://localhost:9200"]
--elasticsearch.serviceAccountToken: "AAEAAWVsYXN0aWMva2liYW5hL215LXRva2VuOjdpWWo1QkV0VFZpVV8tbEpvaXhLX1E"


chạy lệnh này: 
$	elasticsearch-create-enrollment-token -s kibana
=>eyJ2ZXIiOiI4LjUuMyIsImFkciI6WyIxOTIuMTY4LjEuNTc6OTIwMCJdLCJmZ3IiOiIyZTY2MWQxZGU2ODg1NDQ1YTA1ZTI1OTA5YzRkN2Q1ZTVhNWEyNGIyZmQ2NWNlYmVkODZkNjAwZmI1YTBmOTlhIiwia2V5IjoiMF9rV0tJVUI4UlZaQ3F1N2xFQTI6YjBUbXE0LXpUTHFaTl9pNF9oQjllZyJ9
$	kibana-setup --enrollment-token eyJ2ZXIiOiI4LjUuMyIsImFkciI6WyIxOTIuMTY4LjEuNTc6OTIwMCJdLCJmZ3IiOiIyZTY2MWQxZGU2ODg1NDQ1YTA1ZTI1OTA5YzRkN2Q1ZTVhNWEyNGIyZmQ2NWNlYmVkODZkNjAwZmI1YTBmOTlhIiwia2V5IjoiMF9rV0tJVUI4UlZaQ3F1N2xFQTI6YjBUbXE0LXpUTHFaTl9pNF9oQjllZyJ9

