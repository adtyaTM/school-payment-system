# School Payment System

Sistem pembayaran sekolah modern dan profesional untuk SD, SMP, dan SMA.

## 🎯 Fitur Utama

✅ Login Admin Sekolah
✅ Manajemen Data Siswa (Import Excel/CSV)
✅ Manajemen Pembayaran
✅ Integrasi Payment Gateway (Midtrans & Stripe)
✅ Dashboard dengan Riwayat Pembayaran
✅ Notifikasi Pembayaran
✅ Laporan Keuangan (Harian, Bulanan, Tahunan)
✅ Cetak Kwitansi Pembayaran
✅ Integrasi Google Drive untuk Database

## 💻 Teknologi

- **Frontend**: HTML5, CSS3, JavaScript Modern
- **Backend**: Node.js + Express.js
- **Database**: Google Drive API + Google Sheets
- **Payment Gateway**: Midtrans & Stripe
- **UI Framework**: Bootstrap 5
- **Design**: Modern, Responsive, Professional

## 📁 Struktur Project

```
school-payment-system/
├── public/
│   ├── index.html                 # Login page
│   ├── dashboard.html             # Dashboard
│   ├── students.html              # Data siswa + import
│   ├── payments.html              # Pembayaran
│   ├── reports.html               # Laporan
│   ├── css/
│   │   ├── style.css              # Main styles
│   │   ├── dashboard.css          # Dashboard styles
│   │   └── responsive.css         # Mobile responsive
│   ├── js/
│   │   ├── utils.js               # Utility functions
│   │   ├── auth.js                # Authentication
│   │   ├── dashboard.js           # Dashboard handler
│   │   ├── students.js            # Student management
│   │   ├── payment.js             # Payment handler
│   │   └── report.js              # Report handler
│   └── assets/
│       └── images/
├── backend/
│   ├── server.js                  # Entry point
│   ├── config/
│   │   ├── google-drive.js        # Google Drive config
│   │   ├── midtrans.js            # Midtrans config
│   │   └── stripe.js              # Stripe config
│   ├── routes/
│   │   ├── auth.js                # Auth routes
│   │   ├── students.js            # Student routes
│   │   ├── payment.js             # Payment routes
│   │   ├── reports.js             # Report routes
│   │   └── notifications.js       # Notification routes
│   ├── controllers/
│   │   ├── authController.js      # Auth logic
│   │   ├── studentController.js   # Student logic
│   │   ├── paymentController.js   # Payment logic
│   │   └── reportController.js    # Report logic
│   └── middleware/
│       └── auth.js                # JWT middleware
├── docs/
│   ├── SETUP.md                   # Installation guide
│   ├── GOOGLE_DRIVE_SETUP.md      # Google Drive setup
│   └── API.md                     # API documentation
├── .env.example                   # Environment template
├── package.json                   # Dependencies
└── server.js                      # Server file
```

## 🚀 Quick Start

### 1. Clone Repository
```bash
git clone https://github.com/adtyaTM/school-payment-system.git
cd school-payment-system
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Setup Environment
```bash
cp .env.example .env
# Edit .env dengan konfigurasi Anda
```

### 4. Setup Google Drive (Optional)
Lihat `docs/GOOGLE_DRIVE_SETUP.md` untuk panduan lengkap

### 5. Run Application
```bash
# Development
npm run dev

# Production
npm start
```

Akses aplikasi di `http://localhost:3000`

## 📝 Default Login
- **Username**: `admin`
- **Password**: Sesuai konfigurasi `.env`

## 🎓 Fitur Detail

### Login & Autentikasi
- ✅ Username & Password authentication
- ✅ JWT token based
- ✅ Secure password storage
- ✅ Session management

### Data Siswa
- ✅ Import data dari Excel/CSV
- ✅ Download template Excel
- ✅ Preview data sebelum import
- ✅ Tambah/Edit/Hapus siswa manual
- ✅ Filter by tingkat (SD/SMP/SMA)
- ✅ Search by nama, No. Induk, atau kelas
- ✅ Statistik siswa real-time

### Manajemen Pembayaran
- ✅ Tambah pembayaran
- ✅ Integrasi Midtrans & Stripe
- ✅ Tracking status pembayaran
- ✅ Notifikasi pembayaran
- ✅ Cetak kwitansi PDF
- ✅ Riwayat transaksi lengkap

### Dashboard & Analytics
- ✅ Statistik pembayaran real-time
- ✅ Grafik pembayaran bulanan
- ✅ Aktivitas terbaru
- ✅ KPI summary

### Laporan Keuangan
- ✅ Laporan harian
- ✅ Laporan bulanan
- ✅ Laporan tahunan
- ✅ Export ke Excel
- ✅ Print report

## 📱 Responsive Design

- ✅ Desktop (1200px+)
- ✅ Tablet (768px - 1199px)
- ✅ Mobile (< 768px)
- ✅ Touch-friendly buttons
- ✅ Optimized performance

## 🔒 Security Features

- ✅ JWT Authentication
- ✅ Password hashing (bcryptjs)
- ✅ CORS protection
- ✅ Input validation
- ✅ SQL injection prevention
- ✅ Rate limiting ready

## 📊 Data Structure

### Siswa
- No. Induk (unique)
- Nama Siswa
- Kelas
- Tingkat (SD/SMP/SMA)
- Email
- No. HP Orang Tua
- Created At

### Pembayaran
- ID Pembayaran (unique)
- ID Siswa (foreign key)
- Nominal
- Tanggal
- Status (PENDING/SUKSES/GAGAL)
- Metode (MIDTRANS/STRIPE/TRANSFER)
- Referensi

### Laporan
- Tanggal
- Total Pembayaran
- Terkonfirmasi
- Pending
- Gagal

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/login` - Login
- `GET /api/auth/profile` - Get profile
- `PUT /api/auth/change-password` - Change password

### Students
- `GET /api/students` - List students
- `POST /api/students` - Create student
- `POST /api/students/import` - Import students
- `PUT /api/students/:id` - Update student
- `DELETE /api/students/:id` - Delete student

### Payments
- `GET /api/payment` - List payments
- `POST /api/payment` - Create payment
- `POST /api/payment/:id/confirm` - Confirm payment
- `GET /api/payment/:id/receipt` - Get receipt

### Reports
- `GET /api/reports/daily` - Daily report
- `GET /api/reports/monthly` - Monthly report
- `GET /api/reports/yearly` - Yearly report
- `GET /api/reports/export/daily` - Export daily
- `GET /api/reports/export/monthly` - Export monthly

Lihat `docs/API.md` untuk dokumentasi lengkap.

## 📚 Dokumentasi

- [Setup Guide](./docs/SETUP.md) - Panduan instalasi
- [Google Drive Setup](./docs/GOOGLE_DRIVE_SETUP.md) - Setup Google Drive API
- [API Documentation](./docs/API.md) - API reference lengkap

## 🐛 Troubleshooting

### Port Already in Use
```bash
PORT=3001 npm start
```

### Module Not Found
```bash
rm -rf node_modules
npm install
```

### Google Drive Error
- Verify credentials di `.env`
- Check Google Drive API quota
- Refresh OAuth token

Lihat `docs/SETUP.md` untuk troubleshooting lengkap.

## 📄 License

MIT License - Bebas digunakan untuk keperluan apapun.

## 👨‍💻 Author

**adtyaTM** - School Payment System Developer

## 🤝 Contributing

Contribusi sangat diterima! Silakan:
1. Fork repository
2. Buat feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buka Pull Request

## 📞 Support

Untuk bantuan atau pertanyaan, silakan buat issue di repository ini.

---

**Dibuat dengan ❤️ untuk sekolah Indonesia**
