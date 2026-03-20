# Medication Error Dashboard

Dashboard แสดงข้อมูลความคลาดเคลื่อนทางยา (Medication Error) แบบ Interactive
สร้างด้วย HTML + Chart.js + PapaParse | Host บน GitHub Pages (ฟรี)

---

## วิธี Deploy ขึ้น GitHub Pages

### ขั้นตอนที่ 1 — สร้าง GitHub Account (ถ้ายังไม่มี)
ไปที่ https://github.com → Sign up

### ขั้นตอนที่ 2 — สร้าง Repository ใหม่
1. กด **+** (มุมบนขวา) → **New repository**
2. ตั้งชื่อ repo เช่น `med-error-dashboard`
3. เลือก **Public** (จำเป็นสำหรับ GitHub Pages ฟรี)
4. **อย่า** tick "Add a README file"
5. กด **Create repository**

### ขั้นตอนที่ 3 — Upload ไฟล์
**วิธี A — ผ่าน Web browser (ง่ายที่สุด)**
1. เปิด repo ที่สร้างไว้
2. กด **Add file** → **Upload files**
3. ลาก 2 ไฟล์เข้า:
   - `index.html`
   - `data.csv`
4. กด **Commit changes**

**วิธี B — ผ่าน Git (command line)**
```bash
cd "c:/INVC/Dashboard Med"
git init
git add index.html data.csv
git commit -m "Initial dashboard"
git branch -M main
git remote add origin https://github.com/<username>/med-error-dashboard.git
git push -u origin main
```

### ขั้นตอนที่ 4 — Enable GitHub Pages
1. เปิด repo → แถบ **Settings**
2. เมนูซ้าย → **Pages**
3. ใต้ "Branch" เลือก **main** → folder **/ (root)**
4. กด **Save**
5. รอ 1-3 นาที → URL จะปรากฏ:
   `https://<username>.github.io/med-error-dashboard/`

---

## ไฟล์ในโปรเจค

| ไฟล์ | คำอธิบาย |
|---|---|
| `index.html` | Dashboard (HTML + CSS + JavaScript ทั้งหมด) |
| `data.csv` | ข้อมูล Medication Error (~51,700 rows) |
| `README.md` | ไฟล์นี้ |

---

## Features

- **KPI Cards:** Total Incidents, HAD Cases, High Severity (D+E), HAD Rate %
- **Monthly Trend:** Line chart แนวโน้มรายเดือน
- **Unit Distribution:** Doughnut chart (IPD / OPD / PCC / E.R.)
- **Severity:** Bar chart (B / C / D / E)
- **Error Type:** Bar chart ประเภท error
- **Top 15 Wards:** Horizontal bar
- **Top 15 Subtypes:** Horizontal bar
- **Filters:** เดือน, Unit, Severity, HAD — real-time

---

## Tech Stack

- [Chart.js 4](https://www.chartjs.org/) — กราฟ
- [PapaParse 5](https://www.papaparse.com/) — parse CSV
- [Bootstrap 5](https://getbootstrap.com/) — layout/UI
- ไม่ต้อง install หรือ build ใดๆ ทุกอย่างโหลดผ่าน CDN
