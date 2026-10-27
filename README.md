# Student Score Regression

Ứng dụng dự đoán điểm thi bằng hồi quy tuyến tính (scikit-learn), giao diện ipywidgets, chạy bằng Voilà và triển khai trên Render.

Dữ liệu là dữ liệu tổng hợp phục vụ giảng dạy. Không dùng mô hình này để đánh giá sinh viên thật.

## Chạy cục bộ

```bash
python -m venv .venv
source .venv/bin/activate        # Windows PowerShell: .venv\Scripts\Activate.ps1
pip install -r requirements.txt
python -m training.generate_data
python -m training.train_model
voila app.ipynb --no-browser --port=8866
```

## Triển khai

Render đọc `render.yaml`: cài `requirements.txt` và chạy Voilà với `$PORT`. Artifact `artifacts/linear_regression.joblib` được commit sẵn nên dịch vụ không huấn luyện lại khi khởi động.
