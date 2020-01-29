# Fillgoods Open API
***

## API : Create Order
Method : POST

Link : "/order/create"

Headers : 
```json
{
    "Content-Type": "application/json"
}
```

Request Parameter :
```json
{
    "order_number": "19112400001",
    "tracking_number": "111234567891",
    "payment_type": 2,
    "cod_amount": 0,
    "remark": "พัสดุแตกง่าย โปรดใช้ความระมัดระวัง",
    "src_name": "ร้านขายทุกอย่าง 20 บาท",
    "src_phone_number": "0811111111",
    "src_address": "11 หมู่ 2",
    "src_sub_district": "สวนจิตรลดา",
    "src_district": "ดุสิต",
    "src_province": "กรุงเทพมหานคร",
    "src_zipcode": "10300",
    "dst_name": "คุณทดสอบ การสร้างออเดอร์",
    "dst_phone_number": "0822222222",
    "dst_address": "33 หมู่ 4",
    "dst_sub_district": "สุเทพ",
    "dst_district": "เมืองเชียงใหม่",
    "dst_province": "เชียงใหม่",
    "dst_zipcode": "50200",
    "shop_id": 1,
    "weight": 1.5,
    "delivery_cost": 35
}
```

Request Description :

| Name  | Type | Required | Description |
|---|---|---|---|
| order_number  | string(20)  | true | Partner's order number |
| tracking_number  | string(100)  | true | Fillgoods's tracking number |
| payment_type  | integer  | true | Payment type (COD: 2, Transfer: 3)|
| cod_amount  | double  | false | COD amount (unit: baht) |
| remark  | string(500)  | false | Remark |
| src_name  | string(100)  | true | Shipper's name |
| src_phone_number | string(10)  | true | Shipper's phone number |
| src_address | string(200)  | true | Shipper's address |
| src_sub_district | string(100)  | true | Shipper's sub district |
| src_district  | string(100)  | true | Shipper's district |
| src_province  | string(100)  | true | Shipper's province|
| src_zipcode  | string(5)  | true | Shipper's zipcode |
| dst_name  | string(100)  | true | Consignee's name |
| dst_phone_number | string(10)  | true | Consignee's phone number |
| dst_address | string(200)  | true | Consignee's address |
| dst_sub_district | string(100)  | true | Consignee's sub district |
| dst_district  | string(100)  | true | Consignee's district |
| dst_province  | string(100)  | true | Consignee's province |
| dst_zipcode  | string(5)  | true | Consignee's zipcode |
| shop_id | integer | false | Shop ID when have many shops |
| weight | double | false | Product’s weight (kg) |
| delivery_cost | double | false | Delivery cost (baht) |


Response Parameter :
```json
{
    "success": true,
    "message": "",
    "order_number": "19112400001",
    "timestamp": 1528070400
}
```

Response Description :

| Name | Type | Description |
|---|---|---|
| success  | boolean  |  API success status (true, false)  |
| message  | string   | Error message when success = false |
| order_number  | string   | Partner's order number |
| timestamp  | integer   | The current unix timestamp |


<br>
<br>

## API : Create Order Without Tracking Number
Method : POST

Link : "/order/create-without-tracking-number"

Headers : 
```json
{
    "Content-Type": "application/json"
}
```

Request Parameter :
```json
{
    "order_number": "19112400001",
    "payment_type": 2,
    "cod_amount": 0,
    "remark": "พัสดุแตกง่าย โปรดใช้ความระมัดระวัง",
    "src_name": "ร้านขายทุกอย่าง 20 บาท",
    "src_phone_number": "0811111111",
    "src_address": "11 หมู่ 2",
    "src_sub_district": "สวนจิตรลดา",
    "src_district": "ดุสิต",
    "src_province": "กรุงเทพมหานคร",
    "src_zipcode": "10300",
    "dst_name": "คุณทดสอบ การสร้างออเดอร์",
    "dst_phone_number": "0822222222",
    "dst_address": "33 หมู่ 4",
    "dst_sub_district": "สุเทพ",
    "dst_district": "เมืองเชียงใหม่",
    "dst_province": "เชียงใหม่",
    "dst_zipcode": "50200",
    "shop_id": 1,
    "weight": 1.5,
    "delivery_cost": 35
}
```

Request Description :

| Name  | Type | Required | Description |
|---|---|---|---|
| order_number  | string(20)  | true | Partner's order number |
| payment_type  | integer  | true | Payment type (COD: 2, Transfer: 3)|
| cod_amount  | double  | false | COD amount (unit: baht) |
| remark  | string(500)  | false | Remark |
| src_name  | string(100)  | true | Shipper's name |
| src_phone_number | string(10)  | true | Shipper's phone number |
| src_address | string(200)  | true | Shipper's address |
| src_sub_district | string(100)  | true | Shipper's sub district |
| src_district  | string(100)  | true | Shipper's district |
| src_province  | string(100)  | true | Shipper's province|
| src_zipcode  | string(5)  | true | Shipper's zipcode |
| dst_name  | string(100)  | true | Consignee's name |
| dst_phone_number | string(10)  | true | Consignee's phone number |
| dst_address | string(200)  | true | Consignee's address |
| dst_sub_district | string(100)  | true | Consignee's sub district |
| dst_district  | string(100)  | true | Consignee's district |
| dst_province  | string(100)  | true | Consignee's province |
| dst_zipcode  | string(5)  | true | Consignee's zipcode |
| shop_id | integer | false | Shop ID when have many shops |
| weight | double | false | Product’s weight (kg) |
| delivery_cost | double | false | Delivery cost (baht) |


Response Parameter :
```json
{
    "success": true,
    "message": "",
    "order_number": "19112400001",
    "tracking_number": "111123456789",
    "timestamp": 1528070400
}
```

Response Description :

| Name | Type | Description |
|---|---|---|
| success  | boolean  |  API success status (true, false)  |
| message  | string   | Error message when success = false |
| order_number  | string   | Partner's order number |
| tracking_number  | string | Fillgoods's tracking number |
| timestamp  | integer   | The current unix timestamp |

<br>
<br>

## API : Calculate Cost with Weight
Method : POST

Link : "/courier/calculate-cost"

Headers : 
```json
{
    "Content-Type": "application/json"
}
```

Request Parameter :
```json
{
    "weight": 1.5,
    "shipping_province": "กรุงเทพมหานคร"
}
```

Request Description :

| Name  | Type | Required | Description |
|---|---|---|---|
| weight  | double | true | Product's weight (kg) |
| shipping_province  | string  | true | Shipping's province |

Response Parameter :
```json
{
    "success": true,
    "message": "",
    "cost": 68
}
```

Response Description :

| Name | Type | Description |
|---|---|---|
| success  | boolean  |  API success status (true, false)  |
| message  | string   | Error message when success = false |
| cost  | string   | Delivery cost (baht) |


<br>
<br>

## API : Create SCG Booking
Method : POST


Link : "/courier/scg/create-booking"

####  ** MUST USE AN API BEFORE 11:00 (GMT+7) **

Headers : 
```json
{
    "Content-Type": "application/json"
}
```

Request Parameter :
```json
{
    "booking_time": "15:00",
    "quantity": 5,
    "shipper_name": "ร้านขายทุกอย่าง 20 บาท",
    "shipper_phone_number": "0811111111",
    "shipper_address": "11 หมู่ 2",
    "shipper_sub_district": "สวนจิตรลดา",
    "shipper_district": "ดุสิต",
    "shipper_province": "กรุงเทพมหานคร",
    "shipper_zipcode": "10300",
    "remark": "พัสดุแตกง่าย โปรดใช้ความระมัดระวัง"
}
```

Request Description :

| Name  | Type | Required | Description |
|---|---|---|---|
| booking_time  | double | true | Time for booking hh:mm (must be 13:00, 13:30, 14:00, 14:30, 15:00 (GMT+7)) |
| quantity  | double | true | Order quantity for booking |
| shipper_name  | string(100)  | true | Shipper's name for booking |
| shipper_phone_number | string(10)  | true | Shipper's phone number for booking |
| shipper_address | string(200)  | true | Shipper's address for booking |
| shipper_sub_district | string(100)  | true | Shipper's sub district for booking |
| shipper_district  | string(100)  | true | Shipper's district for booking |
| shipper_province  | string(100)  | true | Shipper's province for booking |
| shipper_zipcode  | string(5)  | true | Shipper's zipcode for booking |
| remark  | string(500)  | false | Remark |

Response Parameter :
```json
{
    "success": true,
    "message": "",
    "booking_id": 1
}
```

Response Description :

| Name | Type | Description |
|---|---|---|
| success  | boolean  |  API success status (true, false)  |
| message  | string   | Error message when success = false |
| booking_id  | integer  | SCG booking ID |



<br>
<br>

## API : Cancel SCG Booking
Method : POST

Link : "/courier/scg/cancel-booking"

Headers : 
```json
{
    "Content-Type": "application/json"
}
```

Request Parameter :
```json
{
    "booking_id": 1
}
```

Request Description :

| Name  | Type | Required | Description |
|---|---|---|---|
| booking_id  | interger  | true |  SCG booking ID |

Response Parameter :
```json
{
    "success": true,
    "message": ""
}
```

Response Description :

| Name | Type | Description |
|---|---|---|
| success  | boolean  |  API success status (true, false)  |
| message  | string   | Error message when success = false |

