# Student Management System

A comprehensive web application for managing student information, attendance, and fee payments.

## Features

### 1. Students Panel
- Add new students with basic information
- View all students in a table format
- Edit and delete student records
- Search and filter functionality

### 2. Personal Details Panel (NEW!)
- Comprehensive student personal information management
- **Basic Information**: Name, Student ID, Date of Birth, Gender
- **Contact Information**: Email, Phone, Complete Address (City, State, Pincode)
- **Academic Information**: Course, Year, Section, Roll Number
- **Emergency Contact**: Emergency contact person details
- **Additional Information**: Blood Group, Nationality, Medical Conditions, Notes
- Search and filter by name, ID, or course
- View detailed information for each student
- Edit personal details with form validation

### 3. Attendance Panel
- Mark daily attendance for students
- View attendance statistics and percentages
- Track present/absent days

### 4. Fee Payment Panel
- Record fee payments with different payment methods
- View payment history
- Download payment receipts
- Track payment status

## Technical Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Backend**: Node.js, Express.js
- **Database**: MongoDB with Mongoose ODM
- **Styling**: Custom CSS with responsive design

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up MongoDB connection in `.env` file:
   ```
   MONGODB_URI=mongodb://localhost:27017/student_management
   PORT=3000
   ```
4. Start the server:
   ```bash
   npm start
   ```
5. Open http://localhost:3000 in your browser

## Personal Details Features

### Form Sections
1. **Basic Information**
   - Student ID (required)
   - Full Name (required)
   - Date of Birth (required)
   - Gender selection

2. **Contact Information**
   - Email Address (required)
   - Phone Number (required)
   - Complete Address (required)
   - City, State, Pincode (required)

3. **Academic Information**
   - Course selection (required)
   - Year selection (required)
   - Section (optional)
   - Roll Number (optional)

4. **Emergency Contact**
   - Emergency Contact Name (required)
   - Emergency Contact Phone (required)
   - Relationship (required)

5. **Additional Information**
   - Blood Group (optional)
   - Nationality (defaults to "Indian")
   - Medical Conditions (optional)
   - Additional Notes (optional)

### Functionality
- **Create**: Add new student with complete personal details
- **Read**: View all students with key information in table format
- **Update**: Edit existing student personal details
- **Search**: Filter students by name or ID
- **Filter**: Filter by course
- **View Details**: Click "View" button to see complete information
- **Form Validation**: Client-side validation for required fields and data formats

### Data Validation
- Student ID: Minimum 3 characters
- Name: Minimum 2 characters
- Email: Valid email format
- Phone numbers: Exactly 10 digits
- Required fields validation
- Date format validation

## API Endpoints

- `GET /api/students` - Get all students
- `GET /api/students/:id` - Get specific student
- `POST /api/students` - Create new student
- `PATCH /api/students/:id` - Update student
- `DELETE /api/students/:id` - Delete student (soft delete)

## Database Schema

The Student model includes all personal details fields:
- Basic info (id, name, email, phone, course, year)
- Personal details (dateOfBirth, gender, address, etc.)
- Emergency contact information
- Additional information (blood group, medical conditions, etc.)

## Responsive Design

The application is fully responsive and works on:
- Desktop computers
- Tablets
- Mobile phones

## Error Handling

- Comprehensive error handling for API calls
- User-friendly error messages
- Retry mechanisms for failed requests
- Loading states and notifications

## Future Enhancements

- Export data to Excel/PDF
- Bulk import/export functionality
- Advanced reporting and analytics
- User authentication and authorization
- Email notifications
- Photo upload for students 