Bài tập lớn Big Data
===============================
Gợi ý phim sử dụng Collaborative Filtering
----------------------------------------------------

## Yêu cầu

- Python 2.7
- NodeJS 6 (Đánh giá hiệu năng)

## Cấu hình (config.json)

	{
		"train_name": "ml-1m/training-1.csv", 		// Đường dẫn tới tập training
		"separator": ",",							// Ký tự phân tách giữa các trường trong dữ liệu
		"test_name": "ml-1m/test-1.csv",			// Đường dẫn tới tập test
		"skip": false,								// Skip dòng đầu
		"lower_bound": 4,							// Ngưỡng chọn những bộ phim vào tập gợi ý
		"user_id": 4000,							// ID của user cần gợi ý phim
		"no_of_movies": 10,							// Số lượng phim gợi ý
		"sim": 1,									// Hàm đo độ tương tự: 0 - Cosine, 1 - Pearson
		"recommend": true							// false dùng trong trường hợp đánh giá hiệu năng
	}

## Chạy

Chia [dữ liệu](http://grouplens.org/datasets/movielens/20m/)

	$ python split_input.py

Gợi ý phim

	$ python user-view.py

Đánh giá hiệu năng (Chạy gợi ý với toàn bộ user)

	$ node analytic.js

