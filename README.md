# brainomaly-be

brainomaly-backend/
├── node_modules/
├── src/
│   ├── config/               # Koneksi database, pemuatan variabel lingkungan
│   │   └── db.js
│   │   └── index.js          # Memuat variabel lingkungan
│   ├── models/               # Skema Mongoose untuk entitas data
│   │   └── User.js           # Menambahkan field untuk riwayat analisis (e.g., array of analysis IDs)
│   │   └── Patient.js
│   │   └── AnalysisHistory.js # NEW: Untuk menyimpan detail setiap analisis tumor otak
│   ├── controllers/          # Logika bisnis, penanganan permintaan, berinteraksi dengan model/layanan
│   │   └── authController.js
│   │   └── userController.js
│   │   └── patientController.js
│   │   └── analysisController.js # NEW: Untuk logika analisis tumor dan riwayat
│   ├── routes/               # Mendefinisikan endpoint API dan menghubungkan ke controller
│   │   └── authRoutes.js
│   │   └── userRoutes.js
│   │   └── patientRoutes.js
│   │   └── analysisRoutes.js # NEW: Untuk rute analisis tumor dan riwayat
│   ├── middleware/           # Middleware Express yang dapat digunakan kembali
│   │   └── authMiddleware.js
│   │   └── validationMiddleware.js
│   │   └── errorHandler.js
│   ├── services/             # Abstraksi untuk logika kompleks atau integrasi eksternal
│   │   └── mlService.js      # Menangani interaksi dengan model ML (baik eksternal maupun internal)
│   │   └── uploadService.js  # Menangani unggahan file ke penyimpanan cloud
│   ├── utils/                # Fungsi pembantu
│   │   └── jwt.js
│   │   └── password.js
│   ├── app.js                # Penyiapan aplikasi Express utama
│   └── server.js             # Titik masuk
├── .env.example              # Template untuk variabel lingkungan
├── .gitignore
├── package.json
├── README.md
