Session04-Ex04

## 1. Tạo và cấu hình .gitignore
Tạo file `.gitignore` và thêm:
credentials.txt
Mục đích là để Git bỏ qua file `credentials.txt` trong các lần theo dõi sau.

## 2. Gỡ file khỏi Git nhưng giữ lại trên máy
Do `credentials.txt` đã được commit trước đó, sử dụng lệnh:

git rm --cached credentials.txt

Lệnh này gỡ file khỏi vùng theo dõi của Git nhưng không xóa file vật lý khỏi thư mục làm việc.

Kiểm tra bằng `ls -la credentials.txt` cho thấy file vẫn còn trên máy.

## 3. Sửa commit gần nhất bằng Amend
Sử dụng lệnh:

git commit --amend -m "xoa file nhay cam"

Commit gần nhất được thay thế bằng commit mới với thông điệp:

xoa file nhay cam

Kiểm tra bằng:

git log -n 1

Kết quả:

95f0c95 xoa file nhay cam

## 4. Kiểm tra

Lệnh `git status` không còn hiển thị `credentials.txt`, chứng minh file đã được loại khỏi Git nhưng vẫn tồn tại trên máy.