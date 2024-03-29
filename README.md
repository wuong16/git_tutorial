# git_tutorial

# Sử Dụng Git/GitHub Từ Cơ Bản Đến Nâng Cao
## Các bạn làm việc liên quan đến lập trình đều được nghe rất nhiều về Git hay Github nhưng không hiểu nó là gì, nó thần thánh ra sao, hỗ trợ các bạn trong công việc thế nào. Trong loạt bài viết này mình sẽ hướng dẫn cho các bạn những hiểu biết cơ bản nhất về Git và Github.
### Tại sao nên dùng Git/GitHub?
Hầu hết khi hỏi các bạn sinh viên làm bài tập lớn theo nhóm, mỗi bạn code 1 phần vậy khi ghép lại thành 1 project hoàn chỉnh thì sẽ làm như thế nào?

Phần lớn các bạn đều trả lời rằng: "Bọn em sẽ lên thư viện hoặc hẹn nhau ở chỗ nào đó cùng nhau ghép hoặc copy gửi cho nhau" cũng có trường hợp "Có thằng nó gánh team rồi, em chỉ cần làm tài liệu thôi :D"

Thực trạng trên cho thấy rằng đa số các bạn sinh viên mới ra trường, chưa có kinh nghiệm làm việc nhiều nên hầu hết các bạn này rất lúng túng khi làm việc với Git hoặc thậm chí có bạn còn chưa biết Git là gì, chưa biết làm việc với nó như thế nào. Trên quan điểm của mình, việc này không phải lỗi của bạn ấy, chẳng qua các bạn ấy chưa có cơ hội để sử dụng Git, nên chưa tìm hiểu. Nhưng, sẽ là lỗi của các bạn ấy, nếu trong dự án sử dụng Git mà lại không tìm hiểu.

Vừa qua mình cũng có nhận training cho 1 vài bạn thực tập sinh và cũng xảy ra tình trạng tương tự như trên. Vì vậy qua đây mình xin chia sẻ một số hiểu biết của mình (đã từng tìm hiểu và đã từng làm) về Git trong bài viết này với hy vọng sẽ giúp ích được những bạn tự tin khi làm việc với Git cũng như nâng cao kỹ năng của bản thân trên con đường trở thành lập trình viên chuyên nghiệp.
### 1. Git là gì?
Git là một hệ thống quản lý phiên bản phân tán (Distributed Version Control System). Hiểu nôm na rằng Git là 1 hệ thống giúp cho việc quản lý tài liệu, source code... của 1 nhóm các developer cùng làm chung dự án. Git sẽ ghi nhớ lại toàn bộ lịch sử thay đổi của source code trong dự án. Bạn sửa file nào, thêm dòng code nào, xóa dòng code nào, bỏ thừa dấu ở đâu... tất cả các hành động đều được Git ghi lại. Qua đó giúp dự án có thể điều tra nguyên nhân gây lỗi hệ thống, tổng hợp code trở nên dễ dàng hơn.
### 2. Hướng dẫn sử dụng Git
Trước khi đi vào sử dụng git ta cần hiểu một số khái niệm liên quan đến Git như sau:

Repository: Repository hiểu đơn giản nó chính là cái kho lưu trữ tất cả những thông tin cần thiết để quản lý các sửa đổi và lịch sử của toàn bộ project. Repository của Git được phân thành 2 loại là remote repository và local repository.

- Local Repository: là repository nằm trên chính máy tính của chúng ta, repository này sẽ đồng bộ hóa với remote repository bằng các lệnh của git.
- Remote Repository: là repository được cài đặt trên server chuyên dụng. Ví dụ: GitHub, GitLab, Bitbucket,...
=> GitHub chính là 1 Remote Repository lưu trữ tất cả những thông tin cần thiết để quản lý các sửa đổi và lịch sử của toàn bộ project.

Working tree và Index (hoặc staging area): Là những thư mục được đặt trong sự quản lý của Git, nơi mọi người thực hiện công việc trên đó, được gọi là working tree. Giữa repository và working tree tồn tại một nơi gọi là index hay staging area . staging area là nơi để chuẩn bị cho việc commit vào repository.

Bắt tay vào cài đặt nào!!!

Để cài đặt Git, các bạn chỉ cần download Git về và Next => Next =>... => Finish là xong (Đối với máy windows). Chi tiết các bạn có thể tham khảo thêm ở link sau: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

Sau khi cài đặt xong chúng ta bắt tay vào làm thôi. Trong phần 1 này mình sẽ trình bày một số câu lệnh cơ bản, thao tác với local repository trước (chưa cần tạo tài khoản github vội) để chúng ta vừa hiểu lý thuyết lại làm thực hành luôn cho nhớ nha :D
#### 2.1 Lệnh:  git init
Tác dụng : Khởi tạo 1 git repository 1 project mới hoặc đã có.

Cách dùng: Tạo 1 folder mới => vào trong folder đó => click chuột phải chọn Git Bash Here như hình dưới

Cửa sổ console git bash hiện lên => các bạn gõ lệnh git init 

Sau khi tạo thành công thì trong folder sẽ xuất hiện folder .git => folder này sẽ chứa tất cả những thông tin cần thiết để quản lý các sửa đổi và lịch sử của toàn bộ project. Vậy nên nếu muốn xóa file này hãy cân nhắc trước khi xóa nhé :D

#### 2.2 Lệnh : git add
Tác dụng : Thêm thay đổi vào stage/index trong thư mục làm việc.

Cách dùng: Tại thư mục làm việc => git add .

Khi add thành công
#### 2.3 Lệnh: git commit
Tác dụng: commit là một action để Git lưu lại các sự thay đổi trong thư mục làm việc vào repository

Cách dùng: git commit -m " add source nhaaaaaa"

Khi commit thành công
## Tạm kết
Vậy là trong phần 1 này mình đã chia sẻ kiến thức cơ bản để sử dụng được git và thực hành tạo local repository với các lệnh cơ bản, trong phần tiếp theo mình sẽ chia sẻ thêm các kiến thức nâng cao về merge, branch, resolve conflict... cũng như cách sử dụng GitHub. Mọi người tiếp tục theo dõi nha

Tài liệu tham khảo: https://git-scm.com/doc
