--- 
layout: post 
title: "2026-08-15 [APM구현]php에서-mysql-데이터베이스-연결" 
categories: [WebDev] 
tags: [php,mysql] 
--- 
 
# [APM구현]php에서-mysql-데이터베이스-연결 
 
[공식 홈페이지 참조](https://www.php.net/manual/en/book.mysqli.php)
[숏텀 PHP - PHP 윈도우 실행환경 참고](https://wikidocs.net/271931)

php.ini에서
```ini
;extension=mysqli
```
주석 처리 풀기

```php
<?php
$conn = new mysqli("localhost", "user_id", "user_password", "test");
if ($conn->connect_error) {
    die("연결 실패: " . $conn->connect_error);
}
echo "연결 성공!";
```
<span style='color: red'>mysqli 값은 보여지면 안됩니다.
해당 값의 경우 따로 파일을 관리해야하고 git에서 ignore처리 해야합니다.</span>
추후 처리하는 방법 알아보기


```php
$result = $conn->query("SELECT id from user");
$row = $result->fetch_assoc();
echo $row['id'];
```

```text
admin
```