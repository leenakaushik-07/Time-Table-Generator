# 📅 Timetable Generator System

A complete C++-based solution to generate, manage, and approve academic timetables for multiple sections, ensuring no class overlaps using graph coloring algorithms.

---

## 👥 Team Members

1. **Leena Kaushik** *(Team Lead)*
2. **Prashant Tomar**
3. **Tejas Chauhan**

---

## 🧠 Project Overview

This project is designed to assist educational institutions in automating the generation of subject timetables for different sections while:
- Preventing scheduling conflicts between subjects and teachers
- Allowing administrators to assign and update teaching responsibilities
- Enabling heads of departments to view and approve generated timetables

---

## 🏗️ Tech Stack

- **Language**: C++
- **Concepts Used**:
  - Graph Coloring (Greedy Algorithm)
  - File I/O with CSV
  - `std::filesystem` for folder & file management
  - Basic authentication and role-based access
- **Output**: Timetable CSV files (1 per section)

---

## 📁 Folder Structure

```
├── main.cpp              # Main source file
├── teacher_data.csv      # Initial dataset of teacher assignments
├── update.csv            # Admin-triggered reassignment data
├── user.csv              # User credentials with roles
├── timetables/           # Generated timetables
├── approved/             # Approved timetables (moved from timetables/)
```

---

## 🔑 User Roles

| Role    | Capabilities |
|---------|--------------|
| **Admin** | Generate & update timetables |
| **HOD**   | View & approve timetables |
| **Teacher/Student** | View generated timetables |

---

## 🔐 Sample Login Credentials

```
Username    Password     Role
--------    --------     ----
admin       admin123     admin
hod         hod123       hod
teacher1    pass1        teacher
student1    stud1        student
```

---

## 🛠️ How to Run

### ⏳ Compile the Project
```bash
g++ main.cpp -o timetable -std=c++17
./timetable
```

### 🧾 Required Files

Ensure the following CSVs are present:
- `teacher_data.csv` – Initial teacher assignments
- `update.csv` – Updates teacher-subject assignments
- `user.csv` – Login credentials

---

## 📌 Features

- ✅ Generate conflict-free timetables using graph coloring
- ✅ Save each section's timetable as a CSV
- ✅ Allow admin to reassign teaching duties
- ✅ Let HOD approve timetables, auto-move to `approved/`
- ✅ Authentication for different roles
- ✅ View detailed report of color assignments (graph nodes)

---

## 📊 Sample Output

- `A SEC_timetable.csv`:
```
Day,Slot 1,Slot 2,Slot 3
Monday,351,342,free
Tuesday,343,free,352
...
```

---

## 💡 Future Enhancements

- Web-based or GUI frontend
- Support for lecture types (lab, theory, etc.)
- Export as PDF or Excel
- Drag-and-drop timetable customization

---

> © 2025 Timetable Generator | Made with 💻 by Team Leena, Prashant & Tejas
