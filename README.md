# BOQ Team Workload — Schedule Timeline

เว็บแอปแสดง Timeline และ Workload ของทีม BOQ  
Deploy ผ่าน **GitHub Pages** และเก็บต้นฉบับใน **SharePoint Document Library**

---

## 🌐 GitHub Pages URL
หลัง deploy แล้วจะเข้าได้ที่:
```
https://<your-username>.github.io/<repo-name>/
```

## 📁 โครงสร้างไฟล์
```
boq-workload-site/
├── index.html          ← หน้าเว็บหลัก (BOQ Team Workload)
└── README.md           ← ไฟล์นี้
```

## 🚀 วิธี Deploy ขึ้น GitHub Pages

### ขั้นตอนที่ 1 — สร้าง Repository
1. ไปที่ [github.com/new](https://github.com/new)
2. ตั้งชื่อ repo เช่น `boq-workload-site`
3. เลือก **Public** (GitHub Pages ฟรีต้องเป็น Public)
4. กด **Create repository**

### ขั้นตอนที่ 2 — อัปโหลดไฟล์
**วิธี A — ผ่าน Browser (ง่ายที่สุด):**
1. เข้า repo ที่สร้างไว้
2. กด **Add file → Upload files**
3. ลาก `index.html` และ `README.md` ใส่
4. กด **Commit changes**

**วิธี B — ผ่าน Git CLI:**
```bash
git clone https://github.com/<username>/boq-workload-site.git
cd boq-workload-site
cp /path/to/index.html .
git add .
git commit -m "Add BOQ Workload page"
git push
```

### ขั้นตอนที่ 3 — เปิด GitHub Pages
1. ไปที่ **Settings** ของ repo
2. เลือกเมนู **Pages** (ด้านซ้าย)
3. ใต้ **Source** เลือก `Deploy from a branch`
4. Branch: **main**, Folder: **/ (root)**
5. กด **Save**
6. รอ ~1-2 นาที แล้วหน้าเว็บจะขึ้น URL

---

## 🗂️ วิธีเก็บต้นฉบับใน SharePoint

### ขั้นตอนที่ 1 — เข้า Document Library
1. เปิด SharePoint Site ของทีม
2. เข้าไปที่ **Documents** (หรือ Library ที่ต้องการ)
3. สร้างโฟลเดอร์ใหม่ชื่อ `BOQ-Workload` (แนะนำ)

### ขั้นตอนที่ 2 — อัปโหลดไฟล์
1. กด **Upload → Files**
2. เลือกไฟล์ `index.html` (ต้นฉบับ)
3. กด **Open** → ไฟล์จะขึ้นใน Library

### ขั้นตอนที่ 3 — ตั้งค่า Version History (แนะนำ)
1. คลิกขวาที่ไฟล์ → **Version history**
2. SharePoint จะเก็บประวัติทุกครั้งที่อัปเดตโดยอัตโนมัติ

---

## 🔄 Workflow แนะนำเมื่อต้องอัปเดต

```
แก้ไข HTML → อัปโหลดทับใน SharePoint → อัปโหลดทับใน GitHub → Pages อัปเดตอัตโนมัติ
```

| ที่เก็บ | วัตถุประสงค์ | ใครเข้าถึง |
|---------|------------|-----------|
| SharePoint | ต้นฉบับ + Version control | ทีมภายในองค์กร |
| GitHub Pages | เว็บสาธารณะ / แชร์ลิงก์ | ทุกคนที่มี URL |
