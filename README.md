# Set tên wifi có chứa emoji (ví dụ trong bài là router chạy dd-wrt)
* điều kiện: dùng telnet hay ssh kết nối được với router
chạy lệnh sau:
```
nvram show | grep <tên ssid hiện tại>
```
* Sau khi chạy nó sẽ xuất ra thông tin dạng như sau:
```
wlan0_ssid=⭐P0430⭐
```
* Khi này, ta dùng lệnh sau:
```
nvram set wlan0_ssid="<hangulSSID>"
```
và reboot lại router bằng lệnh
```
reboot
```
**chú ý**: dòng **wlan0_ssid** có thể thay đổi tùy vào interface của từng router, hãy chạy lệnh **nvram** ở trên để kiểm tra.
