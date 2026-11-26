# achitsak-abgroup — Knowledge Base

คลังบทวิเคราะห์ ข้อมูล และ market research ของผม จัดเก็บเป็น static HTML โฮสต์บน GitHub Pages

**เว็บไซต์:** https://achitsak-abgroup.github.io/

## โครงสร้าง 3 ชั้น: BU → Project → Report

```
achitsak-abgroup.github.io/
├── index.html                                        หน้าหลัก list BUs
├── assets/kb.css                                     shared styles (landing/BU/project)
├── .nojekyll
├── README.md
├── ABGV/index.html                                   BU: placeholder
├── ABIN/index.html                                   BU: placeholder
├── ABLM/index.html                                   BU: placeholder
├── ABBL/index.html                                   BU: AB BlueLane
├── ATRX/                                             BU: AB T-REX Car Wash
│   ├── index.html                                    list projects ใน ATRX
│   ├── market-research/
│   │   ├── index.html                                list reports
│   │   └── 20261125-sengcarcare-car-wash-market/
│   │       └── index.html                            รายงาน
│   └── predecessors-survey/
│       ├── index.html
│       └── 20261125-quickwash-field-observation/
│           ├── index.html                            รายงาน
│           └── assets/                               ภาพ Google Maps + Street View
└── Other/index.html                                  BU: catch-all
```

**กฎการตั้งชื่อ:**
- BU: รหัส 4 ตัวอักษร (ABGV, ABBL, ATRX ฯลฯ) ตรงกับ internal BU code
- Project: kebab-case อธิบายหัวเรื่อง เช่น `market-research`, `predecessors-survey`
- Report: `YYYYMMDD-<topic-kebab-case>` เช่น `20261125-quickwash-field-observation`
- URL ไม่ใช้ space และไม่ใช้ตัวอักษรไทย
- รูปของ report เก็บใน `<report-folder>/assets/`

## วิธีเพิ่ม

**รายงานใหม่ใน project เดิม:**
1. สร้างโฟลเดอร์ `<BU>/<project>/<YYYYMMDD>-<topic>/`
2. วาง `index.html` ลงในนั้น (ถ้ามีรูป → `assets/`)
3. เพิ่ม `<a class="r-card">` ใน `<BU>/<project>/index.html`
4. `git add . && git commit -m "atrx: add <topic>" && git push`

**Project ใหม่ใน BU เดิม:**
1. สร้างโฟลเดอร์ `<BU>/<new-project>/`
2. สร้าง `index.html` (copy โครงจาก `ATRX/market-research/index.html` แล้วแก้)
3. เพิ่ม `<a class="p-card">` ใน `<BU>/index.html`
4. ปรับ "N projects" ใน root `index.html`

**BU ใหม่:**
1. สร้างโฟลเดอร์ `<NEWBU>/` + `index.html` (copy จาก `ABGV/index.html` แล้วแก้)
2. เพิ่ม `<a class="p-card">` ใน root `index.html`

GitHub Pages จะ build + deploy อัตโนมัติภายใน 1–2 นาที

## Shared styles

Landing + BU + Project pages โหลด `/assets/kb.css` (ใช้ absolute path เพราะเป็น user page)
- `.p-card` — BU/project card (grid)
- `.r-card` — report card (list)
- `.empty` — placeholder เมื่อไม่มี content
- `.breadcrumb` — nav bar บนสุด

Report pages มี CSS ของตัวเองเพราะเป็น standalone artifact (เผื่อ download ไปใช้ offline)

## BU catalog

| Code | ชื่อ | Projects |
|---|---|---|
| ABGV | — | 0 |
| ABIN | — | 0 |
| ABLM | — | 0 |
| ABBL | AB BlueLane | 0 |
| [ATRX](ATRX/) | AB T-REX Car Wash | 2 |
| Other | — | 0 |

## แหล่งข้อมูล

ข้อมูลทั้งหมดเก็บจากแหล่งสาธารณะ (โพสต์ Facebook, ประกาศเปิด, Google Maps, สำรวจภาคสนาม) เนื้อหาในรายงานเป็นการวิเคราะห์เชิงสถิติ/สังเกตการณ์ ไม่รวมข้อมูลส่วนบุคคล

## สิทธิ์

เนื้อหารายงานและโค้ด HTML เผยแพร่เพื่อการศึกษา กรุณาอ้างอิงที่มาหากนำไปใช้ต่อ
