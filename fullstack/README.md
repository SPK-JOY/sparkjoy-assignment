# Full Stack Technical Assignment

## วัตถุประสงค์

แบบทดสอบนี้มีไว้เพื่อให้เราได้เห็นแนวทางการพัฒนา Full Stack ของผู้สมัคร ทั้งในด้าน Frontend, Backend, การออกแบบโครงสร้างโปรเจกต์ และการเชื่อมต่อระหว่างระบบ

ไม่มีคำตอบที่ถูกหรือผิดเพียงแบบเดียว เราให้ความสำคัญกับแนวคิด กระบวนการคิด และเหตุผลในการออกแบบ มากกว่าการทำฟีเจอร์ให้ครบทุกอย่าง

เราไม่ได้คาดหวังให้ Assignment นี้สมบูรณ์แบบ หากมีข้อจำกัดด้านเวลา สามารถอธิบายสิ่งที่เลือกทำ สิ่งที่ยังไม่ได้ทำ และแนวทางที่จะพัฒนาต่อไว้ใน README ได้

---

## ระยะเวลาที่แนะนำ

Assignment นี้ออกแบบให้ใช้เวลาประมาณ **4–8 ชั่วโมง**

ไม่จำเป็นต้องทำทุกอย่างให้ครบ หากมีเวลาจำกัด สามารถเลือกทำเฉพาะส่วนที่ต้องการแสดงศักยภาพ และอธิบายเหตุผลไว้ใน README

---



## Requirements



### 1. Data Preparation

ศึกษาโครงสร้างข้อมูลจากไฟล์ `posts.json`

ข้อมูลแต่ละ Post ประกอบด้วย


| Field      | Description                                         |
| ---------- | --------------------------------------------------- |
| `title`    | หัวข้อของ Post                                      |
| `content`  | เนื้อหาในรูปแบบ HTML                                |
| `postedAt` | วันที่และเวลาที่โพสต์                               |
| `postedBy` | ผู้สร้าง Post                                       |
| `tags`     | Tag ของ Post โดยหนึ่ง Post สามารถมีได้มากกว่า 1 Tag |


---



### 2. System Requirements

ระบบที่พัฒนาควรมีความสามารถดังต่อไปนี้

- ผู้ใช้งานต้อง Login ก่อนเข้าใช้งาน
- แสดงรายการ Post ทั้งหมด
- ดูรายละเอียดของแต่ละ Post
- แสดงผล HTML Content ได้อย่างถูกต้อง
- Filter Post ตาม Tag ได้

---



### 3. Database

สามารถเลือกใช้ Database ได้ตามความเหมาะสม เช่น

- PostgreSQL
- MySQL
- MongoDB
- SQLite
- หรือ Database อื่นที่ถนัด

---



### 4. Backend

พัฒนา REST API ด้วย **Node.js**

สามารถเลือก Framework ได้ตามความถนัด เช่น

- Express
- NestJS
- Fastify
- Hono
- หรือ Framework อื่นที่เหมาะสม

สิ่งที่ต้องมี

- Seed ข้อมูลจากไฟล์ `posts.json` ลง Database
- เลือกใช้ ORM หรือ Database Library ที่เหมาะสม เช่น Prisma, Drizzle, TypeORM หรือเครื่องมืออื่น
- ออกแบบ Data Model หรือ Entity สำหรับข้อมูล Post
- สร้าง REST API สำหรับใช้งานในระบบ
- จัดการ Error Response อย่างเหมาะสม
- Validate ข้อมูลที่รับเข้ามาใน API ตามความเหมาะสม

> สามารถออกแบบ API เพิ่มเติมได้ตามความเหมาะสม

---
### 5. Frontend

พัฒนา Web Application โดยเลือกใช้ Framework อย่างใดอย่างหนึ่ง

- Next.js (React)
- Nuxt (Vue)

สิ่งที่ต้องมี

- เชื่อมต่อข้อมูลผ่าน Backend API
- รองรับทุกความสามารถตามหัวข้อ System Requirements
- มีหน้า Login
- มีหน้าแสดงรายการ Post
- มีหน้ารายละเอียด Post
- สามารถ Filter Post ตาม Tag ได้
- แสดงผล HTML Content ได้อย่างเหมาะสม
- ออกแบบ UI ได้อย่างอิสระ

สามารถเลือก Library สำหรับหัวข้อต่อไปนี้ได้ตามความเหมาะสม

- State Management
- UI Framework
- Data Fetching
- Form Validation
- Styling

---



### 6. Docker Compose

จัดเตรียมไฟล์ `docker-compose.yml` หรือ `compose.yml` เพื่อให้สามารถเริ่มต้นระบบทั้งหมดได้อย่างสะดวก

Docker Compose ควรรองรับ Service ที่จำเป็น เช่น

- Frontend
- Backend
- Database

ผู้ตรวจควรสามารถเริ่มต้นระบบได้ด้วยคำสั่งใกล้เคียงกับตัวอย่างต่อไปนี้

```bash
docker compose up --build
```

กรุณาระบุรายละเอียดต่อไปนี้ไว้ใน README

- คำสั่งสำหรับเริ่มต้นระบบ
- Port ของแต่ละ Service
- Environment Variables ที่จำเป็น
- วิธี Seed ข้อมูล
- วิธีหยุดและล้างข้อมูลของระบบ
- ข้อจำกัดหรือสิ่งที่ควรทราบเกี่ยวกับ Docker Setup

> สามารถแยก Dockerfile ของ Frontend และ Backend ได้ตามโครงสร้างของโปรเจกต์

---



## สิ่งที่สามารถเลือกทำเพิ่มเติม (Optional)

หัวข้อนี้ไม่มีผลต่อการผ่านหรือไม่ผ่าน แต่จะช่วยให้เราเห็นแนวคิดในการออกแบบระบบมากขึ้น

ตัวอย่างเช่น

- Pagination
- Search
- Sorting
- Responsive Design
- Loading State
- Empty State
- Error State
- Refresh Token Authentication
- Unit Test
- Integration Test
- End-to-End Test
- API Documentation ด้วย Swagger หรือ OpenAPI
- Logging
- Caching
- CI/CD
- Database Migration
- Health Check Endpoint
- Rate Limiting

สามารถเลือกทำหัวข้ออื่นเพิ่มเติมได้ หากเห็นว่าเหมาะสม

---



## สิ่งที่เราจะพิจารณา

เราไม่ได้พิจารณาเฉพาะความครบของฟีเจอร์ แต่ให้ความสำคัญกับคุณภาพของงานโดยรวม เช่น

- Code Quality
- Project Structure
- Architecture and Design Pattern
- Data Modeling
- API Design
- Security
- Performance
- Readability and Maintainability
- Error Handling
- Git Commit History
- Problem Solving and Decision Making
- ความสะดวกในการติดตั้งและเริ่มต้นระบบ
- ความสามารถในการอธิบาย Trade-off ของสิ่งที่เลือกใช้

---



## README

README ของโปรเจกต์ควรประกอบด้วยข้อมูลอย่างน้อยดังต่อไปนี้

- ภาพรวมของโปรเจกต์
- Technology Stack ที่เลือกใช้
- โครงสร้างโปรเจกต์โดยสรุป
- วิธีติดตั้งโปรเจกต์
- วิธีตั้งค่า Environment Variables
- วิธีรันผ่าน Docker Compose
- วิธีรัน Frontend และ Backend แบบไม่ใช้ Docker หากรองรับ
- วิธี Seed ข้อมูลจากไฟล์ `posts.json`
- ข้อมูลสำหรับ Login หรือ Test Account
- รายละเอียด API โดยสรุป
- แนวคิดในการออกแบบระบบ
- Library หรือ Technology ที่เลือกใช้ พร้อมเหตุผล
- สิ่งที่เลือกทำเพิ่มเติม
- สิ่งที่ยังไม่ได้ทำ
- แนวทางที่จะพัฒนาต่อ
- Trade-off หรือข้อจำกัดที่พบระหว่างการพัฒนา

ตัวอย่างคำสั่งที่ควรระบุใน README

```bash
cp .env.example .env
docker compose up --build
```

กรุณาแนบไฟล์ `.env.example` โดยไม่ใส่ Secret หรือข้อมูลสำคัญที่ใช้งานจริง

---



## หมายเหตุ

- สามารถเลือกใช้ Library หรือ Framework ได้ตามความเหมาะสม
- หากมีการตัดสินใจด้าน Architecture หรือมี Trade-off ที่น่าสนใจ สามารถอธิบายไว้ใน README ได้
- สามารถตกแต่ง UI ได้อย่างอิสระ โดยเราไม่ได้เน้นความสวยงามเป็นหลัก

---



## การส่งงาน

เมื่อทำ Assignment เสร็จเรียบร้อยแล้ว กรุณาส่งสิ่งต่อไปนี้

- ลิงก์ GitHub Repository
- README ตามที่ระบุในโจทย์

ส่งมาที่

**To:** [top.k@sparkjoy.in.th](mailto:top.k@sparkjoy.in.th)  
**CC:** [bright.t@sparkjoy.in.th](mailto:bright.t@sparkjoy.in.th)

หัวข้ออีเมลแนะนำ

```text
Full Stack Technical Assignment - [ชื่อผู้สมัคร]
```

เพื่อความสะดวกในการตรวจงาน แนะนำให้ตั้งค่า Repository เป็น **Public**

หากไม่สามารถเปิด Repository เป็น Public ได้ กรุณาเพิ่มสิทธิ์การเข้าถึงให้กับผู้ตรวจ หรือระบุวิธีการเข้าถึง Repository ไว้ในอีเมล

ก่อนส่งงาน กรุณาตรวจสอบว่าโปรเจกต์สามารถเริ่มต้นได้ตามขั้นตอนใน README และสามารถรันผ่าน Docker Compose ได้

---



## สอบถามเพิ่มเติม

หากมีข้อสงสัยเกี่ยวกับ Assignment สามารถสอบถามเพิ่มเติมได้ตลอด เรายินดีช่วยเหลือและชี้แจงรายละเอียดของโจทย์

---



## ขอให้สนุกกับการทำ Assignment 🎉

ขอขอบคุณที่สละเวลาร่วมกระบวนการสัมภาษณ์กับทีม **SparkJoy**

หวังว่าจะได้เห็นแนวคิดและรูปแบบการพัฒนาของคุณ

ขอให้โชคดีครับ 🙏