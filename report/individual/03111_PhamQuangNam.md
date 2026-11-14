# Báo cáo cá nhân — HoVaTen-MSSV

Đổi tên file theo quy tắc `MSSV_HoTen.md`. Ví dụ: `20241234_NguyenVanAn.md`.

Đoạn video: MOT17-09, 150 frame (frame 1–150), nguồn MOTChallenge, giấy phép CC BY-NC-SA 3.0.

## 0. Thông tin học viên

- Họ tên: Phạm Quang Nam 
- MSSV: 03111
- Mã đề (A/B/C): C
- Email: quangnam97425@gmail.com
- Link repository: 
- Giờ bắt đầu: 17h00
- Giờ kết thúc: 19h00

## 1. Xem trước đoạn video (CP0)

Ghi **trước khi vẽ**, mỗi người một dòng.

| Mã | Frame xuất hiện | Frame cuối thấy được | Rẽ / dừng / đổi tốc độ ở frame | Bị che ở frame | Ghi chú |
|---|---|---|---|---|---|
| P1 | 0 | 150 | 30 | 41 | |
| P2 | 61 | 150 |  | 55 | |
| P3 | 40 | 150 |  |  | |
| P4 | 2 | 102 | 48 | 101 | |
| P5 | 28 | 136 |  | 112 | |

## 2. Keyframe và thời gian (CP1, CP4)

Số keyframe lấy từ kết quả `src/check_submission.py`.

| Mã | Số keyframe | Keyframe ở frame | Số frame có mặt | Keyframe / 100 frame | Thời gian (phút) | Chỗ khó |
|---|---|---|---|---|---|---|
| P1 | 15 | 19, 20, 30, 40, 50, 60, 70, 80, 90, 100, 110, 120, 130, 140, 149 | 131  | 11.5 | 20 | |
| P2 | 97 | 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 40, 41, 45, 46, 47, 48, 49, 50, 51, 52, 53, 
54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 70, 71, 72, 73, 74, 75, 76, 77, 78, 80, 81, 82, 83, 84, 85, 87, 89, 90, 91, 93, 94, 95, 96, 97, 99, 100, 101, 102, 103, 104, 105, 106, 110, 111, 
113, 114, 115, 117, 127, 128, 129, 130, 131 | 117 | 82.9 | 25 | |
| P3 | 29 | 0, 24, 49, 55, 57, 60, 66, 69, 75, 81, 83, 84, 85, 87, 88, 94, 99, 103, 105, 108, 113, 115, 118, 119, 122, 125, 131, 140, 149 | 140 | 20.7 | 15 | |
| P4 | 14 | 0, 13, 15, 18, 19, 23, 34, 44, 50, 75, 89, 91, 92, 93 | 104 | 13.5 | 15 | |
| P5 | 19 | 47, 58, 59, 60, 67, 68, 75, 79, 85, 86, 89, 99, 100, 102, 107, 114, 133, 137, 149 | 103 | 18.4 | 10 | |
| **Tổng** | 174 | | 595 | 147 | 75 | |

Keyframe / 100 frame của cả bài = tổng keyframe ÷ tổng số frame có mặt × 100 = ...

Bạn đặt keyframe nhiều nhất ở người nào? Vì sao (người đó rẽ, dừng, lại gần camera hay bị che)?
Tôi đặt keyframe nhiều nhất ở người số 5.
Vì dựa theo góc camera, cơ thể của người số 5 này bắt đầu gần hơn ở camera và dần dần đi xa, thêm với tốc độ đột ngột của người này, thành ra phải có nhiều keyframe.
...

## 3. Đoạn bị che (CP2)

Người bị che: `P1`

| Mốc | Frame |
|---|---:|
| Bắt đầu bị che một phần (bật `occluded`) | 41 |
| Mất hẳn (bật `outside`) | 42 |
| Hiện lại (tắt `outside`) | 50 |
| Thấy rõ trở lại (tắt `occluded`) | 56 |

- Thời gian khuất hẳn: 60 frame = 1 giây.
- Quyết định: giữ cùng ID / tạo track mới.
- Lý do (trả lời 3 câu: khuất bao lâu so với 60 frame, ngoại hình có khớp, chỗ hiện lại có đúng hướng và tốc độ):

...

Ảnh chụp màn hình:

![Trước khi che](images/che_1_truoc.png)
![Giữa đoạn che, thấy cờ trên panel object](images/che_2_giua.png)
![Sau khi hiện lại, cùng ID](images/che_3_sau.png)

## 4. Tự review ID (CP3)

Lượt 1 theo người (đi ngược từ frame 149 về 0 trên CVAT), lượt 2 theo cảnh (nhảy 10 frame). Ít nhất 3 dòng; không có lỗi thì ghi một dòng "đã kiểm hai lượt, không lỗi".

Loại lỗi dùng đúng một trong 7 mã: `id_switch`, `fragmentation`, `lost`, `merge`, `false_track`, `drift`, `flag`.

| Frame | Mã người | Loại lỗi | Mô tả một câu | Phát hiện ở lượt | Đã sửa? |
|---:|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

Tổng hợp số lỗi theo loại:

| `id_switch` | `fragmentation` | `lost` | `merge` | `false_track` | `drift` | `flag` |
|---:|---:|---:|---:|---:|---:|---:|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 |

Lỗi nào chỉ lượt 2 (theo cảnh) mới thấy, lượt 1 (theo người) không thấy? Vì sao?
...

## 5. File xuất và kết quả tự kiểm (CP4)

| Kiểm tra | Kết quả |
|---|---|
| Tên file MOT 1.1 | job_9_annotations_2026_11_13_12_15_41_mot 1.1 |
| Tên file CVAT for video 1.1 | job_9_annotations_2026_11_13_12_15_41_cvat for video 1.1 |
| Số track ID khác nhau trong `gt/gt.txt` (phải là 5) | 1,1,258.32,458.03,94.69,247.91000000000008,1,1,1.0; 1,2,1292.62,461.58,66.76000000000022,196.93,1,1,1.0; 2,1,259.97,457.79,95.25,248.09999999999997,1,1,1.0;  2,2,1294.52,461.61,67.5,197.12,1,1,1.0; 7,1,268.21,456.58,98.04000000000002,249.05,1,1,1.0 |
| Frame `outside` không có dòng trong `gt.txt` (đúng / sai) | Đúng |
| Job đã completed trên CVAT máy cá nhân | Đúng |

Dán phần tóm tắt in ra từ `src/check_submission.py`:

```text
Lỗi: 0   |   Cảnh báo: 1
  Không có lỗi định dạng. Mở CVAT xem lại từng [CẢNH BÁO]; cảnh báo đúng ý bạn thì ghi lý do vào báo cáo.
```

## 6. Ba câu kết

1. Nếu được gán lại, bạn sẽ đặt keyframe khác ở đâu? Vì sao?
Tôi sẽ đặt ở frame 1 và frame cuối, vì keyframe nó hoạt động như linear interpolation qua các frame, nên tôi sẽ đặt thế để tiết kiệm thời gian

2. Có chỗ nào bạn không chắc "cùng ID hay ID mới"? Bạn đã quyết định và ghi chú thế nào?
Không có chỗ nào là tôi không chắc do trường hợp và bài tôi làm chưa gặp trường hợp đó

3. Một lỗi ID trong job của bạn (nếu không còn sót, chọn lỗi đã sửa) có thể làm xe tự lái dự đoán sai chuyển động của người đó như thế nào? Lỗi đó ảnh hưởng MOTA hay IDF1 nhiều hơn?
Một lỗi ID có thể gây ra dự đoán sai và ảnh hưởng nghiêm trọng trong việc dự đoán chuyển động.
Lỗi đó ảnh hưởng IDF1 nhiều hơn MOTA


## Bonus (nếu làm)

### B1 — Hai người đi sát

...

### B2 — So cách đặt keyframe

| Cách đặt | Số keyframe | Frame trôi nhất | Ghi chú |
|---|---:|---:|---|
| Đều mỗi 30 frame | | | |
| Theo chỗ đổi hướng | | | |

...

### B3 — So với tracker có sẵn

| Frame | Mã người | Tracker làm gì | Nhãn của bạn | Giải thích (đoán rồi sửa / ghép IoU / box score thấp / ngoại hình) |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## 7. Tài liệu tham khảo và công cụ AI đã dùng

...
