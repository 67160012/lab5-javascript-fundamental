# JavaScript Fundamentals – Code Explanation & Output

ไฟล์นี้อธิบายการทำงานของโค้ดในแต่ละ Activity พร้อมตัวอย่างผลลัพธ์ (Output) ที่ได้จากการรันด้วย Node.js

---

## 1️⃣ 01-variables.js

### 6. Challenge: Create a Person Object

### 🔹 โค้ดหลัก
- สร้าง object ชื่อ `student`
- มี properties:
  - `firstName`, `lastName`, `age`, `gpa`, `courses`, `isActive`
- มี methods:
  - `getFullName()`
  - `getInfo()`
- ใช้ `this` เพื่ออ้างอิงข้อมูลภายใน object

### 🔹 การทำงาน
- `getFullName()` → คืนค่า string ของชื่อ–นามสกุล
- `getInfo()` → เรียก `getFullName()` แล้วรวมข้อมูลอายุและ GPA

### 🔹 Output

Full name: Alice Smith
Info: Alice Smith, Age: 20, GPA: 3.8
Courses: HTML, CSS, JavaScript


---

## 2️⃣ 02-functions.js

### 8. Returning Objects

### 🔹 โค้ดหลัก
- ฟังก์ชัน `createUser()` คืนค่า object
- ใช้ shorthand property
- มี method เช่น `getFullName()`

### 🔹 การทำงาน
- เรียก `createUser("John", "Doe", 30)`
- ได้ object ใหม่ และเรียกใช้งานได้ทันที

### 🔹 Output

Email: john.doe@example.com

Full name: John Doe


---

### 9. Function as Parameter (Callback)

### 🔹 โค้ดหลัก
- ฟังก์ชัน `processArray(arr, callback)`
- รับ function เป็น parameter

### 🔹 การทำงาน
- `(x) => x * 2` → คูณสอง
- `(x) => x * x` → ยกกำลังสอง

### 🔹 Output

Original: [1,2,3,4,5]
Doubled: [2,4,6,8,10]
Squared: [1,4,9,16,25]


---

## 3️⃣ 03-control-flow.js

### 5. Short-Circuit Evaluation

### 🔹 โค้ดหลัก
- ใช้ `||` เลือกค่าที่เป็น truthy
- ใช้ `?.` (optional chaining)

### 🔹 การทำงาน
- `admin?.name` → undefined
- fallback ไปใช้ `user.name`

### 🔹 Output

User name: John


---

### 7. Form Validation

### 🔹 โค้ดหลัก
- ฟังก์ชัน `validateRegistration(formData)`
- เก็บ error ใน array `errors`

### 🔹 การทำงาน
- ถ้า `errors.length === 0` → valid
- ถ้ามีค่า → invalid

### 🔹 Output

Valid user: { isValid: true, errors: [] }
Invalid user: { isValid: false, errors: [...] }


---

## 4️⃣ 04-loops.js

### 9. Chaining Methods

### 🔹 โค้ดหลัก
- ใช้ `filter → map → join`

### 🔹 การทำงาน
- `filter` → เลขคู่
- `map` → ยกกำลังสอง
- `join` → รวมเป็น string

### 🔹 Output

Even numbers squared: 2²=4, 4²=16, 6²=36, 8²=64, 10²=100


---

### 10. Challenge: Student Grades

### 🔹 โค้ดหลัก
- `map` → ดึงชื่อ
- `filter` → เลือกคะแนนสูง
- `reduce` → average + top scorer
- `sort` → เรียงคะแนน

### 🔹 Output

Class average: 87.00
Top scorer: Alice (95)
Alice: 95 (A)
Diana: 92 (A)
Eve: 88 (B)


---

## 5️⃣ 05-integration.js

### Quiz Application

### 🔹 โค้ดหลัก
- เก็บคำถามใน array `quizzes`
- ใช้ `Math.random()` สุ่มคำตอบ
- เก็บผลใน `results`

### 🔹 การทำงาน
- ใช้ `forEach` วนลูปคำถาม
- ตรวจคำตอบ
- คำนวณคะแนน + เกรด
- ใช้ `filter` และ `reduce` สรุปผล

### 🔹 Output

FINAL SCORE: 3/5 (60.0%)
GRADE: D
Correct: 3
Incorrect: 2