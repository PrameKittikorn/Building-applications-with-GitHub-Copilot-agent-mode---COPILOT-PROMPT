# Building-applications-with-GitHub-Copilot-agent-mode---COPILOT-PROMPT

## เริ่มต้นโปรเจกต์ BMI Calculator

```jsx
Please make a basic BMI calculator web with HTML, CSS, JS
and Design based on Tailwind.css
```

## เพิ่มการ Login

```jsx
รบกวนเพิ่มหน้า Login อย่างง่ายโดยใช้แค่ HTML, CSS, JS และ Tailwind เหมือนเดิม โดยที่ให้ทำตามเงื่อนไขดังนี้

Username ที่ถูกต้องคือ demo และ รหัสที่ถูกต้องคือ dome
ถ้าหากกรอก Username หรือ รหัสผ่านผิด ให้แสดงว่าผิดพลาด
ถ้าหากไม่ได้กรอกรบกวนคิดข้อความใส่ Required field ไว้ด้วย
หาก Login สำเร็จถึงสามารถคำนวณ BMI Calculator (ฟังก์ชันก่อนหน้าที่เขียนไว้ได้)
```

## แสดงผลด้วย SweetAlert2

```jsx
อยากให้การแสดงผล BMI ขึ้นมาให้สวยกว่านี้โดยใช้ SweetAlert2 ในการแสดงผล BMI ที่คำนวณได้

ให้คิด case ที่เป็นไปได้ของ BMI เช่น ผอม น้ำหนักปกติ น้ำหนักเกิน หรือ อื่น ๆ พร้อมทำการออกแบบหน้าตา Alert ให้เหมาะสมกับผลที่ได้

เขียนข้อความกำกับวิธีการดูแลสุขภาพเบื้องต้นสำหรับในเคสต่าง ๆ
```

## เพิ่มหลายฟีเจอร์ลงไป

```jsx
ต้องการเพิ่มฟีเจอร์หลังจาก Login เข้าสู่ระบบ โดยที่โปรแกรมจะไม่ได้มีแค่ฟังก์ชันในการคำนวณ BMI อย่างเดียวแล้ว แต่ยังสามารถคำนวณด้านสุขภาพอย่างอื่นได้ เช่น

- ปริมาณแคลลอรี่ที่ควรได้รับต่อวัน
- ปริมาณน้ำที่ควรดื่มต่อวัน (น้ำหนักตัว (กิโลกรัม) X 0.03)
- ปริมาณของโปรตีนที่ควรได้รับต่อวัน
- BMR (Basal Metabolic Rate)
- % Body Fat (ตาม BMI)

และ หลังจากคำนวณเรียบร้อย ไม่ใช้ SweetAlert2 แล้ว แต่ใช้แค่เพียง Tailwind แทนเพื่อแสดงผลออกมาในรูปแบบ Dashboard เกี่ยวกับข้อมูลสุขภาพของเรา
```

## Refactoring Project

```jsx
รบกวนจัดระเบียบ และ เพิ่มคุณภาพ (Refactoring) ของ Project โดย

- การแยกไฟล์ในส่วนของ Logic / Stylesheets ออกจาก HTML 

- ทำการแยกส่วนการทำงานเป็น Function ให้ชัดเจน โดยในแต่ละฟังก์ชันจะทำหน้าที่ของตัวเอง ไม่เอาส่วนหน้าตามารวมกับ Logic เพื่อให้สามารถทำการ Unit Test ได้
```

## Unit Testing

```jsx
รับบทบาทเป็นผู้เชี่ยวชาญด้านโภชนาการ และ การดูแลสุขภาพ ให้ทำการเขียน Testcase ที่ไว้ทดสอบว่าการคำนวณต่าง ๆ ที่พัฒนาขึ้นนั้นถูกต้องหรือไม่

โดยตอนนี้ในเครื่องของเราได้ติดตั้ง node.js ไว้แล้ว รบกวนวางแผน และ ดำเนินการให้ตั้งแต่การคิด Testcase จนถึง การสร้าง Testcase บน Project ให้หน่อย

ขอบคุณครับ
```

### วิธีแก้ npm.ps1 cannot be loaded because running scripts is disabled on this system (Step by Step)

https:/go.microsoft.com/fwlink/?LinkID=135170.

**1. เปิด PowerShell แบบ Administrator**

- กด Start พิมพ์ว่า “PowerShell”
- คลิกขวา → เลือก **Run as administrator**

**2. เช็ค Policy ปัจจุบัน**

```powershell
Get-ExecutionPolicy
```

ปกติถ้าขึ้นว่า `Restricted` คือเข้มงวดสุด

**3. เปลี่ยน Policy ให้รัน Script ได้**

```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```

- `CurrentUser` = มีผลกับ user ของเรา ไม่กระทบคนอื่นในเครื่อง
- `RemoteSigned` = Script ที่โหลดมาจาก Internet ต้องมีลายเซ็นต์ (แต่ script ที่เขียนเองในเครื่องรันได้)

**4. กด Y (Yes) เพื่อยืนยัน**

**5. ปิด PowerShell แล้วกลับมารัน npm ใน VS Code ตามปกติ**

## ทำการทดสอบและแก้ไขอีกครั้ง

```jsx
รบกวน Run test แล้วดูผลลัพธ์ให้หน่อย เหมือนว่าจะมีการคำนวณที่ผิดในบาง Test case อยู่ รบกวนแก้ไขให้ด้วย
```

## ขึ้น repository
