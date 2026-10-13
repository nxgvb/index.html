# index.html
Website for Kinnauri Products
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sonika's Kinnauri Enterprise | Authentic Ribba Products</title>
    <style>
        :root {
            --primary: #8B263E; /* Traditional Himachali Maroon */
            --secondary: #1E4620; /* Deep Himalayan Pine Green */
            --gold: #D4AF37;
            --light-bg: #FDFBF7;
            --dark-text: #2B2D42;
            --gray: #6C757D;
            --fb-color: #1877F2;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--light-bg);
            color: var(--dark-text);
            line-height: 1.6;
        }

        /* Top Bar */
        .top-bar {
            background-color: var(--secondary);
            color: white;
            font-size: 0.85rem;
            text-align: center;
            padding: 6px 10px;
            font-weight: 500;
            letter-spacing: 0.5px;
        }

        /* Navigation */
        header {
            background-color: white;
            box-shadow: 0 2px 15px rgba(0,0,0,0.06);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo h1 {
            color: var(--primary);
            font-size: 1.6rem;
            font-weight: 700;
            letter-spacing: -0.5px;
        }

        .logo p {
            font-size: 0.8rem;
            color: var(--secondary);
            text-transform: uppercase;
            letter-spacing: 1.5px;
            font-weight: 600;
        }

        .nav-buttons {
            display: flex;
            gap: 12px;
            align-items: center;
        }

        /* Base Buttons */
        .btn {
            padding: 8px 18px;
            text-decoration: none;
            border-radius: 6px;
            font-weight: 600;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            border: none;
            cursor: pointer;
        }

        .btn-primary {
            background-color: var(--primary);
            color: white;
        }

        .btn-primary:hover {
            background-color: #6a1c2e;
            transform: translateY(-1px);
        }

        .btn-fb {
            background-color: var(--fb-color);
            color: white;
        }

        .btn-fb:hover {
            background-color: #135cb8;
            transform: translateY(-1px);
        }

        .btn-wa {
            background-color: #25D366;
            color: white;
        }

        .btn-wa:hover {
            background-color: #128C7E;
            transform: translateY(-1px);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.55), rgba(0, 0, 0, 0.65)), 
                        url('https://unsplash.com') no-repeat center center/cover;
            color: white;
            text-align: center;
            padding: 120px 20px;
        }

        .hero h2 {
            font-size: 2.8rem;
            margin-bottom: 15px;
            font-weight: 700;
            text-shadow: 0 2px 4px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 1.25rem;
            max-width: 700px;
            margin: 0 auto 30px auto;
            opacity: 0.95;
        }

        /* Main Container */
        .container {
            max-width: 1200px;
            margin: 60px auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            color: var(--primary);
            font-size: 2rem;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 3px;
            background-color: var(--secondary);
            margin: 12px auto 0 auto;
            border-radius: 2px;
        }

        /* Product Catalog Grid */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 35px;
        }

        .product-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0,0,0,0.04);
            display: flex;
            flex-direction: column;
            border: 1px solid #F0EFEA;
            transition: all 0.3s ease;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 30px rgba(0,0,0,0.08);
        }

        .product-img-container {
            height: 300px;
            width: 100%;
            overflow: hidden;
            background-color: #f7f7f7;
            position: relative;
        }

        .product-img-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .badge {
            position: absolute;
            top: 15px;
            left: 15px;
            background-color: var(--secondary);
            color: white;
            padding: 4px 10px;
            font-size: 0.75rem;
            font-weight: 700;
            border-radius: 4px;
            text-transform: uppercase;
        }

        .product-info {
            padding: 24px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .product-info h3 {
            margin-bottom: 10px;
            font-size: 1.3rem;
            color: var(--dark-text);
        }

        .product-info p {
            color: var(--gray);
            font-size: 0.95rem;
            margin-bottom: 20px;
            flex-grow: 1;
        }

        .price-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: auto;
            border-top: 1px dashed #EAE9E4;
            padding-top: 15px;
        }

        .price-label {
            font-size: 0.8rem;
            color: var(--gray);
            text-transform: uppercase;
        }

        .price-status {
            font-size: 1.15rem;
            font-weight: 700;
            color: var(--secondary);
        }

        /* Combined Contact & Inquiry Dashboard */
        .info-section {
            background-color: white;
            padding: 60px 20px;
            border-top: 1px solid #EAE9E4;
        }

        .info-grid {
            max-width: 1100px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }

        .info-card {
            background: var(--light-bg);
            padding: 35px;
            border-radius: 12px;
            border-top: 4px solid var(--primary);
            box-shadow: 0 4px 15px rgba(0,0,0,0.02);
        }

        .info-card h3 {
            color: var(--primary);
            margin-bottom: 20px;
            font-size: 1.4rem;
            border-bottom: 1px solid #EAE9E4;
            padding-bottom: 10px;
        }

        .info-item {
            margin-bottom: 15px;
            display: flex;
            flex-direction: column;
        }

        .info-item label {
            font-size: 0.8rem;
            text-transform: uppercase;
            color: var(--gray);
            font-weight: 600;
            margin-bottom: 2px;
        }

        .info-item span, .info-item a {
            font-size: 1.05rem;
            color: var(--dark-text);
            font-weight: 500;
            text-decoration: none;
        }

        .info-item a.email-link {
            color: var(--primary);
            font-weight: 600;
        }

        .info-item a.email-link:hover {
            text-decoration: underline;
        }

        /* Online Inquiry Form Styling */
        .inquiry-form {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 5px;
        }

        .form-group label {
            font-size: 0.85rem;
            font-weight: 600;
            color: var(--dark-text);
        }

        .form-control {
            padding: 10px 14px;
            border: 1px solid #D1CFC9;
            border-radius: 6px;
            font-size: 0.95rem;
            background-color: white;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(139, 38, 62, 0.15);
        }

        footer {
            background-color: var(--dark-text);
            color: white;
            text-align: center;
            padding: 25px 20px;
            font-size: 0.9rem;
            border-top: 3px solid var(--gold);
        }

        /* Mobile Optimization */
        @media (max-width: 768px) {
            .nav-container {
                flex-direction: column;
                text-align: center;
                gap: 15px;
            }
            .hero h2 {
                font-size: 2.1rem;
            }
            .info-grid {
                grid-template-columns: 1fr;
                gap: 30px;
            }
        }
    </style>
</head>
<body>

    <!-- Top Announcement Bar -->
    <div class="top-bar">
        🏔️ Fresh Harvest & Traditional Handlooms Sourced Directly From Ribba Village, Kinnaur
    </div>

    <!-- Header Navigation -->
