# Glossary

**Glossary**  
[Nonce](#nonce)

<h3 id="nonce">Nonce</h3>

Nonce คือ token ที่ระบบของ WordPress สร้างขึ้นมาไว้สำหรับใส่ลงไปใน form ต่าง ๆ เป็นหนึ่งใน field ของ form ซึ่งมักจะเป็น hidden field ไม่มีใครเห็น เนื่องจากว่าไม่มีประโยชน์ในแง่การใช้งานของ user แต่มีไว้เพื่อประโยชน์ทางด้านความปลอดภัย เมื่อ submit form แล้ว nonce token ก็จะถูกส่งไปกับ request ของ form ด้วย เมื่อระบบ WordPress ได้รับ request นั้น ก็จะเช็กดูได้ว่ามี nonce ที่ระบบเพิ่งสร้างแนบมาด้วยหรือเปล่า ถ้าไม่มีก็สันนิษฐานไว้ก่อนเลยว่า request นี้ไม่ได้มาจากหน้าเว็บของระบบ หมายความว่าเป็น request ที่ไม่น่าเชื่อถือ อาจจะไว้ใจไม่ได้นั่นเอง  

อย่างใน WordPress ก็จะมี function ชื่อ `wp_nonce_field` เพียงเรา call function นี้ไปใน HTML Form ตัว function ก็จะ `echo` nonce token ที่ระบบสร้างขึ้นมาให้เอง เป็นอันเรียบร้อย