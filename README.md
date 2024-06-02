# RESORT-BOOKING-WEBSITE

### Frontend

**HTML**
- **Homepage**: A welcoming page with high-quality images of the resort, a brief introduction, and links to other sections of the website.
- **Navigation Bar**: Contains links to the home, rooms, amenities, booking, contact us, and login/register pages.
- **Rooms Page**: Lists all available rooms with images, descriptions, and pricing.
- **Amenities Page**: Showcases the resort's amenities like swimming pool, spa, restaurant, gym, etc., with images and descriptions.
- **Booking Page**: A form where users can select their desired room type, check-in and check-out dates, and number of guests.
- **Contact Us Page**: A form for users to submit inquiries, with fields for name, email, phone number, and message.
- **Login/Register Page**: Allows users to log in or create a new account.

**CSS**
- **Responsive Design**: Ensures the website is mobile-friendly and looks good on all devices.
- **Styling**: Consistent and visually appealing styling for buttons, forms, images, and text across the site. Use of a color scheme that matches the resort’s branding.
- **Animations**: Smooth transitions and animations for interactive elements like buttons, image galleries, and form submissions.

**JavaScript**
- **Form Validation**: Client-side validation for booking and contact forms to ensure all required fields are filled out correctly.
- **Interactive Elements**: Implementing sliders for image galleries, dropdowns for room selection, and date pickers for check-in/check-out dates.
- **AJAX**: Used for dynamic content loading, such as updating available rooms based on user input without refreshing the page.

### Backend

**PHP**
- **User Authentication**: Handles user registration, login, and logout functionality. Passwords are hashed for security.
- **Booking Management**: Processes booking form submissions, checks room availability, calculates total cost, and stores booking details in the database.
- **Contact Form Handling**: Processes inquiries submitted through the contact form and stores them in the database or sends them to the admin via email.
- **Admin Panel**: Allows the resort staff to manage room availability, view bookings, and respond to inquiries. Restricted access to authorized users only.

**MySQL**
- **Database Schema**:
  - **Users Table**: Stores user information (user_id, name, email, hashed_password, etc.).
  - **Rooms Table**: Contains information about each room type (room_id, room_name, description, price, availability, etc.).
  - **Bookings Table**: Stores booking details (booking_id, user_id, room_id, check_in_date, check_out_date, total_cost, etc.).
  - **Inquiries Table**: Records contact form submissions (inquiry_id, name, email, phone, message, submission_date, etc.).
- **Data Relationships**: Foreign keys to ensure referential integrity between tables (e.g., user_id in the Bookings table references user_id in the Users table).

### Example Workflow

1. **User Registration/Login**:
   - User visits the login/register page.
   - If new, fills out the registration form and submits it.
   - PHP processes the form, hashes the password, and stores user info in the database.
   - User logs in using their credentials.

2. **Room Booking**:
   - User navigates to the rooms page, views available rooms, and selects one to book.
   - Fills out the booking form with check-in/check-out dates and guest details.
   - JavaScript validates the form and uses AJAX to check room availability.
   - On successful validation, PHP processes the booking, calculates the cost, and stores the booking in the database.
   - User receives a booking confirmation message.

3. **Admin Management**:
   - Admin logs into the admin panel.
   - Views all bookings, room availability, and inquiries.
   - Can update room details, mark rooms as unavailable, and respond to inquiries.

This comprehensive setup ensures a seamless experience for both users and the resort staff, combining a visually appealing frontend with a robust and secure backend.
