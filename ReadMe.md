
# MongoDB Zen Class Database Design

A comprehensive MongoDB database design for managing a coding bootcamp program including students, assignments, attendance and placements.

## Database Collections

1. Users
- Student information
- Login credentials Like email
- Progress tracking

2. Codekata
- Student id
- Problem-solving metrics

3. Attendance
- Daily attendance records
- Timestamp tracking
- Absence management

4. Topics
- Course curriculum
- Learning modules
- Session details
- Batch information
- Date and time
- Instructor details

5. Tasks
- Assignments
- Project submissions
- Task completion status
- Submission deadlines

6. Company_drives
- Placement opportunities
- Company details
- Drive dates
- Student participation

7. Mentors
- Mentor profiles
- Mentee assignments
- Batch-wise mentor assignments

## Key Queries Implemented

1. Topics and tasks covered in October
2. Company drives between Oct 15-31, 2020
3. Company drives and participating students
4. Student-wise codekata problem completion metrics
5. Mentors with 15+ mentees
6. Absent students with pending tasks (Oct 15-31, 2020)

## Tech Stack
- MongoDB
- MongoDB Queries
- Aggregation Framework

## Sample Query Structure

// Find company drives in date range
db.company_drives.find({
    date: {
        $gte: ISODate("2020-10-15"),
        $lte: ISODate("2020-10-31")
    }
})
