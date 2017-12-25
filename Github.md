# Github Guideline

## Cài đặt tài khoản

- Sử dụng tài khoản mail framgia để tạo tài khoản github
- Đặt tên account theo dạng oNguyenVanA
- Cài đặt public email
- Cài đặt company là @framgia

## Fork Repository

- Trước khi bắt đầu code cần fork repository về tài khoản github cá nhân
- Thêm remote là repository gốc, tên remote có thể dùng tên khách hàng nếu dùng github của khách hàng, hoặc có thể dùng là upstream nếu do framgia tạo
```sh
git remote add [Tên_khách_hàng or Upstream] https://github.com/...
```
Ví dụ:
```sh
git remote add upstream https://github.com/abc
```

## Quy tắc tạo branch

- Luôn checkout về master branch trước khi tạo branch mới
- Lấy source code mới nhất từ upstream về local master
- Tạo branch mới với quy tắc như sau:
> oNguyenVanA_[Ticket_Number]

Trong đó Ticket_Number là ticket number trong redmine. Ví dụ
> oNguyenVanA_12345

## Quy tắc commit

- Trong một pull request có thể có nhiều commit, mỗi commit là một nội dung sửa của pull request đó. Ví dụ pull request cần commit cả resource và sửa logic thì tách thành 2 commmit, 1 commit chứa resources và 1 commit chứa nội dung sửa logic
- Title của commit message theo quy tắc sau:
  - Format: 
> [Bug/Task/Feature #Ticket_Number] Nội_dung_sửa
  - Độ dài commit message không quá 72 ký tự

  Trong đó Bug/Task/Feature theo redmine, Ticket_Number là ticket number trong redmine, Nội_dung_sửa viết một cách ngắn gọn nội dung của pull request. Ví dụ:
  > [Bug #12345] Sửa lỗi navigation bar
  - Trong trường hợp nội dung dài thì sẽ viết thành nhiều dòng. Dòng đầu tiên vẫn theo format như trên, dòng tiếp theo là dòng trắng, các dòng tiếp theo nữa là mô tả về nội dung sửa. Có thể sử dụng gạch đầu dòng hay hoa thị đầu các dòng này.
  Ví dụ:
> [Bug #12345] Fix bug
> 
> - Sửa lỗi các buttons trong toolbar lệch trái
> - Sửa lỗi các buttons trong navigation bar lệch trái

## Quy tắc tạo pull request

- Sử dụng phần title trong commit message hoặc title trong ticket redmine làm title của pull request theo format như sau
> [Bug/Task/Feature #Ticket_Number] Nội_dung_sửa

Ví dụ
> [Bug #12345] Sửa lỗi các buttons trên navigation bar bị lệch trái

- Nội dung pull request

Copy link ticket redmine đặt vào nội dung pull request