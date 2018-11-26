Inventory là file xác định thông tin các remote host được áp dụng. 

Mặc định là file `/etc/ansible/hosts`. Cũng có thể chỉ định file inventory  `-i <path>`

Các host được phân theo các group, mỗi host có thể thuộc nhiều group. Có 2 group mặc định là `all` và `ungrouped`. `all` chứa tất cả các host, `ungrouped` chứa các host không thuộc group nào ngoài `all`.

Ví dụ:

Định dạng INI:

```
mail.example.com

[webservers]
foo.example.com
bar.example.com

[dbservers]
one.example.com
two.example.com
```

Định dạng YAML

```
all:
  hosts:
    mail.example.com:
  children:
    webservers:
      hosts:
        foo.example.com:
        bar.example.com:
    dbservers:
      hosts:
        one.example.com:
        two.example.com:
        three.example.com:
```


