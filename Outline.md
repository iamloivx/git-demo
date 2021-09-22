# Vấn Đề Hiện Tại

- Chưa sử dụng SSH
- Chưa thực hành và sử dụng Git thành thạo (quản lý branch, tag, merge-branch)
- Chưa sử dụng công cụ hỗ trợ (merge code, diff code)

# Công Cụ Hỗ Trợ

- https://meldmerge.org
- http://kdiff3.sourceforge.net

# Thực Hành Git Khoa Học (Teamwork)

- Master (branch chính của project) luôn ở trong trạng thái stable (hạn chế push, commit trực tiếp trên branch master, chỉ sử dụng trong các trường hợp hot-fix)

- Branch - mỗi một branch sẽ tương ứng với một feature của project. Các thành viên trong cùng team nếu cùng làm liên quan tới một feature thì chỉ làm việc trên một branch (đôi khi các developer thường sợ việc xử lý conflict nên mỗi developer lại làm việc trên một branch riêng cho một feature => teamwork không cao và sinh ra nhiều branch khác nhau). Sau khi một feature được test và ổn định, sẽ merge branch này vào branch master.

- Sử dụng công cụ merger tool để hạn chế các lỗi phát sinh trong quá trình merge

- Không xóa file của người khác (nếu không sử dụng file này thì nên comment lại toàn bộ code của file). Nếu thực sự muốn xóa file, thì cần trao đổi trước với người viết file ấy.

- Hạn chế sử dụng công cụ pull của git (thông qua lệnh  git pull), thay vào đó sử dụng lệnh git fetch kết hợp với git merge (sau quá trình merge nếu xảy ra conflict thì sử dụng merge tool để xử lý conflict)
http://stackoverflow.com/questions/292357/what-are-the-differences-between-git-pull-and-git-fetch

- Sử dụng khoảng cách tab giống nhau giữa các thành viên (tránh việc người A dùng tab là 3 kí tự cách với người B dùng tab là 4 kí tự cách. Sử dụng khoảng cách tab khác nhau cũng có thể sinh ra conflict khi merge giữa các thành viên)

- Hạn chế sử dụng `commit -a`. Lệnh trên có thể tiện khi muốn commmit tất cả các thay đổi như sửa file, xóa file. Tuy nhiên, sử dụng nó cũng dễ gây ra những vấn đề phát sinh (mình xóa nhầm file, commit những file không mong muốn). Thay vì thế, chỉ nên chọn lựa và commit những file thực sự mình muốn commit.

# Demo

