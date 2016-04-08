鱿鱼旅行接口文档
===================================
### 获取推荐路线详情
> @GET("http://apidev.youyulx.com/1.0/product?product_id=1&sid=0.28298112302865286&vid=dc15268c732ded686ce41e3500dfe33b&ts=1459149571261&cid=q94ibEVe")


###  product 产品详情

| 字段        | 类型           |备注|
| ------------- |:-------------:|:-------------:|
|  liked     |boolean |该用户是否收藏  |
|   like_count    |int |该推荐线路收藏次数  |
| product_number      |string | 线路编号 |
|   product_number    |string | 费用说明 |
|    id   |string |线路id  |
|    introduction   |string | 产品简介 |
|  tags     |array<string> | 产品标签 |
|  recommend     |boolean | 是否为推荐路线  |
|    effective_date   |string | 有效期? |
|   spec    |spec | 产品套餐规格 对象|
|  more_info     |string | 产品更多信息  |
|     notice  |string | 产品须知 提示  |
|   departure_place    |departure_place | 出发地 对象 |
|    price   |array<price> | 套餐价格  对象数组|
|      expiry_date |string | (套餐 产品)过期时间? |
|   price_range    |array<string> | 价格区间 |
|   name    |string | 产品名称 |
|   created_at    |string | 创建时间 |
|   summary    |string | 产品简介 |
|    tour   |tour | 路线行程  对象|
|    date_rule   |string | 产品可下单时间  |
|    cover_image   |string | 产品封面图 |
|    category_id   |int | 产品种类 3:个人;4:团体 |


#### product -> spec 产品套餐规格

| 字段        | 类型           |备注|
| ------------- |:-------------:|:-------------:|
|product_id|int | 该产品路线id |
|  items     |array<items> | 套餐对象 |
|  created_at  |string | 创建时间 |
|  updated_at |string | 更新时间 |
|  id   |int | 规格id |
|  name   |string | 规格总名称  |


##### product -> spec -> items 产品套餐规格详情

| 字段        | 类型           |备注|
| ------------- |:-------------:|:-------------:|
|updated_at|string | |
|created_at|string |  |
|product_spec_id|int | 产品规格id |
|id |int | 规格下的自增id |
|name |string |规格名称  |


#### product -> price 产品套餐价格

| 字段        | 类型           |备注|
| ------------- |:-------------:|:-------------:|
|  sku   |string |  |
|  product_id   |string |  该产品线路id |
|  price   |float |套餐价格   |
|  updated_at   |string |   |
|    id  |string |  套餐id |
|  date_rule_id   |string | 时间对应规则id  |
|  created_at   |string |   |


#### product -> tour 路线行程

| 字段        | 类型           |备注|
| ------------- |:-------------:|:-------------:|
|  route   | array<route> | 每天行程安排  |
|    id  |int |  自增id |

#### product -> tour -> route 每天行程安排

| 字段        | 类型           |备注|
| ------------- |:-------------:|:-------------:|
|  items   | array<items> | 具体每天行程安排 |
|  day   | int | 第几天 |
|    subject  | string |  当前行程主题 |

#### product -> tour -> route -> items 每天行程安排

| 字段        | 类型           |备注|
| ------------- |:-------------:|:-------------:|
|  images   | array<string> | 项目图片数组 |
|  type   | int | 项目类型 |
|    description  | string |  项目类型说明 |
|    resource_id  | int |  资源id |


#### product -> date_rule 路线套餐日期

| 字段        | 类型           |备注|
| ------------- |:-------------:|:-------------:|
|    byday  |string |  ???? |
|    product_id  |int | 该产品id  |
|     bymonth |string | 可出发月份?  |
|   created_at   |string |   |
|   priority   |string | 优先级?|
|    byweekday  |array<int> |  可出发星期几 |
|    id  |int |  日期id  |
































