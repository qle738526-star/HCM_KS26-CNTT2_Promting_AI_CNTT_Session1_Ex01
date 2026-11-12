**Bài 1: Hiểu đúng bản chất "Máy dự đoán từ tiếp theo" (Next Token Prediction) của LLM** 

**Phần 1 (Bóc tách nhận thức sai) 2 điểm sai lầm trong báo cáo của Nam:**

**\- Sai lầm 1: Cho rằng "phần mềm bị hỏng hoặc máy chủ bị lỗi".** Việc mô hình đưa ra kết quả sai (44.130) không phải là sự cố hệ thống. AI vẫn đang hoạt động hoàn toàn bình thường theo đúng cơ chế thiết kế của nó, chỉ là Nam đang dùng sai công cụ cho mục đích tính toán.

**\- Sai lầm 2: Tin rằng LLM có "bộ vi xử lý máy tính bên trong".** Hàng trăm tỷ tham số của ChatGPT dùng để lưu trữ các mẫu ngôn ngữ và trọng số thống kê, không chứa các thuật toán số học logic cứng nhắc như một chiếc máy tính bỏ túi

**\- Nguyên nhân tính sai:** Trong giai đoạn **Pre-training**, LLM chỉ học xác suất ngôn ngữ chứ không học thuật toán toán học. Do đó, nó sử dụng **Next Token Prediction** để "đoán" chuỗi chữ số tiếp theo dựa trên thói quen dữ liệu. Vì phép toán này ít xuất hiện, AI đã đoán sai xác suất dẫn đến kết quả 44.130. .

**Phần 2: Sửa lỗi và đề xuất lệnh Promt**:

\-Câu lệnh Promt: "Hãy tính tổng của 15.480 và 28.750. Yêu cầu: Hãy sử dụng công cụ Code Interpreter (viết đoạn mã Python) để thực thi phép tính này và trả về kết quả."

\-Giải thích: Cách này ép AI ngừng việc "đoán chữ" và kích hoạt môi trường lập trình. Môi trường Python sẽ xử lý phép toán theo đúng logic máy tính, đảm bảo kết quả chính xác 100%.

