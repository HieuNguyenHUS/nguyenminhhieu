# 🌐 Hướng Dẫn Chỉnh Sửa Website Cá Nhân

> Tài liệu hướng dẫn sử dụng VS Code để chỉnh sửa, phát triển và triển khai website cá nhân của bạn.

---

## 📁 Mục Lục

1. [Cài đặt môi trường](#1-cài-đặt-môi-trường)
2. [Cấu trúc file](#2-cấu-trúc-file)
3. [Mở và xem trước website](#3-mở-và-xem-trước-website)
4. [Hướng dẫn chỉnh sửa từng phần](#4-hướng-dẫn-chỉnh-sửa-từng-phần)
5. [Thêm ảnh đại diện](#5-thêm-ảnh-đại-diện)
6. [Thay đổi màu sắc & font chữ](#6-thay-đổi-màu-sắc--font-chữ)
7. [Thêm bài báo mới](#7-thêm-bài-báo-mới)
8. [Thêm bài blog mới](#8-thêm-bài-blog-mới)
9. [Workflow làm việc](#9-workflow-làm-việc)
10. [Đưa lên web (khi sẵn sàng)](#10-đưa-lên-web-khi-sẵn-sàng)

---

## 1. Cài đặt môi trường

### Bước 1: Cài VS Code Extensions (khuyến nghị)

Mở VS Code → nhấn `Ctrl+Shift+X` → tìm và cài:

| Extension | Tác dụng |
|-----------|----------|
| **Live Server** (Ritwick Dey) | Xem trước website trực tiếp, tự động reload khi lưu |
| **HTML CSS Support** | Gợi ý code HTML/CSS |
| **Auto Rename Tag** | Tự đổi cả thẻ mở và đóng |
| **Prettier** | Format code đẹp hơn |

### Bước 2: Tạo thư mục dự án

```
📂 my-website/
├── 📄 index.html          ← file website chính (file bạn đã tải về)
├── 📂 images/             ← thư mục chứa ảnh
│   ├── profile.jpg        ← ảnh đại diện
│   └── blog/              ← ảnh cho blog posts
├── 📂 docs/               ← file CV PDF, tài liệu
│   └── CV-HarryNguyen.pdf
└── 📄 HUONG-DAN.md        ← file hướng dẫn này
```

### Bước 3: Mở thư mục trong VS Code

```bash
# Mở terminal, chạy:
cd đường/dẫn/tới/my-website
code .
```

Hoặc: Mở VS Code → `File` → `Open Folder` → chọn thư mục `my-website`

---

## 2. Cấu trúc file

File `index.html` gồm các phần chính (tìm bằng `Ctrl+F`):

| Từ khóa tìm kiếm | Phần tương ứng | Dòng khoảng |
|-------------------|----------------|-------------|
| `<!-- ─── NAVIGATION` | Thanh menu trên cùng | Đầu body |
| `<!-- ─── HERO` | Phần giới thiệu lớn | Sau nav |
| `<!-- ─── ABOUT` | Giới thiệu bản thân | Section 1 |
| `<!-- ─── RESEARCH` | Hướng nghiên cứu | Section 2 |
| `<!-- ─── PUBLICATIONS` | Danh sách bài báo | Section 3 |
| `<!-- ─── CV` | Timeline học vấn & kinh nghiệm | Section 4 |
| `<!-- ─── BLOG` | Blog & ghi chú nghiên cứu | Section 5 |
| `<!-- ─── CONTACT` | Thông tin liên hệ & form | Section 6 |
| `<!-- ─── FOOTER` | Chân trang | Cuối body |

**Mẹo:** Dùng `Ctrl+F` (tìm kiếm) và gõ `<!-- ───` để nhảy nhanh giữa các section.

---

## 3. Mở và xem trước website

### Cách 1: Live Server (khuyến nghị)

1. Mở file `index.html` trong VS Code
2. Click chuột phải → chọn **"Open with Live Server"**
3. Trình duyệt tự mở tại `http://127.0.0.1:5500`
4. **Mỗi khi lưu file (`Ctrl+S`), trang tự động reload**

### Cách 2: Mở trực tiếp

- Nhấn đúp vào file `index.html` trong File Explorer
- Mỗi lần sửa, cần refresh trình duyệt (`F5`)

---

## 4. Hướng dẫn chỉnh sửa từng phần

### 4.1 Thông tin cá nhân (Hero Section)

Tìm `<!-- ─── HERO` rồi sửa:

```html
<!-- Tên của bạn -->
<h1>Harry Nguyen</h1>

<!-- Chức danh -->
<p class="subtitle">Condensed Matter Physicist &amp; Materials Scientist</p>

<!-- Mô tả ngắn -->
<p class="tagline">
  Thay đổi nội dung mô tả tại đây...
</p>
```

> ⚠️ **Lưu ý:** Ký tự `&` phải viết thành `&amp;` trong HTML.

### 4.2 About Me

Tìm `<!-- ─── ABOUT` → sửa nội dung trong các thẻ `<p>`:

```html
<div class="about-text">
  <p>Đoạn giới thiệu thứ nhất...</p>
  <p>Đoạn giới thiệu thứ hai...</p>
  <p>Đoạn giới thiệu thứ ba...</p>
</div>
```

Sửa thông tin Quick Facts trong sidebar:

```html
<div class="info-row">
  <span class="info-label">Position</span>
  <span class="info-value">Sửa chức danh tại đây</span>
</div>
<div class="info-row">
  <span class="info-label">Institution</span>
  <span class="info-value">Tên trường / viện</span>
</div>
```

Thêm/xóa research tags:

```html
<span class="tag">Tên tag mới</span>
```

### 4.3 Research Cards

Tìm `<!-- ─── RESEARCH` → mỗi card có dạng:

```html
<div class="research-card">
  <div class="research-icon">⚛</div>                    <!-- Icon (emoji) -->
  <h3>Tên hướng nghiên cứu</h3>                         <!-- Tiêu đề -->
  <p>Mô tả chi tiết hướng nghiên cứu...</p>             <!-- Nội dung -->
  <span class="research-status status-active">Active</span> <!-- Trạng thái -->
</div>
```

**Thêm card mới:** Copy toàn bộ block `<div class="research-card">...</div>` và paste bên dưới.

**Đổi trạng thái:** Dùng `status-active` (xanh lá) hoặc `status-ongoing` (vàng).

### 4.4 CV Timeline

Tìm `<!-- ─── CV` → mỗi mục có dạng:

```html
<div class="cv-entry">
  <h4>Tên vị trí / bằng cấp</h4>
  <div class="cv-org">Tên tổ chức</div>
  <div class="cv-date">20XX – 20XX</div>
  <p>Mô tả chi tiết...</p>
</div>
```

**Thêm mục mới:** Copy block `cv-entry` và paste vào trong `cv-entries`.

**Thêm category mới** (ví dụ "Awards"):

```html
<div class="cv-section">
  <div class="cv-category">Awards</div>
  <div class="cv-entries">
    <div class="cv-entry">
      <h4>Tên giải thưởng</h4>
      <div class="cv-org">Tổ chức trao giải</div>
      <div class="cv-date">2024</div>
      <p>Mô tả...</p>
    </div>
  </div>
</div>
```

### 4.5 Contact

Tìm `<!-- ─── CONTACT` → sửa thông tin:

```html
<!-- Email -->
<a href="mailto:email-thật-của-bạn@university.edu" class="contact-method">

<!-- Thay đổi giá trị hiển thị -->
<div class="cm-value">email-thật-của-bạn@university.edu</div>

<!-- ORCID -->
<div class="cm-value">0000-000X-XXXX-XXXX</div>

<!-- Phòng làm việc -->
<div class="cm-value">Phòng XXX, Tòa nhà Y, Trường Z</div>
```

---

## 5. Thêm ảnh đại diện

### Bước 1: Chuẩn bị ảnh

- Kích thước khuyến nghị: **400×500px** (tỷ lệ 4:5)
- Định dạng: `.jpg` hoặc `.png`
- Đặt file vào thư mục `images/profile.jpg`

### Bước 2: Thay code

Tìm đoạn `photo-placeholder` trong Hero section và **thay thế toàn bộ** `<div class="photo-frame">...</div>` bằng:

```html
<div class="photo-frame">
  <img src="images/profile.jpg"
       alt="Harry Nguyen"
       style="width: 100%; height: 100%; object-fit: cover;">
</div>
```

---

## 6. Thay đổi màu sắc & font chữ

### Màu sắc

Tìm `:root {` ở đầu phần `<style>` và sửa:

```css
:root {
  --ink: #1a1a2e;        /* Màu chữ chính */
  --paper: #faf9f6;      /* Màu nền */
  --cream: #f3f0e8;      /* Màu nền phụ (sidebar, cards) */
  --accent: #8b2500;     /* Màu nhấn chính (đỏ nâu) */
  --accent-light: #c4560a; /* Màu nhấn sáng hơn */
  --muted: #6b6b7b;      /* Màu chữ phụ (xám) */
  --border: #d4d0c8;     /* Màu viền */
  --gold: #b8860b;       /* Màu vàng (status) */
  --sage: #4a6741;       /* Màu xanh lá (journal name) */
}
```

**Gợi ý bảng màu thay thế:**

| Phong cách | accent | accent-light | sage |
|------------|--------|-------------|------|
| Classic Blue | `#1a3a5c` | `#2d5f8a` | `#4a6741` |
| Deep Teal | `#0d5c63` | `#14919b` | `#2d6a4f` |
| Burgundy | `#800020` | `#a52a2a` | `#4a6741` |
| Navy | `#1b2a4a` | `#2c4a7c` | `#3d6b4f` |

### Font chữ

Tìm dòng `@import` hoặc `<link>` Google Fonts ở đầu file. Font hiện tại:

- **Cormorant Garamond** — tiêu đề (serif, học thuật)
- **Source Sans 3** — nội dung (sans-serif, dễ đọc)
- **JetBrains Mono** — năm, label (monospace)

Để đổi font, thay tên font trong cả link Google Fonts và CSS `font-family`.

---

## 7. Thêm bài báo mới

Tìm `<div class="pub-list">` → thêm block sau vào **đầu danh sách** (bài mới nhất ở trên):

```html
<div class="pub-item" data-type="journal">
  <div class="pub-year">2026</div>
  <div class="pub-info">
    <h4>Tên bài báo đầy đủ</h4>
    <div class="pub-authors">
      <strong>H. Nguyen</strong>, Author B, Author C
    </div>
    <div class="pub-journal">
      Tên tạp chí, Vol. XX, pp. XXX–XXX
    </div>
  </div>
  <div class="pub-links">
    <a href="https://doi.org/xxx" class="pub-link">DOI</a>
    <a href="link-pdf" class="pub-link">PDF</a>
  </div>
</div>
```

**Lưu ý:**
- `data-type="journal"` cho bài tạp chí, `data-type="conference"` cho hội nghị
- Tên mình in đậm: dùng `<strong>H. Nguyen</strong>`
- Ký tự đặc biệt: `Nd₀.₇` viết là `Nd₀.₇` (copy trực tiếp Unicode) hoặc dùng `<sub>0.7</sub>`

---

## 8. Thêm bài blog mới

Tìm `<div class="blog-grid">` → thêm block:

```html
<a href="link-bài-viết-hoặc-#" class="blog-card">
  <div class="blog-thumb blog-thumb-1">
    <!-- Đổi blog-thumb-1/2/3 để đổi màu gradient -->
    <div class="blog-thumb-pattern"></div>
    <span class="blog-thumb-label">Thể loại</span>
  </div>
  <div class="blog-body">
    <div class="blog-date">April 2026</div>
    <h3>Tiêu đề bài viết</h3>
    <p>Mô tả ngắn bài viết, khoảng 1-2 câu...</p>
    <span class="blog-read-more">Read more →</span>
  </div>
</a>
```

**Tạo màu thumbnail mới:** Thêm CSS class mới:

```css
.blog-thumb-4 {
  background: linear-gradient(135deg, #2e1a2e 0%, #5c2e5c 50%, #8b4a8b 100%);
}
```

---

## 9. Workflow làm việc

### Quy trình chỉnh sửa hàng ngày

```
┌─────────────────────────────────────────────────┐
│  1. Mở VS Code → Open Folder → my-website      │
│                    ↓                            │
│  2. Mở index.html → Right-click → Live Server   │
│                    ↓                            │
│  3. Sửa nội dung (Ctrl+F để tìm section)       │
│                    ↓                            │
│  4. Lưu file (Ctrl+S) → Trình duyệt tự reload  │
│                    ↓                            │
│  5. Kiểm tra trên trình duyệt                  │
│                    ↓                            │
│  6. Lặp lại bước 3-5 cho đến khi hài lòng      │
└─────────────────────────────────────────────────┘
```

### Checklist trước khi hoàn thành

- [ ] Đã thay tên, chức danh, trường viện
- [ ] Đã thay ảnh đại diện
- [ ] Đã cập nhật email và ORCID thật
- [ ] Đã thêm đầy đủ bài báo (publications)
- [ ] Đã sửa CV timeline (học vấn, kinh nghiệm)
- [ ] Đã cập nhật research interests
- [ ] Đã viết/sửa các bài blog
- [ ] Đã thêm link Google Scholar, ResearchGate
- [ ] Đã upload file CV PDF
- [ ] Đã kiểm tra trên điện thoại (thu nhỏ trình duyệt)
- [ ] Đã kiểm tra tất cả các link hoạt động

### Phím tắt VS Code hữu ích

| Phím tắt | Tác dụng |
|----------|----------|
| `Ctrl+F` | Tìm kiếm trong file |
| `Ctrl+H` | Tìm và thay thế |
| `Ctrl+S` | Lưu file |
| `Ctrl+Z` | Undo (hoàn tác) |
| `Ctrl+Shift+Z` | Redo |
| `Alt+Shift+↓` | Nhân đôi dòng hiện tại |
| `Ctrl+/` | Comment/Uncomment code |
| `Alt+Z` | Bật/tắt word wrap |
| `Ctrl+D` | Chọn từ giống nhau tiếp theo |

---

## 10. Đưa lên web (khi sẵn sàng)

### Lựa chọn 1: GitHub Pages (Miễn phí — Khuyến nghị)

```bash
# 1. Cài Git (nếu chưa có): https://git-scm.com

# 2. Tạo tài khoản GitHub: https://github.com

# 3. Tạo repository mới tên: username.github.io

# 4. Trong thư mục my-website, mở terminal:
git init
git add .
git commit -m "First commit - personal website"
git remote add origin https://github.com/username/username.github.io.git
git push -u origin main

# 5. Truy cập: https://username.github.io
```

**Cập nhật sau này:**
```bash
git add .
git commit -m "Mô tả thay đổi"
git push
```

### Lựa chọn 2: Netlify (Miễn phí — Kéo thả)

1. Vào [netlify.com](https://www.netlify.com)
2. Đăng ký → "Add new site" → "Deploy manually"
3. **Kéo thả thư mục `my-website`** vào trang
4. Xong! Netlify tự tạo link cho bạn
5. Có thể đổi tên thành `harrynguyen.netlify.app`

### Lựa chọn 3: Vercel (Miễn phí)

1. Vào [vercel.com](https://vercel.com)
2. Kết nối GitHub repository
3. Tự động deploy mỗi khi push code mới

### So sánh nhanh

| Tiêu chí | GitHub Pages | Netlify | Vercel |
|----------|-------------|---------|--------|
| Giá | Miễn phí | Miễn phí | Miễn phí |
| Độ khó | Cần biết Git | Kéo thả | Cần GitHub |
| Tên miền riêng | ✅ | ✅ | ✅ |
| HTTPS | ✅ Tự động | ✅ Tự động | ✅ Tự động |
| Tốc độ deploy | ~1 phút | ~30 giây | ~30 giây |

---

## 💡 Mẹo & Lưu ý

1. **Backup thường xuyên:** Copy thư mục `my-website` ra nơi khác trước khi sửa lớn
2. **Test responsive:** Nhấn `F12` → click icon điện thoại (hoặc `Ctrl+Shift+M`) để xem trên mobile
3. **Validate HTML:** Vào [validator.w3.org](https://validator.w3.org/) để kiểm tra lỗi HTML
4. **Tối ưu ảnh:** Dùng [tinypng.com](https://tinypng.com/) để nén ảnh trước khi thêm vào
5. **Google Scholar link:** Format → `https://scholar.google.com/citations?user=YOUR_ID`
6. **ORCID link:** Format → `https://orcid.org/0000-000X-XXXX-XXXX`

---

> 📝 *Tài liệu tạo bởi Claude — Cập nhật: Tháng 4/2026*
