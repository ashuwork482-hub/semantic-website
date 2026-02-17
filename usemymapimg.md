HTML me `<map>` tag image ke different parts ko clickable banane ke liye use hota hai. Isko **Image Map** kehte hain.

Agar **ek hi image me 3 different cheezein** hain (for example: mobile, laptop, watch) aur aap chahte ho har cheez alag link par jaye, to aap `<area>` tag ke through unke coordinates define karte ho.

---

## 🔹 Step 1: Basic Structure

```html
<img src="devices.jpg" usemap="#mymap">

<map name="mymap">
    <area shape="rect" coords="34,44,270,350" href="mobile.html">
    <area shape="rect" coords="290,172,333,250" href="laptop.html">
    <area shape="circle" coords="500,200,60" href="watch.html">
</map>
```

---

## 🔹 Important Attributes Samjho

### 1️⃣ `usemap="#mymap"`

* `img` ko batata hai ke ye image kis map se connected hai.
* `#mymap` ka name `<map name="mymap">` ke equal hona chahiye.

---

### 2️⃣ `<area>` Tag

Ye image ke andar specific area define karta hai.

#### ➤ `shape`

3 types hote hain:

* `rect` → rectangle
* `circle` → circle
* `poly` → custom shape

---

### 3️⃣ `coords`

Yahan **X aur Y axis ke numbers** likhte hain.

---

## 🔹 Rectangle (rect) Coordinates

```html
shape="rect"
coords="x1,y1,x2,y2"
```

📌 Example:

```html
coords="34,44,270,350"
```

Matlab:

* 34 = left se distance
* 44 = top se distance
* 270 = right end
* 350 = bottom end

👉 Pehla point (top-left)
👉 Doosra point (bottom-right)

---

## 🔹 Circle Coordinates

```html
shape="circle"
coords="centerX,centerY,radius"
```

📌 Example:

```html
coords="500,200,60"
```

* 500 = center X
* 200 = center Y
* 60 = radius

---

## 🔹 Polygon (Custom Shape)

```html
shape="poly"
coords="x1,y1,x2,y2,x3,y3,x4,y4"
```

Ye multiple points connect karta hai.

---

# 🔥 3 Cheezein Ek Image Me Define Karna

Suppose image width 800px hai.

```html
<img src="example.jpg" usemap="#examplemap">

<map name="examplemap">
    
    <!-- Left side object -->
    <area shape="rect" coords="0,0,250,400" href="item1.html">
    
    <!-- Center object -->
    <area shape="rect" coords="260,0,500,400" href="item2.html">
    
    <!-- Right side object -->
    <area shape="rect" coords="510,0,800,400" href="item3.html">

</map>
```

Is tarah ek image ko 3 parts me divide kar diya.

---

# 🔥 Coordinates Kaise Find Karein?

### ✅ Method 1 (Easy Way)

Image ko browser me open karo
Right click → Inspect → Mouse ko move karo
Console me X Y position show hoti hai

### ✅ Method 2

Online tool use karo:
Search karo:
"HTML image map generator"

Example tool:

* image-map.net

Ye automatically coordinates de deta hai.

---

# 🎯 Important Note

Coordinates **pixels me hote hain**
Start hota hai top-left corner se (0,0)

👉 X axis → left se right
👉 Y axis → top se bottom

---

Agar chaho to mai ek practical demo image bana kar step-by-step coordinate samjha du Roman Urdu me with diagram type explanation 😊
