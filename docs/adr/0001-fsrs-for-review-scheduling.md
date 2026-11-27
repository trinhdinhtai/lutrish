# 1. FSRS cho lịch ôn tập

- Trạng thái: Accepted
- Ngày: 2026-11-27

## Bối cảnh

Lutrish xếp lịch ôn Card theo lặp lại ngắt quãng. Hai lựa chọn chính: SM-2 (thuật toán cổ điển của Anki, đơn giản) và FSRS (mô hình độ nhớ hiện đại, có thư viện TypeScript `ts-fsrs`).

## Quyết định

Dùng FSRS qua `ts-fsrs`. Learner tự chấm bằng 4 mức (Quên / Khó / Được / Dễ), ánh xạ thẳng sang Again / Hard / Good / Easy của FSRS.

## Hệ quả

- Lịch ôn chính xác hơn SM-2, Learner cần ít lượt ôn hơn cho cùng độ nhớ.
- Trạng thái Card lưu theo mô hình FSRS (stability, difficulty, …) và lịch sử từng lượt ôn được giữ lại. Đổi thuật toán về sau cần chuyển đổi dữ liệu, nên quyết định này khó đảo ngược.
- Giữ lịch sử lượt ôn cho phép tối ưu tham số FSRS theo dữ liệu thật sau này.
