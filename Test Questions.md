# Test Questions

## 1. Anh đã từng dùng AI để hoàn thành những công việc gì?

Mình dùng AI để rút ngắn cycle từ research đến MVP xuống còn vài ngày thay vì vài tuần. Cụ thể có 3 use case chính:

- **Automate due diligence:** Mình xây một hệ thống gồm 4 Agent trên Paperclip để tự động hoá quá trình DD chuyên sâu cho các project trước khi list trên Whales Market. Trước đó việc này mất nhiều giờ manual, giờ output ra nhanh hơn và consistent hơn.

- **Research trend & tìm ý tưởng sản phẩm:** Mình build một Agent có skill research chuyên theo dõi và phân tích các trend mới xuất hiện trên market, từ đó đề xuất ý tưởng product phù hợp thay vì chờ brainstorm thủ công.

- **Từ ý tưởng đến MVP:** Khi sếp approve ý tưởng, mình dùng Claude CLI để build MVP trực tiếp trên GitHub và demo luôn. Nếu được confirm, mình tinh chỉnh theo yêu cầu biz rồi bàn giao cho team Tech để estimate và xử lý phần chuyên sâu.

---

## 2. Quy trình sử dụng AI trong quá trình làm?

- **Knowledge base tự build:** Mình maintain một knowledge base riêng, cập nhật thường xuyên để làm trusted source cho AI — tránh hallucinate và đảm bảo output bám sát context thực tế của công ty.

- **Chọn model theo độ khó task:** Task research đơn giản thì dùng model nhẹ hơn như Haiku hoặc Flash để tiết kiệm token. Task cần reasoning sâu hoặc code phức tạp thì mới leo lên Opus hay Gemini Pro.

- **Dùng đúng skill cho từng task:** Mỗi loại task mình có prompt template chuyên biệt — giúp AI focus đúng context, tránh generate lan man và giảm thiểu vòng lặp fix lỗi không cần thiết.

---

## 3. Khi gặp vấn đề anh xử lý như nào?

Mình không có một quy trình cứng nhắc mà phân loại vấn đề trước rồi mới chọn tool:

- **Vấn đề cần research/thông tin thị trường:** Dùng Grok vì strong ở real-time data và trending context.

- **Vấn đề về bug hoặc logic tính năng:** Dùng Claude, vibe coding thẳng phần fix để team có thể review trực tiếp thay vì đọc mô tả.

- **Quan trọng hơn là validate output:** Mình không trust AI 100% — sau khi có kết quả, mình luôn cross-check với knowledge base hoặc test thực tế trước khi bàn giao. Điều này giúp tránh được khá nhiều lỗi âm thầm mà AI tự tin generate sai.

---

## 4. Quy trình hoặc cách sử dụng nào là tối ưu?

Sau một thời gian dùng, mình rút ra 3 nguyên tắc cốt lõi:

- **Knowledge base là nền tảng:** AI giỏi đến đâu mà không có context đúng thì output vẫn lệch. Việc build và maintain knowledge base riêng là thứ tạo ra sự khác biệt lớn nhất.

- **Đúng model, đúng task:** Mỗi model mạnh một điểm — Codex/Claude tốt cho code chi tiết và MVP, Gemini mạnh về visual và gen ảnh/video, Grok tốt cho research real-time. Dùng đúng chỗ vừa ra kết quả tốt hơn, vừa tiết kiệm chi phí.

- **Skill chuyên biệt thay vì prompt chung:** Thay vì hỏi AI theo kiểu chung chung, mình dùng các skill/template được thiết kế riêng cho từng loại task. Cách này giúp không bỏ sót case và đôi khi còn ra được những góc nhìn phụ giá trị mà mình chưa nghĩ tới.
