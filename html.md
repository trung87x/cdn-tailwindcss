# HTML5 Semantic Elements — Cheatsheet (Tiếng Việt)

> Tài liệu tóm tắt các **thẻ semantic** trong HTML5 để làm layout chuẩn **SEO** và **Accessibility (A11y)**.  
> Dùng cho học nhanh hoặc làm reference khi code.

---

## 1) Thẻ semantic là gì?
**Thẻ semantic** là thẻ HTML mang **ý nghĩa** về nội dung được bao bọc, giúp trình duyệt, máy đọc màn hình và công cụ tìm kiếm hiểu vai trò của nó.  
Khác với `<div>` hoặc `<span>` là container "trung tính", không mang nghĩa.

Ví dụ nhanh:
```html
<header>...</header>   <!-- header của trang hoặc của một section -->
<article>...</article> <!-- một bài viết/khối nội dung độc lập -->
<footer>...</footer>   <!-- phần chân trang hoặc chân section -->
```

---

## 2) Nhóm thẻ semantic phổ biến

### 2.1 Cấu trúc tổng thể trang
| Thẻ | Ý nghĩa | Ví dụ sử dụng |
|---|---|---|
| `<header>` | Phần đầu của trang hoặc của một section (logo, nav, tiêu đề) | Logo + Menu + Title |
| `<nav>` | Khu vực điều hướng (navigation) | Menu chính, breadcrumbs |
| `<main>` | Nội dung chính của trang (mỗi trang **chỉ 1** cái) | Toàn bộ phần content chính |
| `<section>` | Một khu vực nội dung cùng chủ đề | About, Services, Testimonials |
| `<article>` | Khối nội dung độc lập, có thể tồn tại riêng | Blog post, Tin tức, Card sản phẩm |
| `<aside>` | Nội dung phụ, không thuộc luồng chính | Sidebar, liên kết liên quan, quảng cáo |
| `<footer>` | Phần chân trang hoặc chân section | Bản quyền, liên hệ, social links |

### 2.2 Nội dung & văn bản
| Thẻ | Ý nghĩa | Ví dụ |
|---|---|---|
| `<h1>`–`<h6>` | Tiêu đề cấp 1–6 | `<h1>Portfolio của Trung</h1>` |
| `<p>` | Đoạn văn bản | `<p>Giới thiệu ngắn.</p>` |
| `<blockquote>` | Trích dẫn dài (khối) | `<blockquote>“Design is thinking made visual.”</blockquote>` |
| `<q>` | Trích dẫn ngắn trong dòng | `<p>Ông nói: <q>Học HTML dễ thôi.</q></p>` |
| `<abbr>` | Viết tắt có chú thích | `<abbr title="HyperText Markup Language">HTML</abbr>` |
| `<address>` | Thông tin liên hệ | `<address>Email: trung@example.com</address>` |
| `<cite>` | Nguồn tham khảo, tên tác phẩm | `<cite>— Steve Jobs</cite>` |
| `<time>` | Biểu diễn thời gian | `<time datetime="2025-11-09">9 Nov 2025</time>` |

### 2.3 Phân nhóm nội dung
| Thẻ | Ý nghĩa | Ví dụ |
|---|---|---|
| `<div>` | Container khối **không mang nghĩa** | Dùng khi không có thẻ semantic phù hợp |
| `<span>` | Container inline **không mang nghĩa** | `<span class="highlight">quan trọng</span>` |
| `<figure>` | Gói hình ảnh/biểu đồ kèm chú thích | |
| `<figcaption>` | Chú thích cho `<figure>` | “Hình 1. Bãi biển Cancun” |
| `<hr>` | Ngắt về mặt ngữ nghĩa giữa hai phần | Ngăn cách chủ đề |
| `<br>` | Xuống dòng trong văn bản | Dùng hạn chế |

### 2.4 Form & tương tác người dùng
| Thẻ | Ý nghĩa | Ghi chú |
|---|---|---|
| `<form>` | Biểu mẫu nhập liệu | Bao quanh toàn bộ input |
| `<label>` | Nhãn cho input | Cần `for` khớp `id` input |
| `<input>` | Ô nhập liệu | `type="text|email|password|..."` |
| `<textarea>` | Vùng nhập nhiều dòng |  |
| `<button>` | Nút bấm | Submit / hành động |
| `<fieldset>` | Nhóm các input có liên quan |  |
| `<legend>` | Tiêu đề cho fieldset |  |

### 2.5 Phần tử HTML5 khác hữu ích
| Thẻ | Công dụng | Ví dụ |
|---|---|---|
| `<details>` | Khối có thể thu gọn/mở rộng | Accordion cơ bản |
| `<summary>` | Tiêu đề cho `<details>` | Tiêu đề nhấn để mở |
| `<dialog>` | Hộp thoại (modal) native HTML | `<dialog open>Welcome!</dialog>` |
| `<mark>` | Tô sáng văn bản | `<mark>quan trọng</mark>` |
| `<data>` | Gắn dữ liệu máy-đọc được | `<data value="42">Trung</data>` |

---

## 3) Lưu ý về SEO & A11y (rất quan trọng)
- **Mỗi trang chỉ nên có 1 `<main>` và 1 `<h1>` chính**.
- Dùng thứ tự heading **theo cấp bậc** (h1 → h2 → h3...), không nhảy cấp lung tung.
- **`<nav>`** nên có `aria-label` nếu có nhiều khu điều hướng (ví dụ: `aria-label="Chính"`, `aria-label="Breadcrumbs"`).
- Luôn viết **`alt` cho ảnh**; dùng `<figure>` + `<figcaption>` khi cần diễn giải.
- Dùng `<time datetime="YYYY-MM-DD">` để máy hiểu đúng mốc thời gian.

---

## 4) Ví dụ layout semantic hoàn chỉnh
```html
<body>
  <header>
    <nav aria-label="Chính">
      <a href="/">Trang chủ</a>
      <a href="#about">Giới thiệu</a>
      <a href="#contact">Liên hệ</a>
    </nav>
  </header>

  <main id="content">
    <section id="about">
      <h1>Xin chào, tôi là Trung</h1>
      <p>Front-end Developer & UI Designer.</p>
    </section>

    <article>
      <h2>Dự án nổi bật</h2>
      <figure>
        <img src="project.jpg" alt="Ảnh dự án" />
        <figcaption>Portfolio React + Tailwind</figcaption>
      </figure>
    </article>
  </main>

  <aside aria-label="Thông tin phụ">
    <h3>Liên hệ nhanh</h3>
    <address>Email: trung@example.com</address>
  </aside>

  <footer>
    <p>&copy; 2025 Trung Dinh. All rights reserved.</p>
  </footer>
</body>
```

---

## 5) Checklist nhanh khi code semantic
- [ ] Có `<main>` duy nhất chứa nội dung chính
- [ ] Heading theo cấp (h1 → h2 → h3…)
- [ ] Khu điều hướng gói trong `<nav>` (kèm `aria-label` nếu cần)
- [ ] Hình ảnh có `alt`; cụm ảnh dùng `<figure>` + `<figcaption>`
- [ ] Thời gian dùng `<time datetime="...">...`
- [ ] Nội dung phụ (sidebar/quảng cáo) dùng `<aside>`
- [ ] Footer/ Header rõ ràng cho trang hoặc cho từng section nếu cần

---

## 6) Mẹo áp dụng với React/Tailwind (tuỳ chọn)
- Trong React, bạn **vẫn dùng thẻ semantic** như thường lệ.
- Tailwind giúp style nhanh: ví dụ
  ```jsx
  <main className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10">
    <section className="space-y-4">
      <h1 className="text-3xl font-bold">Xin chào, tôi là Trung</h1>
      <p className="text-gray-600">Front-end Developer & UI Designer.</p>
    </section>
  </main>
  ```

---

> **Tip**: Nếu không chắc dùng thẻ nào, hãy tự hỏi: *“Phần này có vai trò gì trong trang?”* — nếu là nội dung chính → `<main>`; nhóm chủ đề → `<section>`; nội dung độc lập → `<article>`; điều hướng → `<nav>`; phụ trợ → `<aside>`.

Chúc bạn code semantic đẹp, chuẩn SEO/A11y! 🚀
