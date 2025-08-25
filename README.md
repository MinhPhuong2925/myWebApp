# Chương 1: Giới thiệu về PHP và Laravel Khoa Coursera (Khoa 1):

https://www.coursera.org/leam/laravel-frameworkand-php Module 1:

 ## 1.1 Giới thiệu PHP

PHP (Hypertext Preprocessor) là ngôn ngữ lập trình kịch bản phía server (server-side scripting language).
Được dùng chủ yếu để phát triển ứng dụng web.
PHP có thể nhúng trực tiếp vào HTML.
Chạy trên nhiều hệ điều hành (Windows, Linux, macOS) và hỗ trợ nhiều máy chủ web (Apache, Nginx…).
Dễ học, cú pháp gần với C, Java.

 ## 1.2 Cú pháp PHP

+ Code PHP bắt đầu bằng <?php và kết thúc bằng ?>.
```
<?php
  echo "Xin chào, đây là trang PHP đầu tiên!";
?>
```

+ Có biến (bắt đầu bằng $).
+ Câu lệnh kết thúc bằng dấu ;.
```
$ten = "Phenikaa";
```
Chú thích:

+ Một dòng: // đây là chú thích
+ Nhiều dòng: /* chú thích nhiều dòng */

  ```
  //đây là chú thích một dòng
  /*
   * đây là chú thích nhiều dòng
   */
  
  ```
Có thể viết trong file .php hoặc nhúng vào HTML.

Ví dụ:
---
<!DOCTYPE html>
<html>
<body>
  <h1>Ví dụ PHP</h1>
  <?php
    $name = "Minh Phương";
    $age = 20;
    echo "Xin chào $name. Bạn $age tuổi.";
  ?>
</body>
</html>
---

  ## 1.3 Cấu trúc điều khiển


// Câu lệnh rẽ nhánh:
```
$diem = 8;
if ($diem >= 9) {
    echo "Xuất sắc";
} elseif ($diem >= 7) {
    echo "Khá";
} else {
    echo "Trung bình";
}
```

// Vòng lặp for:
```
for ($i = 1; $i <= 5; $i++) {
    echo "Số: $i <br>";
}
```

// Vòng lặp while
```
$i = 1;
while ($i <= 3) {
    echo "Hello $i <br>";
    $i++;
}

// do...while
```
$i = 0;
do {
  echo $i;
  $i++;
}
while ($i < 5);
```

//Rẽ nhanh switch..case

switch...case: 
```
$ngay = "thu hai";
switch ($ngay)
{ case "thu hai":
  echo "Hôm nay là đầu tuần.";
  break;

  case "thu ba":
  echo "Hôm nay là thứ 3.";
  break;

  default: echo "Không rõ ngày.";
}

```

  ## 1.4 Hàm

Hàm dùng để tái sử dụng code.
Được khai báo bằng function.
Có thể có tham số và giá trị trả về.


Ví dụ:

function tinhTong($a, $b) {
    return $a + $b;
}

echo tinhTong(5, 7); // Kết quả: 12

PHP có nhiều hàm dựng sẵn (built-in functions):

strlen("abc") → Độ dài chuỗi.

date("Y-m-d") → Lấy ngày tháng năm.

count($array) → Đếm số phần tử mảng.




---

  ## 1.5 Vai trò của PHP trong phát triển ứng dụng web

Xử lý động dữ liệu: PHP nhận dữ liệu từ người dùng (form HTML), xử lý và trả kết quả.

Kết nối cơ sở dữ liệu: Tích hợp dễ dàng với MySQL, MariaDB, PostgreSQL.

Xây dựng hệ thống web lớn:

Laravel (framework của PHP) giúp viết code nhanh, an toàn, dễ bảo trì.

PHP là nền tảng của nhiều CMS: WordPress, Joomla, Drupal.


Ưu điểm: miễn phí, cộng đồng lớn, tài liệu phong phú.


Ví dụ: Xử lý form đơn giản

<form method="post">
  Nhập tên: <input type="text" name="ten">
  <input type="submit" value="Gửi">
</form>

<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $ten = $_POST["ten"];
    echo "Xin chào, $ten!";
}
?>


---
