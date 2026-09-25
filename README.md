
#Al Ikthibar Repair — Website

A dark navy & gold automotive workshop website for **Al Ikthibar Repair**, a car repair business with two service centres in Mussafah Industrial Area, Abu Dhabi, UAE.

Built with plain PHP + MySQL (no framework), the website is fully database-driven and manageable through a lightweight admin panel.

## Features

### 🏠 Home Page
- Hero slider
- Animated statistics
- "Why Choose Us" section
- Services preview
- Customer testimonials
- Call-to-action section

### 🔧 Services
- Category filter
- Individual service cards
- Services dynamically loaded from the database

### 📅 Book Appointment
- Date & time picker using Flatpickr
- Business hours restricted to 9:00 AM – 8:00 PM
- Client-side validation
- Server-side validation
- Appointment details saved to MySQL
- Automatically opens a pre-filled WhatsApp message
- Customers can send appointment details directly to the workshop

### 📞 Contact
- Both workshop locations
- WhatsApp chat buttons
- Embedded Google Map
- Quote/message form

### 🔐 Admin Panel
- Password-protected admin login
- Booking management dashboard
- Filter bookings by status
- Update booking status:
  - New
  - Confirmed
  - In Progress
  - Completed
  - Cancelled
- Add services
- Delete services
- Upload service photos

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Plain PHP 8.x |
| Database | MySQL via PDO (prepared statements) |
| Frontend | HTML5, Bootstrap 5, Custom CSS, Vanilla JavaScript |
| Date/Time Picker | Flatpickr |
| Leads | WhatsApp wa.me Click-to-Chat Integration |

## Security

The project includes several security measures:

- PDO prepared statements throughout the application for SQL injection protection
- `htmlspecialchars()` output escaping for XSS protection
- CSRF tokens on every form
- `password_hash()` / `password_verify()` for secure admin authentication
- File upload validation for service photos
  - File type validation
  - File size validation

## Setup

### XAMPP / Local Development

1. Import `schema.sql` into MySQL.
   - This creates the `ikthibar` database and inserts the initial seed data.
2. Open:
   ```
   config/db.php
   ```
   Update the MySQL configuration with your:
   - Host
   - Username
   - Password
   - Database name
3. Copy the project folder into:
   ```
   htdocs
   ```
4. Start Apache and MySQL from XAMPP.
5. Open the project in your browser.
6. Access the admin panel at:
   ```
   /admin/login.php
   ```

### Default Admin Login
```
Email:    admin@alikthibar.com
Password: admin123
```

**Important:** Change the default admin password immediately after the first login.

## Project Structure

```
/config
    database connection

/includes
    shared header
    footer
    helper functions

/admin
    admin panel
    login
    bookings
    services

/assets
    CSS
    JavaScript

/uploads
    uploaded service photos

schema.sql
    database schema
    seed data
```

## Roadmap

- [ ] Gallery page
- [ ] Testimonial submission form
- [ ] Email confirmations using PHPMailer
- [ ] Admin management for working hours
- [ ] Admin management for holidays
- [ ] Admin management for workshop locations
- [ ] Admin management for hero slider
- [ ] Admin management for testimonials
- [ ] WhatsApp Cloud API integration for fully automatic notifications without requiring a customer tap

## Project Highlights

- Fully database-driven website
- Responsive automotive workshop design
- No PHP framework required
- Lightweight admin panel
- Appointment booking system
- WhatsApp lead integration
- Secure authentication
- CSRF protection
- SQL injection protection
- XSS protection
- Service management with image uploads
- Booking status management
```
