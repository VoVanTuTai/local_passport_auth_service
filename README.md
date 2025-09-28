🔐 Simple Auth
🚀 Cách chạy
1. Vào thư mục chứa dự án
cd src/local_passport_auth_service
2. Cài đặt dependencies bash Copy code: npm install express Basic Auth Chạy server bash Copy code: node app.js
Kiểm tra API
mongo trước khi đăng ký 
<img width="960" height="540" alt="3000" src="https://github.com/VoVanTuTai/local_passport_auth_service/blob/main/Images_report/mongo_after_register.png" />
POST: http://localhost:3000/auth/register (đăng ký sai)
body->raw->chỉnh type sang Json nội dung "{"username":"", "password":"12345"}"
<img width="960" height="540" alt="3000" src="https://github.com/VoVanTuTai/local_passport_auth_service/blob/main/Images_report/register_error.png" />
POST: http://localhost:3000/auth/register (đăng ký đúng)
body->raw->chỉnh type sang Json nội dung "{"username":"VoVanTuTai", "password":"12345"}"
<img width="960" height="540" alt="3000" src="https://github.com/VoVanTuTai/local_passport_auth_service/blob/main/Images_report/register.png" />
mongo sau khi đăng ký
<img width="960" height="540" alt="3000" src="https://github.com/VoVanTuTai/local_passport_auth_service/blob/main/Images_report/mongo_after_register.png" />
POST: http://localhost:3000/auth/login (đăng nhập sai)
body->raw->chỉnh type sang Json nội dung "{"username":"", "password":"12345"}"
<img width="960" height="540" alt="3000" src="https://github.com/VoVanTuTai/local_passport_auth_service/blob/main/Images_report/login_error.png" />
POST: http://localhost:3000/auth/login (đăng nhập đúng)
body->raw->chỉnh type sang Json nội dung "{"username":"VoVanTuTai", "password":"12345"}"
<img width="960" height="540" alt="3000" src="https://github.com/VoVanTuTai/local_passport_auth_service/blob/main/Images_report/login_success.png" />
GET: http://localhost:3000/auth/profile (xem profile khi đã đăng nhập thành công)
<img width="960" height="540" alt="3000" src="https://github.com/VoVanTuTai/local_passport_auth_service/blob/main/Images_report/profile.png" />
GET: http://localhost:3000/auth/logout (đăng xuất)
<img width="960" height="540" alt="3000" src="https://github.com/VoVanTuTai/local_passport_auth_service/blob/main/Images_report/logout.png" />
GET: http://localhost:3000/auth/profile (xem profile khi đã đăng xuất)
<img width="960" height="540" alt="3000" src="https://github.com/VoVanTuTai/local_passport_auth_service/blob/main/Images_report/prolife_after_logout.png" />
