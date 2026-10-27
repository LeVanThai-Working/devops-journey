# Module 0
- Lab:
    + Chạy Floci bằng Docker Compose, tạo S3 bucket
    + Kết nối AWS CLI :
        `export AWS_ENDPOINT_URL=http://localhost:4566
        export AWS_DEFAULT_REGION=us-east-1
        export AWS_ACCESS_KEY_ID=test
        export AWS_SECRET_ACCESS_KEY=test`
    -> Cần nắm: lệnh export chỉ có tác dụng trong terminal đang mở. Mở terminal mới là mất, và AWS CLI sẽ báo lỗi kết nối.

    + Tạo bucket:
       `aws s3 mb s3://my-second-bucket`
       `aws s3 ls`
    -> Cần nắm: bucket là “thùng chứa” cấp cao nhất, tên phải duy nhất trong phạm vi một dịch vụ (trên AWS thật là duy nhất global)

    + Tạo file ở local (Ubuntu) xong upload lên aws s3:
        `echo "file one" > file1.txt`
        `echo "file two" > file2.txt`
        `aws s3 cp file1.txt s3://my-second-bucket/`
        `aws s3 cp file2.txt s3://my-second-bucket/docs/file2.txt`
        `aws s3 ls s3://my-second-bucket/`
        `aws s3 ls s3://my-second-bucket/ --recursive`
    -> Cần nắm: 
        + Đối tượng trong S3 gọi là object (key + dữ liệu)
        + S3 không có thư mục thật. docs/file2.txt chỉ là key (tên đối tượng) có dấu /. Giao diện hiển thị như thư mục cho dễ nhìn.
        + --recursive liệt kê tất cả object ở mọi “thư mục con”.
- Lỗi đã gặp: Compose báo "services must be a mapping" do file YAML sai thụt lề; git init hiện hint về nhánh master (không phải lỗi)
- Bài học: Delivery = có nút duyệt thủ công; Deployment = tự động hoàn toàn

