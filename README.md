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
    "dst_zipcode": "50200"
}
```

Request Description :

| Name  | Type | Required | Description |
|---|---|---|---|
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
| message  | string   | Error message when success = false ||
