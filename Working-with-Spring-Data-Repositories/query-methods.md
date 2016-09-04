### 4.2 查询方法

标准的CRUD功能存储库通常对底层数据存储查询。 Spring Data把这些查询变成了四个步骤的过程:

1、声明一个接口扩展库和类型它或者它的一个个子域类和ID类型,它将处理。
``` java
interface PersonRepository extends Repository<User, Long> { … }
```

2、接口上新建条件查询的方法。
``` java
interface PersonRepository extends Repository<User, Long> { List<Person> findByLastname(String lastname); }
```

