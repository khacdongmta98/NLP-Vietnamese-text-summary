# text-summarization-with-kmeans
This project can help us summary Vietnamese text automatically. We use word2vec technique to vectorize every sentences in input and use K-Means Clustering to cluster these vectors.
----
Bài toán được xử lý làm 2 hướng:
--Hướng 1: Sử dụng pre-train model w2v đã được train sẵn với tiếng việt 
           link download: https://github.com/sonvx/word2vecVN
           Tóm tắt văn bản vừa sử dụng model w2v với K-means, hierarchical clustering 
           => kết quả: sub_text1
--Hướng 2: Sử dụng bộ dữ liệu VNTC để train lại model w2v 
           Sử dụng model vừa train với văn bản đầu vào
           Tóm tắt với K-means,hierarchical clustering
           => Kết quả: sub_text2
--So sánh sub_text1 và sub_text2 để xem kết quả nào tốt hơn 

Processing:
--Load data: VNTC-- train_full and test_full
--pre-procesing data
--train model w2v 
--using model w2v for input_text
--K-means with input_text
--compare result 
............
Một số câu hỏi đặt ra khi giải quyết bài toán: 
1. Tại sao lại lựa chọn vector 128 chiều ?
2. Model word2vec sử dụng hoạt động như nào ? mục đích để làm gì?
3. Tách câu như nào ? thư viện đó hoạt động như nào ?
4. vector hóa từ => vector hóa câu như nào ? mục đích làm gì ?
5. Đánh trọng số các câu như nào ? 
6. chuẩn hóa unicode tổ hợp, chuẩn hóa dấu câu, tách từ ( bộ tokenizer của VN Core NPL) , loại bỏ stop words, rare words
7. đánh giá mức độ chính xác so với văn bản ban đầu  


