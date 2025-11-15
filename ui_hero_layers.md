# Hướng dẫn 3 bước xây UI Hero theo 3 Layer

## ✅ Khi xây 1 đoạn UI (ví dụ Hero), làm theo 3 bước đơn giản:

1) **Đặt khung (Layout)**
2) **Đặt chữ (Content)**
3) **Trang trí (Surface)**

Không cần suy nghĩ phức tạp.

---

## 1) 🧱 LAYOUT = dựng khung + vị trí, chưa cần đẹp

Bạn chỉ cần xác định:

- Cái nào là nền
- Cái nào là nội dung
- Nội dung đặt ở đâu (giữa / trái / phải)

**Ví dụ Layout Hero:**

```html
<header class="relative">
  <figure class="aspect-video overflow-hidden"></figure>
  <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2">
    <section class="max-w-2xl text-center space-y-3"></section>
  </div>
</header>
```

Vậy là xong Layout.  
Chưa có màu, chưa có chữ, chưa có ảnh → nhưng **vị trí đã đúng**.

---

## 2) 📝 CONTENT = thêm chữ, câu, ý nghĩa

```html
<section class="max-w-2xl text-center space-y-3">
  <h1>Tiêu đề nổi bật</h1>
  <p>Đoạn mô tả ngắn.</p>
</section>
```

Chỉ thêm chữ, **không thêm màu**.

---

## 3) 🎨 SURFACE = trang trí: ảnh, overlay, màu, đổ bóng

```html
<figure>
  <img class="size-full object-cover" src="..." />
</figure>

<div class="absolute inset-0 bg-gradient-to-t from-black/40 to-transparent"></div>

<h1 class="text-white text-4xl font-bold"></h1>
<p class="text-white/80"></p>
```

---

## 🎯 Tóm gọn trong 1 câu dễ nhớ

```
Layout = đặt đồ đúng chỗ
Content = để chữ vào
Surface = làm cho đẹp
```

---

## 🧩 Full code hoàn chỉnh — rõ ràng — dễ đọc

```html
<header class="relative">

  <!-- 1) Layout -->
  <figure class="aspect-video overflow-hidden">
    <!-- 3) Surface -->
    <img
      class="size-full object-cover object-[center_top]"
      src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?q=80&w=1920&auto=format&fit=crop"
      alt=""
    />
  </figure>

  <!-- 3) Surface -->
  <div class="absolute inset-0 bg-gradient-to-t from-black/40 to-transparent"></div>

  <!-- 1) Layout: căn giữa -->
  <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2">

    <!-- 2) Content -->
    <section class="max-w-2xl text-center space-y-3">
      <h1 class="text-3xl font-bold text-white sm:text-4xl">
        Tiêu đề nổi bật
      </h1>
      <p class="text-white/90">
        Đoạn mô tả ngắn gọn để người dùng hiểu nhanh.
      </p>
    </section>

  </div>

</header>
```

---

Nếu bạn muốn, mình làm tiếp bản:

- **Hero-left** (chữ căn trái)
- **Hero-bottom** (chữ ở đáy)

Chỉ cần trả lời: `left` hoặc `bottom` 😊
