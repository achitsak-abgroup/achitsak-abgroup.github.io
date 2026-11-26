# achitsak-abgroup — Knowledge Base

คลังบทวิเคราะห์ ข้อมูล และ market research ของผม จัดเก็บเป็น static HTML โฮสต์บน GitHub Pages

**เว็บไซต์:** https://achitsak-abgroup.github.io/

## โครงสร้าง

```
achitsakp.github.io/
├── index.html                                        หน้าหลัก list projects
├── ATRX/                                             project: market research
│   ├── index.html                                    list รายงานใน ATRX
│   └── 20261125-sengcarcare-car-wash-market/
│       └── index.html                                รายงาน
└── <project>/                                        (projects อื่นๆ ในอนาคต)
    └── <YYYYMMDD>-<topic-kebab-case>/
        └── index.html
```

**กฎการตั้งชื่อ:**
- Project: ตัวพิมพ์ใหญ่ รหัสสั้น เช่น `ATRX`, `ABG`, `ATLAS`
- Report: `YYYYMMDD-<topic-kebab-case>` เช่น `20261125-sengcarcare-car-wash-market`
- URL ไม่ใช้ space (ใช้ dash แทน) และไม่ใช้ตัวอักษรไทย

## วิธีเพิ่มรายงานใหม่

1. สร้างโฟลเดอร์ `<PROJECT>/<YYYYMMDD>-<topic>/`
2. วาง `index.html` ลงในนั้น
3. เพิ่ม card ใน `<PROJECT>/index.html` (block `.r-card`)
4. ถ้าเพิ่ม project ใหม่: สร้าง `<PROJECT>/index.html` + เพิ่ม card ในหน้า root `index.html`
5. `git add . && git commit -m "atrx: add <topic>" && git push`

GitHub Pages จะ build + deploy อัตโนมัติภายใน 1–2 นาที

## Projects

| Code | ชื่อ | รายงาน |
|---|---|---|
| [ATRX](ATRX/) | Market Research &amp; Business Analysis | 1 |

## แหล่งข้อมูล

ข้อมูลทั้งหมดเก็บจากแหล่งสาธารณะ (โพสต์ Facebook, ประกาศเปิด, ข่าว) เนื้อหาในรายงานเป็นการวิเคราะห์เชิงสถิติ ลิงก์ในตารางชี้ไปที่ต้นทางเพื่อตรวจสอบย้อนกลับได้

## สิทธิ์

เนื้อหารายงานและโค้ด HTML เผยแพร่เพื่อการศึกษา กรุณาอ้างอิงที่มาหากนำไปใช้ต่อ
