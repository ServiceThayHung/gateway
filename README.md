- Notification service:
POST **/email/sender

[
    {
        "email": "emilydotmancy007@gmail.com",
        "subject": "Xin chào",
        "content": "Cảm ơn bạn"   
    },
    {
        "email": "nguyenvietanh140820@gmail.com",
        "subject": "Xin chào",
        "content": "Cảm ơn bạn"   
    }
]

- Keyword service:

POST https://my-keyword-finder.herokuapp.com/keyword/finder
{
    "text": "fgjdljafldsaf",
    "keywords": [
        "ja",
	  "fdsjf"
    ]
}


- Cv service:

URL: https://my-cv-service.herokuapp.com/

Upload file:
	POST https://my-cv-service.herokuapp.com/cv/upload
	form: file 
	
	api trả về id của file mới upload

Upload nhiều file:
	POST https://my-cv-service.herokuapp.com/cv/uploads
	form: files 
	
	api trả về ds id của files mới upload

Xem list files:
	GET https://my-cv-service.herokuapp.com/cv/files
	
Tải file:
	GET https://my-cv-service.herokuapp.com/cv/files/{id}

Lấy nội dung của cv:
	GET https://my-cv-service.herokuapp.com/cv/gettextscan/{id}

Lấy nội dung của nhiều cv:
	GET https://my-cv-service.herokuapp.com/cv/gettextscan?ids={id1},{id2},...

Lấy metadata của cv:
	GET https://my-cv-service.herokuapp.com/cv/getmetadata/{id}

Lấy metadata của nhiều cv:
	GET https://my-cv-service.herokuapp.com/cv/getmetadata?ids={id1},{id2},...

Lấy tất cả của CV (nội dung + metadata tương ứng):
	GET https://my-cv-service.herokuapp.com/cv/getall/{id}

Lấy tất cả của nhiều CV (nội dung + metadata tương ứng):
	GET https://my-cv-service.herokuapp.com/cv/getall?ids={id1},{id2},...
