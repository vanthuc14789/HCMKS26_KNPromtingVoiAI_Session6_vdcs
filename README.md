---


---

<h1 id="bài-tập-thiết-kế-giải-pháp-prompting-ứng-dụng-ai-trong-học-tập"><strong>BÀI TẬP: THIẾT KẾ GIẢI PHÁP PROMPTING ỨNG DỤNG AI TRONG HỌC TẬP</strong></h1>
<h2 id="phân-tích-bài-toán"><strong>1. Phân tích bài toán</strong></h2>
<p><strong>Tên giải pháp:</strong> AI gia sư Feynman kết hợp chấm bài bằng Rubric.</p>
<p><strong>Mục tiêu:</strong></p>
<ul>
<li>Giải thích kiến thức dễ hiểu.</li>
<li>Kiểm tra mức độ hiểu bài.</li>
<li>Tự động chấm điểm theo Rubric.</li>
<li>Phát hiện dữ liệu thiếu hoặc sai.</li>
</ul>
<h2 id="bước-1-thiết-kế-input--output"><strong>2. Bước 1: Thiết kế Input / Output</strong></h2>
<p><strong>Input (Đầu vào):</strong></p>
<ul>
<li>Chủ đề cần học.</li>
<li>Trình độ sinh viên.</li>
<li>Câu hỏi bài tập.</li>
<li>Bài làm của sinh viên.</li>
<li>Tiêu chí Rubric và thang điểm.</li>
</ul>
<p><strong>Output (Đầu ra):</strong></p>
<ul>
<li>Giải thích kiến thức theo Feynman.</li>
<li>3 câu hỏi kiểm tra.</li>
<li>Bảng điểm theo Rubric.</li>
<li>Nhận xét ưu, nhược điểm.</li>
<li>Tổng điểm và cách cải thiện.</li>
</ul>
<h2 id="bước-2-viết-prompt-thực-thi"><strong>3. Bước 2: Viết Prompt thực thi</strong></h2>
<p>Bạn là AI gia sư sử dụng phương pháp Feynman và chấm bài theo Rubric.</p>
<p><strong>Nhiệm vụ:</strong></p>
<ol>
<li>Giải thích kiến thức bằng ngôn ngữ đơn giản, có ví dụ thực tế.</li>
<li>Đặt 3 câu hỏi kiểm tra kiến thức.</li>
<li>Chấm bài theo từng tiêu chí Rubric.</li>
<li>Nhận xét ưu điểm, nhược điểm và cách cải thiện.</li>
</ol>
<p><strong>Input:</strong></p>
<ul>
<li>Chủ đề: Mạng máy tính.</li>
<li>Trình độ: Sinh viên năm nhất.</li>
<li>Bài làm: Mạng máy tính là hệ thống kết nối nhiều máy tính để trao đổi dữ liệu.</li>
<li>Rubric:
<ul>
<li>Đúng kiến thức: 4 điểm.</li>
<li>Giải thích rõ ràng: 3 điểm.</li>
<li>Ví dụ thực tế: 2 điểm.</li>
<li>Trình bày: 1 điểm.</li>
</ul>
</li>
</ul>
<p><strong>Điều kiện xử lý lỗi:</strong></p>
<ul>
<li>Nếu thiếu bài làm, không chấm điểm.</li>
<li>Nếu thiếu Rubric, yêu cầu bổ sung.</li>
<li>Nếu dữ liệu sai, yêu cầu kiểm tra lại.</li>
<li>Không tự bịa thông tin hoặc thay đổi thang điểm.</li>
</ul>
<p><strong>Output:</strong> Trình bày kết quả rõ ràng, ngắn gọn, dễ hiểu và có tổng điểm.</p>
<h2 id="kết-quả-chạy-thử"><strong>4. Kết quả chạy thử</strong></h2>
<p><strong>Giải thích Feynman:</strong></p>
<p>Mạng máy tính là hệ thống kết nối nhiều máy tính để chia sẻ dữ liệu và tài nguyên.</p>
<p>Ví dụ: Các máy tính trong phòng học có thể kết nối để sử dụng chung máy in.</p>
<p><strong>Câu hỏi kiểm tra:</strong></p>
<ol>
<li>Mạng máy tính là gì?</li>
<li>Mạng máy tính có lợi ích gì?</li>
<li>Internet có phải mạng máy tính không?</li>
</ol>
<p><strong>Kết quả chấm Rubric:</strong></p>

<table>
<thead>
<tr>
<th>Tiêu chí</th>
<th>Điểm tối đa</th>
<th>Điểm đạt</th>
</tr>
</thead>
<tbody>
<tr>
<td>Đúng kiến thức</td>
<td>4</td>
<td>4</td>
</tr>
<tr>
<td>Giải thích rõ ràng</td>
<td>3</td>
<td>3</td>
</tr>
<tr>
<td>Ví dụ thực tế</td>
<td>2</td>
<td>0</td>
</tr>
<tr>
<td>Trình bày</td>
<td>1</td>
<td>1</td>
</tr>
<tr>
<td><strong>Tổng</strong></td>
<td><strong>10</strong></td>
<td><strong>8</strong></td>
</tr>
</tbody>
</table><p><strong>Nhận xét:</strong></p>
<ul>
<li>Ưu điểm: Kiến thức đúng, trình bày rõ ràng.</li>
<li>Nhược điểm: Chưa có ví dụ thực tế trong bài làm.</li>
<li>Cải thiện: Bổ sung ví dụ minh họa.</li>
</ul>
<h2 id="kiểm-thử-lỗi-dữ-liệu"><strong>5. Kiểm thử lỗi dữ liệu</strong></h2>
<ul>
<li>Thiếu bài làm: Yêu cầu nhập bài.</li>
<li>Thiếu Rubric: Yêu cầu bổ sung tiêu chí.</li>
<li>Sai thang điểm: Yêu cầu kiểm tra lại.</li>
<li>Dữ liệu trống: Không thực hiện chấm điểm. 					
