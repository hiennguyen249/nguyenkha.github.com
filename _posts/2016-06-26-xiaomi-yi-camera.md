---
layout: post
title: Xiaomi Yi Camera
categories:
- blog
---

Vì vài lý do nên mình quyết định chọn mua một con IP camera nhỏ nhỏ, rẻ rẻ để lắp ở nhà. Thấy trên mạng con của Xiaomi được nhiều người biết đến nên quyết định mua trên Lazada, giá sau khi dùng các mã khuyến mãi là 500k, với mình thì hợp lý. Với mình nghĩ thì nó chỉ là một cái camera đơn giản thôi, nhưng thật với con số 500k thì nó mang lại nhiều "kinh nghiệm xương máu"... Các vấn đề như sau:

Vấn đề 1: Quốc tế hay Trung Quốc 
================================

Phiên bản mình mua là phiên bản CHỈ DÀNH cho thị trường Trung Quốc, nghĩa là nếu KHÔNG có thay đổi gì trên firmware thì sẽ không dùng được ngoài TQ. May đứa bán đã cài sẵn firmware được "mod" nên xài được ở nước ngoài. Mình xin tạm không bàn về tính hợp pháp giấy phép đối với người dùng cuối (EULA), tương tự với iPhone lock mạng hay jailbreak/root điện thoại vì mỗi lúc mỗi khác, và quan điểm của mình, mình có toàn quyền sử dụng với phần cứng thuộc sở hữu của mình.

Vấn đề 2: Mi Home hay YI Home
=============================

Vừa bắt đầu các bước cài đặt mình đã gặp ngay vấn đề không kết nối được với wifi... Mình không thể nào gõ password sai cả chục lận được. Thế là google, hóa ra là bản Yi TQ thì phải dùng Mi Home và quốc tế thì dùng YI Home... Cứ incorrect password quài bực cả mình.

Vấn đề 3: Nâng cấp firmware
===========================

Các bài này học quài chưa thuộc: **PHẢI TÌM HIỂU THẬT KỸ TRƯỚC KHI ĐỤNG ĐẾN FIRMWARE**. Thế là dại dại ấn nút update firmware... Tèn tèn, khởi động lại, cái camera cứ la làng... Cái cục này chỉ sử dụng được ở Trung Quốc... Thôi teo, sao giờ, má biết giết mình chết vì quăng 500k qua cửa sổ. Lật đật google, kêu, cập nhật là firmware cũ hơn. Thế là lấy thẻ nhớ ra, download 1 cái firmware cũ cũ về. Tèn ten, bắt đầu chuyển sang nói chuyện bằng tiếng TQ, mà mình thì ứ hiểu gì. Thôi kệ, miễn sao xài được là được, hy vọng thế... Rồi, lại wifi connect không được, thử các kiểu phiên bản firmware cũng không được... Thôi rồi...

Bắt đầu mò mẫm, đọc thử [yi-hack](https://github.com/fritz-smh/yi-hack/tree/master/sd/test). Mới dần hiểu ra còn Yi thực chất tương tự như 1 con Pi, chắc là cũng là ARM (yếu + sensor hình ảnh) chạy Linux (Hilinux). Nó có một điểm mở là đặt 1 file script .sh lên thư mục /home/hd1/test/equip_test.sh thì nó sẽ chạy file đó đầu tiên khi khởi động, cho phép can thiệp hay sửa chữa hệ thống. Bắt đầu cứ sửa file script cho nó chạy thử kết nối wifi xem tại sao không được. Chắc rút ra máy tính cắm vô còn Yi gần trăm lần, cuối cùng phát hiện ra... Không thấy card mạng wifi. Quái, chả lẽ hư phần cứng rồi sao? Thế là quăng à???

Say khi suy nghĩ lại thì thấy, có thể do driver không tương thích phần cứng. Mấy cái firmware mình xài cũng cũng rồi mà. Ráng lục trí nhớ lại xem cái firmware mình xài trước khi update là gì? Cuối cùng cũng ra được 1.8.6.1B gì gì đó. Google cái ra ngay 1 trang tiếng Việt, chỉ qua một trang tiếng Nga nói anh Nga ngố đã mod bản này. Download về update ngay, thế là boot lên là thấy y chang như cũ rồi. Yeah yeah!!!

Cài lại xong giờ coi lại bản mod này đã bao gồm sẵn các sửa chữa. Nhưng tốt nhất bạn vẫn nên set lại root password, kẻo rước họa vào nhà nhé ;). Con Yi này chắc còn nhiều trò để chơi đây haha :)). Nhiều khi mình cũng chả rảnh để mò nó, nhưng tình huống bắt buộc :))