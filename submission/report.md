1. Tôi dùng AWS, ap-southeast-2 (Sydney), t3.medium, source commit mới nhất.
2. Dataset có 284,807 dòng, chia train/validation/test 60/20/20 cùng phân bố Class, seed 16.
3. Load dữ liệu mất 2.34 giây; training mất 3.48 giây; best iteration là 68.
4. AUC 0.9768, Accuracy 0.9995, F1 0.8478, Precision 0.9070, Recall 0.7959 trên tập test.
5. Latency 1 dòng 1.19 ms; throughput batch 1.000 dòng 322,757 dòng/giây; đo bằng median của predict_proba.
6. CPU/RAM/Network tôi quan sát lúc benchmark xong là: CPU nhàn rỗi 99%, RAM dư 1.8GB, Network nhận ~277MB; ảnh đính kèm.
7. Billing ghi nhận "Data unavailable" do độ trễ hiển thị của AWS; ước tính chi phí $0.10/giờ.
8. Tôi đã tải kết quả, copy mã nguồn và tiến hành chạy lệnh destroy tài nguyên.
