---
title: Chia sẻ cách tạo blog đơn giản và đẹp
date: 2024-04-23 15:00:00 +0700
categories: ["Blog"]
tags: ["Blog"]
---

# Chào bạn

Đôi khi bạn thích có 1 blog riêng, để chia sẻ những điều bạn muốn, nhưng bạn không biết bắt đầu từ đâu. Hôm nay mình sẽ hướng dẫn bạn cách tạo blog đơn giản và đẹp.

## Bước 1: Tạo tài khoản Github
- Truy cập vào trang chủ của Github: [github]
- Đăng ký tài khoản Github ([sign up for Github]), làm theo các bước hướng dẫn.
- Đăng nhập vào tài khoản Github. ([sign in to Github])

## Bước 2: Truy cập vào Repositories để tạo blog
- Truy cập vào [repositories] sau.
- Click vào nút `Use this template` để tạo blog.
- Đặt tên cho blog của bạn, sau đó click vào nút `Create repository from template`.
- Chờ 1 chút, blog của bạn đã được tạo thành công.

## Bước 3: Chỉnh sửa thông tin blog
- Tải repository về máy tính của bạn. Click vào nút `Code` -> `Download ZIP`.
- Giải nén file vừa tải về, mở thư mục blog bằng Visual Studio Code.
- Tải và cài đặt [Visual Studio Code](https://code.visualstudio.com/).
- Mở Visual Studio Code, click vào File -> Open Folder, chọn thư mục blog vừa tạo.
- Click vào file `_config.yml` để chỉnh sửa thông tin blog.
- Các thông tin cần chỉnh sửa:
  - `title`: Tiêu đề blog.
  - `description`: Mô tả blog.
  - `url`: Địa chỉ blog của bạn.
  - `baseurl`: Thư mục chứa blog.
  - `avatar`: Ảnh đại diện của bạn.
  - `name`: Tên của bạn.
  - `email`: Email của bạn.
  - `bio`: Giới thiệu về bạn. 
  - `twitter_username`: Tên tài khoản Twitter của bạn.
  - `github_username`: Tên tài khoản Github của bạn.
  - `linkedin_username`: Tên tài khoản Linkedin của bạn.

## Bước 4: Đăng bài viết
- Click vào thư mục `_posts`, sau đó click vào nút `Add file` -> `Create new file`.
- Đặt tên file theo định dạng `yyyy-mm-dd-title.md`.
- Copy nội dung bài viết vào file vừa tạo.
- Click vào nút `Commit new file` để lưu bài viết.
- Chờ 1 chút, bài viết của bạn đã được đăng thành công.

## Bước 5: Deploy blog sử dụng vercel
- Truy cập vào trang chủ của Vercel: [vercel](https://vercel.com/).
- Đăng nhập vào tài khoản Vercel, sử dụng tài khoản github mà bạn đã đăng ký ở bước 1.
- Click vào nút `Import project`, chọn repository blog của bạn.
- Chờ 1 chút, blog của bạn đã được deploy thành công.

## Kết luận
- Đến đây, bạn đã tạo thành công blog của mình. Chúc mừng bạn. Chúc bạn có những trải nghiệm tuyệt vời khi sử dụng blog của mình

Và mình là [diepchiaser], cảm ơn bạn đã đọc bài viết này.

[github]: https://github.com/
[sign up for Github]: https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home
[sign in to Github]: https://github.com/login
[repositories]: https://github.com/cotes2020/chirpy-starter
[diepchiaser]: https://chiaser.vercel.app/
