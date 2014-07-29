# README

## Using MongoDB in Rails - NghiaMT

Sử dụng Mongoid để tích hợp MongoDB vào Rails (gem “mongoid”)

Sau khi bundle install xong thì chạy dòng lệnh sau đề config mongoid:

```rails generate mongoid:config```

Thay đổi database cleaner strategy từ transaction thành truncation trong file features/support/env.rb

```
-  DatabaseCleaner.strategy = :transaction
+  DatabaseCleaner.strategy = :truncation
```

Sau đó ta có thể thao tác với DB như bình thường.Ví dụ tạo 1 resources bằng scaffold:

```Ruby
rails generate scaffold product name description price:float
```
