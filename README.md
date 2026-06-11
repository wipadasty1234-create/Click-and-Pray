# SMC Backtest Journal — PWA

## โครงสร้างไฟล์
```
smc-backtest-pwa/
├── index.html          ← แอพหลัก
├── manifest.json       ← PWA config
├── sw.js               ← Service Worker (offline cache)
└── icons/
    ├── icon-72.png
    ├── icon-96.png
    ├── icon-128.png
    ├── icon-144.png
    ├── icon-152.png
    ├── icon-192.png
    ├── icon-384.png
    └── icon-512.png
```

---

## วิธีติดตั้งบน iPad / iPhone (Safari)

1. **เปิดไฟล์ index.html** ใน Safari
2. กดปุ่ม **⬆ Share** (ไอคอนกล่องมีลูกศรขึ้น) ที่แถบด้านล่าง
3. เลื่อนลงในเมนู → กด **"Add to Home Screen"**
4. แก้ชื่อเป็น **"SMC Journal"** (หรือชื่อที่ชอบ)
5. กด **"Add"**
6. App icon จะปรากฏบน Home Screen ทันที

> ⚠️ ต้องใช้ **Safari เท่านั้น** (Chrome/Firefox บน iOS ไม่รองรับ Add to Home Screen)

---

## วิธีติดตั้งบน Android (Chrome)

1. เปิดไฟล์ใน Chrome
2. Chrome จะแสดง banner **"Add to Home Screen"** อัตโนมัติ
3. กด **"Install"** หรือ **"ติดตั้ง"**

---

## วิธีใช้งาน Offline

Service Worker จะ cache ทุกไฟล์ไว้อัตโนมัติตั้งแต่เปิดครั้งแรก
หลังจากนั้น **ใช้งานได้โดยไม่ต้องต่อเน็ตเลย**

---

## หมายเหตุสำคัญ

- ข้อมูล trade เก็บใน **Local Storage** ของ browser
- ถ้าลบ app / clear browser data — ข้อมูลจะหาย
- แนะนำ **Export JSON** ไว้สำรองเป็นประจำ
- ถ้าเปลี่ยนเครื่อง ให้ Import JSON กลับมา
