# TypeScript Learning Guideline

## Disclaimer

AI-Based (Gemini 2.5 Pro) -> Need to clarify.

## Phase 0: The Foundation (ก่อนจะเริ่มกับ TypeScript)

ก่อนจะจับ TypeScript เราต้องมีพื้นฐาน JavaScript ที่แข็งแรงมากๆ ก่อนนะคะ เพราะ TypeScript คือ Superset ของ JavaScript ค่ะ

สิ่งที่ต้องรู้ใน JavaScript:

- พื้นฐานแน่นๆ: ตัวแปร (var, let, const), Data Types, Functions, Scope, this keyword.
- Modern JavaScript (ES6+): Arrow Functions, Destructuring, Spread/Rest Operators, Template Literals.
- Asynchronous: Promises และโดยเฉพาะ async/await สำคัญมากๆ ค่ะ
- Modules: การทำงานของ import และ export.
- ความเข้าใจเรื่อง Prototype & Class: แม้ TypeScript จะมี Class ที่ดูง่าย แต่การเข้าใจว่าเบื้องหลังมันคือ Prototype จะช่วยได้มากค่ะ

## Phase 1: The Basics (พื้นฐาน TypeScript ที่ต้องรู้)

เฟสนี้คือการทำความรู้จักกับ "ไวยากรณ์" และ "แนวคิด" หลักของ TypeScript ค่ะ

หัวข้อการเรียนรู้:

- Core Types: ทำความรู้จักไทป์พื้นฐาน string, number, boolean, null, undefined.
- Special Types: เข้าใจความแตกต่างและการใช้งานของ any, unknown, และ never.
- Arrays & Tuples: การประกาศไทป์ให้กับ Array และการใช้ Tuple สำหรับ Array ที่มีโครงสร้างตายตัว
- Objects, type vs interface: เรียนรู้การสร้างไทป์สำหรับ Object และทำความเข้าใจว่าเมื่อไหร่ควรใช้ type หรือ interface.
- Functions: การกำหนดไทป์ให้ Parameters และ Return Value ของฟังก์ชัน
- Union (|) & Intersection (&) Types: การรวมไทป์เพื่อให้ยืดหยุ่นมากขึ้น
- การติดตั้งและใช้งาน: เรียนรู้วิธีติดตั้ง TypeScript Compiler (tsc), การคอมไพล์ไฟล์ .ts เป็น .js, และการตั้งค่าไฟล์ tsconfig.json เบื้องต้น

## Phase 2: Intermediate - The Power Unleashed (สู่การเป็น TypeScript Master)

เมื่อพื้นฐานแน่นแล้ว เราจะมาปลดปล่อยพลังของ TypeScript กันค่ะ! ความรู้ในเฟสนี้จะทำให้พี่สามารถอ่านโค้ดของ ElysiaJS ได้เข้าใจมากขึ้น

หัวข้อการเรียนรู้:

- Generics (<T>): นี่คือหัวใจสำคัญที่สุด! คือการสร้างฟังก์ชันหรือไทป์ที่ "ยืดหยุ่น" และใช้ซ้ำได้โดยไม่สูญเสีย Type Safety
- Enums: การสร้างกลุ่มของค่าคงที่ที่มีชื่อเรียก
- Classes & Access Modifiers: การใช้งาน public, private, protected ในคลาส
- Utility Types: ฝึกใช้ Utility Types ที่มีมาให้จนคล่อง เช่น Partial<T>, Readonly<T>, Pick<T, K>, Omit<T, K>, ReturnType<T>.
- Type Guards & Narrowing: เทคนิคการตรวจสอบเพื่อ "จำกัด" ไทป์ให้แคบลงและปลอดภัยขึ้น เช่น การใช้ typeof, instanceof, in และการสร้าง User-Defined Type Guards (e.g., function isUser(obj: any): obj is User)

## Phase 3: Advanced - The Magic Level (ระดับเทพ: Type-Level Programming)

นี่คือเฟสที่สนุกและท้าทายที่สุด! เป็นระดับที่ใช้สร้างไลบรารีอย่าง ElysiaJS ซึ่งเป็นการ "เขียนโปรแกรมด้วยไทป์" เพื่อให้ TypeScript ทำงานให้เราโดยอัตโนมัติ

หัวข้อการเรียนรู้:

- Conditional Types: T extends U ? X : Y มันคือ if-else ในโลกของไทป์!
- Mapped Types: [P in keyof T]: ... การวนลูปบน Key ของ Object เพื่อสร้างไทป์ใหม่ (เบื้องหลังของ Utility Types ส่วนใหญ่)
- infer Keyword: เวทมนตร์ที่แท้จริง! ใช้คู่กับ Conditional Types เพื่อ "ดึง" ไทป์ที่ซ่อนอยู่ออกมา เช่น ดึงไทป์ของ Return Value จากฟังก์ชัน หรือไทป์ของ property ใน Object
- Template Literal Types: การสร้างและจัดการไทป์ที่เป็น string เช่น type Path = \/${string}``
- Recursive Types: การสร้างไทป์ที่สามารถอ้างอิงถึงตัวเองได้ เพื่อจัดการข้อมูลที่ซับซ้อนอย่าง JSON
- keyof และ typeof ขั้นสูง: การใช้สองคำสั่งนี้ร่วมกับเทคนิคอื่นเพื่อสร้างไทป์ที่ซับซ้อน
- ฝึกฝนกับ Type-Challenge: สำคัญที่สุดในเฟสนี้! ไปที่ Type-Challenge แล้วเริ่มทำตั้งแต่ข้อแรกๆ มันคือสนามเด็กเล่นและยิมที่ดีที่สุดสำหรับการฝึกสมองด้าน Type-Level Programming ค่ะ

## Phase 4: The Application (นำไปใช้จริง: วิเคราะห์ ElysiaJS และสร้าง Library)

เมื่อมีอาวุธครบมือแล้ว ก็ถึงเวลาลงสนามจริง!

วิเคราะห์ ElysiaJS:

- เปิดดูโค้ดที่พี่อัปโหลดมา โดยเฉพาะไฟล์ src/index.ts, src/schema.ts, และ src/types.ts.
- พยายามหาแพทเทิร์นจากสิ่งที่เรียนมาใน Phase 3:
- "ตรงนี้ใช้ Generic เพื่อให้ .get() รับไทป์ของ Schema ได้"
- "ตรงนี้ใช้ Conditional Type กับ infer เพื่อดึงไทป์ body ออกมาจาก Schema ที่เราประกาศไว้"
- "ทำไม Context ถึงมี body ที่ถูกต้องได้? อ๋อ เพราะมันถูกสร้างขึ้นมาจาก Mapped Types นี่เอง"

สร้าง Library ของตัวเอง:

- ตั้งเป้าหมายเล็กๆ: เช่น "สร้าง Mini-Elysia ที่มีแค่ .get() กับ .post() และมี Type-safe body"
- ออกแบบ API: คิดว่าจะให้ผู้ใช้เขียนโค้ดแบบไหน (Developer Experience)
- เริ่มจาก Types: สร้างไทป์หลักๆ ด้วย Generics และ Conditional Types ก่อน
- เขียนโค้ด Runtime: เขียน Logic การทำงานจริงๆ ของฟังก์ชันต่างๆ
- ทดสอบ: เขียนเทสสำหรับทั้ง Type และ Runtime Behavior
