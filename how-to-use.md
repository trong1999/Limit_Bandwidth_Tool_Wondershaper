## Giới hạn băng thông bằng cách nào
- Giới hạn số lượng băng thông download bằng cách
 + **$ wondershaper -a ens09 -d 4048**
 + Với các options: **-a** để định nghĩa interface, với **-d** để xác định đối tượng cần limit, **4048** định lượng số Kbps
cần được limit.
 + **$ wondershaper -a ens09 -u 2024**
 + Tương tự thì **-u** sẽ option upload.
- Ngoài ra còn có thể cài đặt hai options trên một command line
 + **$ wondershaper -a ens09 -d 4048 -u 1048**
- Để xem current status thì sẽ chọn option **-s** (status)
 + **$ wondershaper -sa ens09** 
- Nếu sau một thời gian bạn muốn bỏ việc giới hạn băng thông thì bạn chỉ cần lựa chọn option **-c** (clear)
 + **$ wondershaper -ca ens09**
## Cách thứ 2 là set rate trong file configure của Wondershaper.
- ** /etc/conf.d/wondershaper**
 + [wondershaper]
 + #/ Adapter
 + IFACE="ens09"

 + #/ Download rate in Kbps
 + DSPEED="4048"

 + #/ Upload rate in Kbps
 + USPEED="2024"

- Sau khi configure xong thì cần restart lại wondershaper.
## Qua blog này chúng ta có hiểu hơn về wondershaper và cách cài đặt cũng như cách sử dụng nó, chúc bạn đọc th
