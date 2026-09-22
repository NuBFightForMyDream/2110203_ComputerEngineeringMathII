# CEMII Lab — 2110203 Visualizers

เปิด `index.html` ในเบราว์เซอร์ → หน้ารวมที่แบ่งตาม part ของวิชา กดเลือก lecture แล้วหน้านั้นจะเปิดในหน้าเดียวกัน

## โครงสร้าง

```
Visualizer Web/
├── index.html                      ← หน้ารวม (แถบเมนู + รายการตาม part)
├── Signal Part I/
│   └── convolution-lab.html        ← Lecture 02 Convolution
└── Optimization/                   ← ยังว่าง
```

แต่ละไฟล์ `.html` ของ lecture เป็นไฟล์เดียวจบ (CSS + JS อยู่ในตัว) เปิดเดี่ยว ๆ ก็ได้

## เพิ่ม lecture ใหม่

1. วางไฟล์ `.html` ของ lecture ไว้ในโฟลเดอร์ของ part นั้น เช่น `Signal Part I/fourier-lab.html`
2. เปิด `index.html` แล้วเพิ่ม object ใน `lectures` ของ part นั้นใน `PARTS`:

```js
{ id: 'fourier', no: '03', title: 'Fourier Transform', th: 'การแปลงฟูเรียร์', file: 'fourier-lab.html',
  desc: 'คำอธิบายสั้น ๆ', tags: ['แท็ก 1', 'แท็ก 2'] }
```

3. part ใหม่ = เพิ่ม object ใน `PARTS` (`folder` คือชื่อโฟลเดอร์)

ลิงก์ออนไลน์ (Claude artifact) ใช้หน้าเดียวกันนี้ แต่รวมไฟล์ lecture ไว้ข้างในแล้ว จึงเปิดได้จากลิงก์เดียว
