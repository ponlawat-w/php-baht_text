# php-baht_text

ฟังก์ชัน `baht_text` ใช้สำหรับแปลงจำนวนเงินให้เป็นข้อความ ในภาษา PHP

`baht_text` is a PHP function that converts a number into Thai text with baht currency format (as `BAHTTEXT()` function in Excel).

## พารามีเตอร์

1. **`double|int $number`** - จำนวนเงิน
2. **`bool $include_unit`** - เพิ่มหน่วยบาท/สตางค์หรือไม่ (ค่าเริ่มต้น: `true`)
3. **`bool $display_zero`** - แสดงผลข้อความสำหรับเลข 0 หรือไม่ เช่น ศูนย์บาทถ้วน (ค่าเริ่มต้น: `true`)

## การคืนค่า

จะคืนค่าเป็น `string` ของข้อความจำนวนเงินที่แปลงแล้ว แต่หากอินพุตไม่ใช่ตัวเลขจะคืนค่าเป็น `null`

## ตัวอย่าง

### ตัวอย่าง 1
```
echo baht_text(54627); // ห้าหมื่นสี่พันหกร้อยยี่สิบเจ็ดบาทถ้วน
```

### ตัวอย่าง 2
```
echo baht_text('361.75'); // สามร้อยหกสิบเอ็ดบาทเจ็ดสิบห้าสตางค์
```

### ตัวอย่าง 3
```
echo baht_text(5001, false); // ห้าพันหนึ่ง
```

### ตัวอย่าง 4
```
echo baht_text(532729.78, false); // ห้าพันหนึ่ง
```

### ตัวอย่าง 5
```
var_dump(baht_text('500a')); // NULL
```