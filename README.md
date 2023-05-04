# De_makeup_and_Super_resolution_Muilti_task_Learning
Trong project này chúng ta cũng sẽ thử nghiệm multi-task learning bằng cách thực hiện thêm một task thứ hai là Super Resolution task, model nhận input là một ảnh và output ra ảnh input với size tăng 4 lần. Như vậy ta sẽ có một multi-task model gồm hai task De-makeup và Super Resolution.
Gần đây Multi-task learning cũng là một hướng nghiên cứu được chú ý với ý tưởng là nếu chỉ học một task cụ thể thì đôi khi model có thể sẽ chỉ tập trung vào các thông tin task chính mà bỏ qua những thông tin hữu ích khác có thể giúp model học tốt hơn. Do đó nếu model học thêm các task khác có thể bổ sung tri thức (các thông tin này) liên quan giữa các task giúp cải thiện performance của model.
Dataset này sẽ sử dụng GAN để tạo ra de-makeup data (sẽ có ảnh makeup tốt và makeup tệ) do đó project sẽ được xem nhưu loại bỏ makeup là tốt hay tệ để khôi phục lại gương mặt trước khi makeup.

Có 3 mục tiêu trong project này:
1. Thực hiện demak-up task bằng cách xây dựng một model dựa trên kiến trúc Unet với encoder là ResNet34 và không dùng skip connection giữa encoder và decoder.
2. Thực hiện demak-up task bằng cách xây dựng một model dựa trên kiến trúc Unet với encoder là ResNet34 và có dùng skip connection giữa encoder và decoder.
3. Thực hiện mutitask-learning với hai task là demak-up và super resolution task bằng cách xây dựng một model dựa  trên kiến trúc Unet với encoder là ResNet34 và có dùng skip connection giữa encoder và decoder. Đồn thời mở rộng output của decoder để thực hiện được cả hai task đồng thời.
