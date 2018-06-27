
[Adding meta box](#snippet-adding-meta-box)
# API
- [Meta box](#meta-box)
    - [Add](#meta-box-add)


### Meta box
<h4 id="meta-box-add">Add</h4>

เพิ่ม meta box ลงไปในหน้าที่เราต้องการ  
```php
function prefix_add_meta_boxes() {
    add_meta_box(
        'my_meta_box', // HTML ID attribute ของ meta box element
        'My meta box', // ชื่อของ meta box
        'prefix_meta_box_content_callback', // ชื่อของ callback ที่ใช้ echo content ของ meta box
        'post', // หน้าจอที่จะให้ meta box นี้ปรากฏอยู่
        'normal', // Context หรือตำแหน่งที่จะแสดง meta box
        10, // Priority หรือลำดับตำแหน่งของ meta box ในแนวดิ่ง ว่าจะให้อยู่อันแรก อันท้าย หรืออันที่ n
        [
            'a' => 'hahaha',
            'b' => 'hehehe'
        ] // Array ของ arguments ที่จะใส่ไปใน callback ที่ใช้แสดง content ของ meta box นี้
    );
}

add_action( 'add_meta_boxes', 'prefix_add_meta_boxes' );
```

ดู:
- https://developer.wordpress.org/reference/functions/add_meta_box/
- https://wordpress.stackexchange.com/questions/186026/add-special-meta-box-to-custom-post-type
