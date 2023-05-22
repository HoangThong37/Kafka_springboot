# Kafka_springboot
Learn Kafka_springboot basic

### Kafka là gì?
Kafka là một nền tảng message publish/subscribe phân tán (distributed messaging system) mã nguồn mở được xây dựng nhằm mục đích xử lý dữ liệu streaming theo thời gian thực.

### Một số khái niệm cơ bản trong Kafka
Để làm việc với Kafka, các bạn cần nắm một số khái niệm cơ bản về:

#### 1. Producer

Producer là những application produce data và gửi data tới Kafka Server. Data này sẽ là những message có định dạng, được gửi dưới dạng mảng byte tới Kafka server. 
Ví dụ như các bạn có một tập tin .txt chứa text bên trong, chúng ta có thể dùng Producer để đọc từng dòng trong tập tin này rồi gửi tới Kafka server.

#### 2. Consumer

Kafka sử dụng consumer để subscribe vào topic, các consumer được định danh bằng các group name. Nhiều consumer có thể cùng đọc một topic. Sau khi nhận được data, Consumer có thể thêm code để xử lý data theo nhu cầu của mình.

#### 3. Cluster

Kafka cluster là một set các server, mỗi một set này được gọi là 1 broker.

#### 4. Broker

Broker là Kafka server, là cầu nối giữa Message Publisher và Message Consumer, giúp chúng có thể trao đổi message với nhau.

#### 5. Topic

Dữ liệu truyền trong Kafka theo topic, khi cần truyền dữ liệu cho các ứng dụng khác nhau thì sẽ tạo ra các topic khác nhau.

#### 6. Partitions

Kafka là một distributed messaging system và chúng ta có thể setup Kafka server với cluster. Trong trường hợp một topic nhận quá nhiều message tại cùng một thời điểm, chúng ta có thể chia topic này thành những partitions được share giữa các Kafka server với nhau trong một cluster được handle các message này.

Một partition sẽ small và independent với các partitions khác. Số lượng partition cho mỗi topic thì tuỳ theo nhu cầu của ứng dụng mà chúng ta có thể quyết định.

#### 7. Consumer Group

Consumer group là một group các Consumer consume message từ Kafka server. Mỗi một Consumer Group sẽ share với nhau việc handle message.

#### 8. ZOOKEEPER: được dùng để quản lý và bố trí các broker.
