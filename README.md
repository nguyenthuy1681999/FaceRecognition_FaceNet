# FaceRecognition_FaceNet
-MTCNN nhận diện khuôn mặt, Keras FaceNet sẽ được sử dụng để tạo nhúng khuôn mặt cho từng khuôn mặt được phát hiện, sau đó mô hình phân loại Máy vectơ hỗ trợ tuyến tính (linear SVM) sẽ để dự đoán danh tính của một khuôn mặt nhất định:
+ Data gồm ảnh khuôn mặt của người tuy nhiên ảnh chưa được cắt sát phần mặt (vẫn còn thân người, áo, tay…). Sử dụng MTCNN để trích xuất khuôn mặt từ ảnh.
+ Tiến hành detect face cho tất cả các ảnh của mỗi folder và gán nhãn cho chúng. Cả tập train và val. Sau đó lưu toàn bộ dataset vào một file mảng NumPy nén data.npz.
+ Sử dụng dụng facenet từ facenet_keras để face embedding, lưu và nén vào file faces-embeddings.npz
+ Cuối cùng sử dụng Support vector machine kernel linear để dự đoán khuôn mặt, show kết quả gồm ảnh, nhãn dự đoán kèm xác suất.
