# DEMO
## Step 1
Khởi tạo Repository

Đầu tiên, chúng ta sẽ khởi tạo một repository mới. Mở terminal và di chuyển đến thư mục mà bạn muốn tạo repository. Sau đó chạy lệnh sau:
```sh
git init my_project
cd my_project
```
## Step 2
Thêm và Commit Tệp

Tiếp theo, hãy tạo một tệp mới trong thư mục của dự án và thêm nội dung vào đó. Chẳng hạn, tạo một tệp hello_world.txt và thêm vào đó một dòng văn bản:
```sh
echo "Hello, World!" > hello_world.txt
```
Sau đó, thêm tệp này vào khu vực sắp xếp và thực hiện commit:
```sh
git add hello_world.txt
git commit -m "Add hello world file"
```
## Step 3
Tạo và Sử Dụng Nhánh

Bây giờ, hãy tạo một nhánh mới và chuyển đến nó:

```sh
git branch feature_branch
git checkout feature_branch
```
Thêm một thay đổi vào tệp hello_world.txt, ví dụ:

```sh
echo "This is a feature branch change" >> hello_world.txt
```

Thêm và commit thay đổi:
```sh
git add hello_world.txt
git commit -m "Add feature branch change"
```
## Step 4
Merge Nhánh

Tiếp theo, chúng ta sẽ hợp nhất nhánh feature_branch vào nhánh chính (thường là master hoặc main):
```sh
git checkout master
git merge feature_branch
```
## Step 5
Đẩy Thay Đổi Lên Remote Repository

Nếu bạn đã liên kết repository local với một remote repository, bạn có thể đẩy các thay đổi lên remote repository. Đầu tiên, chắc chắn rằng bạn đã thêm remote repository:
```sh
git remote add origin <url_to_your_remote_repository>
```
Sau đó, đẩy các thay đổi lên remote repository:
```sh
git push -u origin master
```
Đây là một demo đơn giản về việc sử dụng Git để quản lý phiên bản của dự án. Để hiểu rõ hơn và làm quen với các tính năng và lệnh khác của Git, bạn có thể tham khảo tài liệu hướng dẫn hoặc các khóa học trực tuyến.