# Full Stack Technical Assignment

## วัตถุประสงค์

แบบทดสอบนี้มีไว้เพื่อให้เราได้เห็นแนวทางการพัฒนา Full Stack ของผู้สมัคร ทั้งในด้าน Frontend, Backend, การออกแบบโครงสร้างโปรเจกต์ และการเชื่อมต่อระหว่างระบบ

ไม่มีคำตอบที่ถูกหรือผิดเพียงแบบเดียว เราให้ความสำคัญกับแนวคิด กระบวนการคิด และเหตุผลในการออกแบบ มากกว่าการทำฟีเจอร์ให้ครบทุกอย่าง

เราไม่ได้คาดหวังให้ Assignment นี้สมบูรณ์แบบ หากมีข้อจำกัดด้านเวลา สามารถอธิบายสิ่งที่เลือกทำ สิ่งที่ยังไม่ได้ทำ และแนวทางที่จะพัฒนาต่อไว้ใน README ได้

---

## ระยะเวลาที่แนะนำ

Assignment นี้ออกแบบให้ใช้เวลาประมาณ **4–8 ชั่วโมง**

ไม่จำเป็นต้องทำทุกอย่างให้ครบ หากมีเวลาจำกัด สามารถเลือกทำเฉพาะส่วนที่ต้องการแสดงศักยภาพ และอธิบายเหตุผลไว้ใน README

หากมีเวลาจำกัด แนะนำให้จัดลำดับความสำคัญดังนี้

1. ฟีเจอร์หลักตาม System Requirements ทำงานได้จริง
2. คุณภาพโค้ด การออกแบบ Data Model และ API
3. Docker Compose
4. หัวข้อ Plus

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

> สิ่งที่ควรทราบเกี่ยวกับข้อมูล
>
> - ข้อมูลมีจำนวนประมาณ 10,000 Posts การออกแบบวิธี Seed และวิธีแสดงผลควรคำนึงถึงปริมาณข้อมูลนี้ด้วย
> - ข้อมูลไม่มี Field `id` มาให้ การออกแบบ Primary Key และความสัมพันธ์ของข้อมูล เช่น Tags เป็นส่วนหนึ่งของการออกแบบ Data Model ที่เราสนใจ

---



### 2. System Requirements

ระบบที่พัฒนาควรมีความสามารถดังต่อไปนี้

- ผู้ใช้งานต้อง Login ก่อนเข้าใช้งาน
- แสดงรายการ Post ทั้งหมด
- ดูรายละเอียดของแต่ละ Post
- แสดงผล HTML Content ได้อย่างถูกต้องและปลอดภัย
- Filter Post ตาม Tag ได้

> เกี่ยวกับ Login
>
> - เราไม่ได้เตรียมข้อมูลผู้ใช้มาให้ ผู้สมัครสามารถ Seed Test Account ขึ้นมาเองได้ และระบุข้อมูลสำหรับ Login ไว้ใน README
> - เลือกวิธี Authentication ได้อย่างอิสระ เช่น Session หรือ JWT พร้อมอธิบายเหตุผลที่เลือกใช้
> - ไม่จำเป็นต้องมีหน้า Register

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

- Seed ข้อมูลจากไฟล์ `posts.json` ลง Database โดยควรรันได้ด้วยคำสั่งเดียวหรือรันอัตโนมัติเมื่อเริ่มระบบ
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



## สิ่งที่สามารถเลือกทำเพิ่มเติม (Plus)

หัวข้อนี้ไม่มีผลต่อการผ่านหรือไม่ผ่าน แต่จะช่วยให้เราเห็นแนวคิดในการออกแบบระบบมากขึ้น

ตัวอย่างเช่น

**User Experience**

- Pagination หรือ Infinite Scroll
- Search
- Sorting
- Responsive Design
- Loading State / Empty State / Error State

**Testing**

- Unit Test
- Integration Test
- End-to-End Test

**API & Security**

- API Documentation ด้วย Swagger หรือ OpenAPI
- Refresh Token Authentication
- Rate Limiting
- Health Check Endpoint

**Infrastructure**

- Logging
- Caching
- CI/CD
- Database Migration

สามารถเลือกทำหัวข้ออื่นเพิ่มเติมได้ หากเห็นว่าเหมาะสม

---



## สิ่งที่เราจะพิจารณา

เราไม่ได้พิจารณาเฉพาะความครบของฟีเจอร์ แต่ให้ความสำคัญกับคุณภาพของงานโดยรวม

สิ่งที่เราให้น้ำหนักเป็นพิเศษ

- Code Quality, Readability and Maintainability
- Data Modeling และ API Design
- Security
- ความสะดวกในการติดตั้งและเริ่มต้นระบบ

สิ่งที่เราพิจารณาประกอบ

- Project Structure / Architecture and Design Pattern
- Error Handling
- Performance
- Git Commit History
- Problem Solving and Decision Making
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
- สามารถใช้ AI Tools ช่วยพัฒนาได้ แต่ผู้สมัครควรเข้าใจโค้ดทุกส่วนและอธิบายการตัดสินใจในการออกแบบได้ เนื่องจากอาจมีการพูดคุยเจาะลึกถึงงานชิ้นนี้ในขั้นตอนสัมภาษณ์

---
## การส่งงาน

เมื่อทำ Assignment เสร็จแล้ว รบกวนส่งลิงก์ GitHub Repository มาที่ top.k@sparkjoy.in.th และ cc ไปที่ bright.t@sparkjoy.in.th พร้อม README ตามที่ระบุในโจทย์

แนะนำให้ตั้งค่า Repository เป็น Public เพื่อความสะดวกในการตรวจงาน

หากมีข้อสงสัยเกี่ยวกับโจทย์ สามารถสอบถามเพิ่มเติมได้ตลอดครับ 

ขอให้สนุกกับการทำ Assignment และขอบคุณที่สละเวลาร่วมกระบวนการสัมภาษณ์กับทีม SparkJoy 🙏