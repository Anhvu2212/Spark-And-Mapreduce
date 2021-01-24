# Spark-And-Mapreduce

TỒNG QUAN VỀ "SPARK"
 ![SPARK](https://www.onlinebooksreview.com/uploads/blog_images/2017/11/27_file.png)

Apache Spark là một open source cluster computing framework được phát triển sơ khởi vào năm 2009 bởi AMPLab tại đại học California, Berkeley. Sau này, Spark đã được trao cho Apache Software Foundation vào năm 2013 và được phát triển cho đến nay.

Spark cho phép xây dựng và phân tích nhanh các mô hình dự đoán. Hơn nữa, nó còn cung cấp khả năng truy xuất toàn bộ dữ liệu cùng lúc, nhờ vậy ta không cần phải lấy mẫu dữ liệu – đòi hỏi bởi các ngôn ngữ lập trình như R. Thêm vào đó, Spark còn cung cấp tính năng streaming, được dùng để xây dựng các mô hình real-time bằng cách nạp toàn bộ dữ liệu vào bộ nhớ.

Khi ta có một tác vụ nào đó qúa lớn mà không thể xử lý trên một laptop hay một server, Spark cho phép ta phân chia tác vụ này thành những phần dễ quản lý hơn. Sau đó, Spark sẽ chạy các tác vụ này trong bộ nhớ, trên các cluster của nhiều server khác nhau để khai thác tốc độ truy xuất nhanh từ RAM. Spark sử dụng API Resilient Distributed Dataset (RDD) để xử lý dữ liệu.

Spark nhận được nhiều sự hưởng ứng từ cộng đồng Big data trên thế giới do cung cấp khả năng tính toán nhanh và nhiều thư viện đi kèm hữu ích như Spark SQL (với kiểu dữ liệu DataFrames), Spark Streaming, MLlib (machine learning: classification, regression, clustering, collaborative filtering, và dimensionality reduction) và GraphX (biểu diễn đồ thị nhờ kết qủa tính toán song song).

![SPARK](https://scontent.fsgn5-4.fna.fbcdn.net/v/t1.0-9/92214447_2562652790634293_8507872163703816192_n.jpg?_nc_cat=102&ccb=2&_nc_sid=32a93c&_nc_ohc=AKgy3-yiYXoAX8JWKGY&_nc_ht=scontent.fsgn5-4.fna&oh=75c81ee202517f59cb6513bb652d9f55&oe=60334B74)

NHỮNG ƯU ĐIỂM:

Sự đơn giản: Một trong những chỉ trích thường gặp ở Hadoop đó là sự phức tạp trong qúa trình phát triển, mặc dù đây là một trong những phương pháp tính toán đơn gỉan và hiệu qủa gíup tăng tốc độ xử lý của hệ thống. Thay vì đòi hỏi người dùng phải hiểu rạch ròi về MapReduce và lập trình Java, Spark sinh ra để gíup mọi người tiếp cận với công nghệ tính toán song song dễ dàng hơn rất nhiều. Người dùng chỉ cần một vài kiến thức cơ bản về database cộng với lập trình Python hay Scala là có thể sử dụng được.

Độc lập với các nhà cung cấp dịch vụ Hadoop: Hầu hết các nhà cung cấp dịch vụ Hadoop đều hỗ trợ Spark. Điều này có nghĩa Spark không phụ thuộc vào các nhà cung cấp này. Nếu bạn muốn thay đổi nhà cung cấp dịch vụ, ta chỉ cần đem hệ thống Spark qua nhà cung cấp mới mà không lo ngại việc mất mát thông tin.


TỒNG QUAN VỀ "MAPREDUCE"

1.Map reduce là gì?
Mapreduce có thể hiểu là 1 phương thức thực thi để giúp các ứng dụng có thể xử lý nhanh 1 lượng dữ liệu lớn. Các dữ liệu này được đặt tại các máy tính phân tán.Các máy tính này sẽ hoạt động song song độc lập với nhau.Điều này làm rút ngẵn thời gian xử lý toàn bộ dữ liệu

Một đặc điểm đáng chú ý của Mapreduce là dữ liệu đầu vào có thể là dữ liệu có cấu trúc ( dữ liệu lưu trữ dạng bảng quan hệ 2 chiều ) hoặc dữ liệu không cấu trúc ( dữ liệu dạng tập tin hệ thống )

Các máy tính lưu trữ các dữ liệu phân tán trong quá trình thực thi được gọi là các nút (nodes) của hệ thống.Nếu các máy tính này cùng sử dụng chung trên 1 phần cứng thì chúng được gọi là 1 cụm ( Cluster ).Nếu các máy này hoatj động riêng rẽ trên các phần cứng khác nhau thì chúng được gọi là 1 lưới (Grid)

2.Ưu điểm của mapreduce
Xử lý tốt bài toán về lượng dữ liệu lớn có các tác vụ phân tích và tính toán phức tạn không lướng trước được

Có thể tiến hành chạy song song trên các máy phân tán 1 cahs chính xác và hiệu quả.Không phải quan tâm đến sự trao đổi dữ liệu giữa các clusters với nhau vì chúng hoạt động 1 cách đọc lập, không phải theo dõi xử lý các tác vụ,xủa lý lỗi.

Có thể thực hiên mô hình Mapreduce trên nhiều ngôn ngữ (Java,C++,Python,Perl,Ruby,C) với các thư viện tương ứng

3.Nguyên tắc hoạt động của Mapreduce
Mapreduce hoạt dộng gồm 2 quá trình thực hiện 2 hàm "Map" và "Reduce"

Ý tưởng chính của Mapreduce chính là thực hiện việc "Chia để trị"
  -Chia vấn đề cần xử lý (dữ liệu ) thành các phàn nhỏ để xử lý
  -Xử lý các vấn đề nhỏ đó 1 cách song song trên các máy tính phân tán hoạt động đọc lập
  -Tông hợp các kết quả thu được để đưa ra kết quả cuối cùng
  
Như vậy toàn bộ quá trình mapreduce có thể hiểu như sau
  -Đọc dữ liệu đầu vào
  -Thực hiên xử lý các phần dữ liệu vào (xử lý từng phấn một ) (Thực hiện hàm Map)
  -Trộn và sắp xếp các kết quả thu được từ các máy tính làm sao để được kết quả tiện lợi nhất so với mục đích của quá trình
  -Tổng hợp các kết quả trung gian thu được từ các máy tính phân tán (Thực hiện hàm reduce)
   -Đưa ra kết quả cuối cùng
   
Sơ đồ hoạt đọng của quá trình Mapreduce:

![SPARK](https://blog.itnavi.com.vn/wp-content/uploads/2020/06/Mapreduce-l%C3%A0-g%C3%AC-4.jpg)
