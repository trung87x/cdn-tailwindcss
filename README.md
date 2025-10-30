# 🧩 Tailwind CSS Master Labs

Tài liệu thực hành chuyên sâu cho từng nhóm chủ đề CSS, được chuyển hoá thành utility trong Tailwind v4+.  
Mỗi lab gồm: **Mục tiêu học tập**, **Checklist class quan trọng**, và **Trang mẫu demo**.

---

## 1️⃣ Layout & Positioning Lab — _Trang “Cards + TOC”_

**Mục tiêu:** Nắm bố cục, stacking, cuộn.

**Checklist:**

- aspect-ratio: `aspect-[16/9]`, `aspect-square`
- columns: `columns-2`, `columns-[14rem]`
- break-_: `break-inside-avoid`, `break-after-page` _(bonus: in/print)\*
- box-sizing: `box-border`, `box-content`
- display: `grid`, `flex`, `contents`, `hidden`
- float/clear: `float-right`, `clear-both`
- isolation: `isolate`
- object-fit/position: `object-cover`, `object-[center_top]`
- overflow/overscroll: `overflow-x-auto`, `overscroll-contain`
- position + inset + transform: `sticky`, `absolute`, `inset-0`, `top-1/2`, `-translate-y-1/2`
- visibility: `visible`, `invisible`, `collapse`
- z-index: `z-10`, `z-[9999]`

**Trang mẫu:** Danh sách bài viết có TOC sticky, hero 16:9, lưới thẻ, bảng cuộn ngang.

---

## 2️⃣ Flexbox & Grid Catalog — _Gallery bố cục_

**Mục tiêu:** Thuần thục Flex/Grid & auto flow.

**Checklist:**

- basis: `basis-1/2`, `basis-[320px]`
- direction/wrap: `flex-row`, `flex-col`, `flex-wrap`, `flex-nowrap`
- flex: `flex-1`, `flex-[2_2_0%]`
- grow/shrink: `grow`, `shrink-0`
- order: `order-1`, `order-[999]`
- grid templates: `grid-cols-3`, `grid-rows-[auto_1fr_auto]`
- grid line placement: `col-span-2`, `col-start-2 col-end-4`, `row-span-3`
- auto-flow/cols/rows: `grid-flow-col`, `auto-cols-fr`, `auto-rows-min`
- gap: `gap-6`, `gap-x-4 gap-y-2`
- justify-/align-/place-\*: `justify-center`, `justify-items-stretch`, `justify-self-end`, `items-center`, `content-between`, `self-start`, `place-content-center`, `place-items-start`, `place-self-center`

**Trang mẫu:** Gallery ảnh + footer sticky bằng grid areas.

---

## 3️⃣ Spacing & Sizing Playground — _Card responsive_

**Mục tiêu:** Khoảng cách & kích thước “an toàn”.

**Checklist:**

- padding: `p-6`, `px-4`, `pt-[3.5rem]`
- margin: `m-0`, `mx-auto`, `-mt-2`, `mb-[2ch]`
- width/min/max: `w-64`, `min-w-0`, `max-w-2xl`, `w-[min(50vw,40rem)]`
- height/min/max: `h-10`, `min-h-[50svh]`, `max-h-96`

**Trang mẫu:** Thẻ sản phẩm với container co giãn, tiêu đề hai dòng.

---

## 4️⃣ Typography Specimen — _Trang “Type Scale + Links”_

**Mục tiêu:** Hệ chữ hoàn chỉnh.

**Checklist:**

- font-family: `font-sans`, `font-[var(--font-display)]`
- font-size: `text-sm md:text-lg`, `text-[13px]`
- smoothing: `antialiased`, `subpixel-antialiased`
- style/weight/stretch: `italic`, `not-italic`, `font-medium`, `font-[550]`, `[font-stretch:condensed]`
- numeric: `ordinal`, `tabular-nums`, `slashed-zero`
- letter spacing: `tracking-wide`, `tracking-[.02em]`
- clamp/leading: `line-clamp-3`, `leading-6`, `leading-[1.15]`
- list-style: `list-disc`, `list-inside`, `list-[square]`
- align: `text-left md:text-center`
- color: `text-gray-700`, `text-[color:var(--color-brand-600)]`
- decoration: `underline`, `decoration-dotted`, `decoration-2`, `decoration-[--color-brand-500]`, `underline-offset-4`, `underline-offset-[6px]`
- transform/overflow/wrap/indent/vertical: `uppercase`, `normal-case`, `truncate`, `text-ellipsis`, `text-clip`, `text-balance`, `text-pretty`, `text-nowrap`, `indent-8`, `indent-[2ch]`, `align-middle`, `align-[3px]`
- white-space/breaks/hyphens: `whitespace-nowrap`, `whitespace-pre-wrap`, `break-words`, `break-all`, `hyphens-auto`, `hyphens-none`
- content (pseudo): `before:[content:"New"]`

**Trang mẫu:** Trang giới thiệu brand type + link states + bảng số.

---

## 5️⃣ Backgrounds & Masks Gallery

**Mục tiêu:** Nền, gradient, clip, mask.

**Checklist:**

- attachment/clip/color: `bg-fixed`, `bg-local`, `bg-clip-padding`, `bg-clip-text`, `bg-gray-100`, `bg-[var(--color-brand-50)]`
- image/origin/position/repeat/size: `bg-[url(/dots.svg)]`, `bg-none`, `bg-gradient-to-r`, `bg-origin-border`, `bg-center`, `bg-[left_2rem_top_1rem]`, `bg-no-repeat`, `bg-repeat-x`, `bg-cover`, `bg-[length:200%_100%]`
- masks (fallback arbitrary): `[mask-image:linear-gradient(#000,transparent)]`, `[mask-type:luminance]`

**Trang mẫu:** Hero với text gradient + card có mask-fade.

---

## 6️⃣ Borders & Outline Showroom

**Mục tiêu:** Biên, góc, kiểu đường viền & outline.

**Checklist:**

- radius: `rounded-lg`, `rounded-[--radius-md]`, `rounded-s-2xl`
- width: `border`, `border-0`, `border-x-2`
- color: `border-gray-300`, `border-[color:oklch(0.7_0.2_250)]`
- style: `border-dashed`, `border-double`, `border-[inset]`
- outline: `outline-2`, `outline-blue-500`, `outline-dashed`, `outline-offset-2`

**Trang mẫu:** Bộ nút / thẻ trạng thái với focus ring chuẩn a11y.

---

## 7️⃣ Effects, Blend & Filters Lab

**Mục tiêu:** Đổ bóng, mờ, hòa trộn, backdrop.

**Checklist:**

- shadow: `shadow`, `shadow-lg`, `shadow-[0_2px_0_#0003]`
- text-shadow (fallback): `[text-shadow:0_1px_2px_rgb(0_0_0/.15)]`
- opacity: `opacity-60`, `opacity-[.35]`
- mix/background-blend: `mix-blend-multiply`, `mix-blend-[plus-lighter]`, `bg-blend-overlay`
- filter/backdrop: `blur`, `brightness-110`, `contrast-125`, `grayscale`, `hue-rotate-15`, `invert`, `saturate-150`, `sepia`, `drop-shadow-md`, `blur-[3px]`, `backdrop-blur`, `backdrop-brightness-125`

**Trang mẫu:** Card glassmorphism trên ảnh nền.

---

## 8️⃣ Data Table Pro — _Bảng nâng cao_

**Mục tiêu:** Bảng chuẩn, spacing, layout cố định.

**Checklist:**

- collapse/separate: `border-collapse`, `border-separate`
- border-spacing: `border-spacing-2`, `border-spacing-x-4`, `border-spacing-[0_8px]`
- table layout: `table-auto`, `table-fixed`
- caption side: `caption-top`, `caption-bottom`

**Trang mẫu:** Bảng có caption, cột cố định, cuộn ngang.

---

## 9️⃣ Transitions & Animations Micro-UI

**Mục tiêu:** Vi chuyển động chuẩn UX.

**Checklist:**

- property/behavior: `transition`, `transition-colors`, `transition-[transform,opacity]`, `[transition-behavior:allow-discrete]`
- duration/ease/delay: `duration-300`, `duration-[75ms]`, `ease-in-out`, `ease-[cubic-bezier(.2,.8,.2,1)]`, `delay-150`
- animation: `animate-spin`, `animate-pulse`, `animate-[wiggle_1s_ease-in-out_infinite]`

**Trang mẫu:** Nút, tooltip, accordion, toast với enter/exit mượt.

---

## 🔟 2D/3D Transforms Deck

**Mục tiêu:** Transform, origin, perspective.

**Checklist:**

- backface/perspective/origin/style (fallback): `[backface-visibility:hidden]`, `[perspective:800px]`, `[perspective-origin:50%_0]`, `[transform-style:preserve-3d]`
- rotate/scale/skew/translate: `-rotate-3`, `scale-95`, `skew-x-6`, `translate-y-1/2`
- origin: `origin-center`, `origin-[20%_80%]`

**Trang mẫu:** Card flip 3D + gallery hover tilt.

---

## 11️⃣ Interactivity & Forms Lab

**Mục tiêu:** Form controls & hành vi cuộn/chạm.

**Checklist:**

- accent/appearance/caret: `accent-blue-600`, `accent-[var(--brand-500)]`, `appearance-none`, `caret-indigo-600`, `caret-[oklch(...)]`
- color-scheme: `color-scheme-dark`, `color-scheme-[light_only]`
- cursor: `cursor-pointer`, `curs
