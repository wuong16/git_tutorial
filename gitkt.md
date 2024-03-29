# Kiên Trúc của GIT

Git là một hệ thống quản lý phiên bản phân tán (DVCS - Distributed Version Control System) được phát triển bởi Linus Torvalds vào năm 2005. Kiến trúc của Git bao gồm các thành phần cơ bản sau:
## Repository (Kho lưu trữ):
-Repository là nơi chứa dữ liệu và lịch sử thay đổi của dự án.

-Có hai loại repository: local repository (kho lưu trữ địa phương) và remote repository (kho lưu trữ từ xa).

-Local repository là thư mục mà bạn đang làm việc trên máy tính của mình, trong khi remote repository là nơi lưu trữ trên máy chủ từ xa
## Working Directory (Thư mục làm việc):

Thư mục làm việc là nơi mà bạn thực hiện công việc thay đổi các tệp và thư mục của dự án.
Các thay đổi được thực hiện trong thư mục làm việc sẽ không ảnh hưởng đến repository cho đến khi bạn thực hiện commit.

## Staging Area (Khu vực sắp xếp):

Khu vực sắp xếp là nơi mà các thay đổi được chuẩn bị để commit vào repository.
Trước khi commit, bạn cần thêm các tệp và thay đổi vào khu vực sắp xếp sử dụng lệnh git add.

## Commit (Bản ghi):

Một commit là một phiên bản của dự án tại một thời điểm nhất định.
Khi bạn commit, các thay đổi trong khu vực sắp xếp sẽ được lưu vào repository với một thông điệp commit đi kèm.

## Branches (Nhánh):

Branches cho phép bạn phát triển song song, mỗi nhánh đại diện cho một luồng công việc riêng.
Mỗi nhánh có thể chứa các commit khác nhau và được sử dụng để phát triển tính năng mới, sửa lỗi, hoặc thực hiện các nhiệm vụ khác mà không ảnh hưởng đến nhánh chính.
Git sử dụng một con trỏ đặc biệt gọi là HEAD để xác định nhánh hiện tại mà bạn đang làm việc.

## Merge (Hợp nhất):

Merge là quá trình kết hợp các thay đổi từ một nhánh vào nhánh hiện tại.
Khi bạn merge hai nhánh, Git sẽ cố gắng tự động hợp nhất các thay đổi, nhưng có thể xảy ra xung đột cần giải quyết thủ công.

## Remote (Từ xa):

Remote repositories là các bản sao của dự án trên các máy chủ từ xa, mà bạn có thể đồng bộ hóa với và chia sẻ thay đổi.
Phổ biến nhất là sử dụng remote repository để làm việc cộng tác với nhóm hoặc sao lưu dự án của bạn.