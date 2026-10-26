1. Vòng đời của DevOps (hình số 8 vô tận): 
- Plan: lập kế hoạch, xác định yêu cầu cho dự án
- Code: bắt đầu viết code cho dự án
- Build: build code đã viết ra để chạy
- Test: kiểm thử trước khi đưa vào sản phẩm
- Release: bàn giao repo hoàn thiện sau khi được tích hợp (chưa đên lên production)
- Deploy: phát triển dự án lên production
- Operate: vận hành sản phẩm trong thực tế
- Monitor: giám sát hiệu suất của hệ thống, để có các biện pháp phòng ngừa kịp thời, rồi phản hồi quay lại Plan
2. CI vs Continuous Delivery vs Continuous Deployment:
- CI (Continuous Integration): tự động tích hợp (build + test) code lên production
- CD (Continuous Delivery): giao bản code sẵn sàng nhưng chưa deploy, cần phải manual deploy
- CD (Continuous Deployment): tự động deploy lên prodcution mà không cần ai duyệt hay thực hiện manual
3. 4 vai trò:
- DevOps: người xây dựng hệ thống pipeline xử lí tự động hóa deploy
- SRE: vai trò giữ ổn định cho hệ thống, đo bằng SLO và xử lí sự cố
- Platform engineer: xây dựng nền tảng local (nội bộ) để dev tự phục vụ
- Cloud Engineer: thiết kế và xây dựng các hạ tầng trên điện toán đám mây (cloud)
