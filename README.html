<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Student Registration</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: 
        linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
        url('https://imgcdn.stablediffusionweb.com/2024/9/24/0105ea50-2c8d-4e10-bbbd-fceef2175ba6.jpg');
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      background-attachment: fixed;
      color: #fff;
    }

    .logo-container {
      position: absolute;
      top: 10px;
      left: 20px;
    }

    .logo-container img {
      height: 96px;
    }

    .section-heading {
      text-align: center;
      font-size: 32px;
      font-weight: bold;
      color: #fff;
      background-color: rgba(202, 4, 4, 0.9);
      padding: 15px 20px;
      margin: 80px auto 10px auto;
      width: fit-content;
      border-radius: 12px;
      box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3);
    }

    .form-container {
      display: flex;
      justify-content: center;
      margin: 40px auto;
    }

    form {
      background: rgba(92, 76, 76, 0.95);
      padding: 40px;
      border-radius: 15px;
      width: 500px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
    }

    input, button {
      display: block;
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      font-size: 15px;
    }

    .students-container {
      display: flex;
      justify-content: center;
      margin-top: 15px;
      margin-bottom: 100px;
    }

    ul {
      list-style: none;
      padding: 0;
      max-width: 960px;
      width: 100%;
    }

    li {
      background: rgb(195, 191, 191);
      padding: 15px;
      margin-bottom: 15px;
      border-left: 15px solid #2ecc71;
      position: relative;
      border-radius: 24px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      color: black;
    }

    .actions {
      position: absolute;
      top: 50%;
      right: 24px;
      transform: translateY(-50%);
      display: flex;
      gap: 10px;
    }

    .actions button {
      padding: 5px 10px;
      font-size: 14px;
      cursor: pointer;
      border: none;
      border-radius: 4px;
      background-color: #3498db;
      color: #fff;
      transition: background-color 0.3s;
    }

    .actions button:hover {
      background-color: #2980b9;
    }
  </style>
</head>
<body>

  <!-- Logo Top Left -->
  <div class="logo-container">
    <img src="https://www.englandairpark.org/wp-content/uploads/2018/11/Reddy-Ice-Logo-1024x256.jpg" alt="Logo">
  </div>

  <!-- Student Registration Heading -->
  <div style="display: flex; justify-content: center;">
    <h1 class="section-heading">Student Registration</h1>
  </div>

  <!-- Form Section -->
  <div class="form-container">
    <form id="studentForm">
      <input type="hidden" id="student_id">
      <input type="text" id="first_name" placeholder="First Name" required>
      <input type="text" id="last_name" placeholder="Last Name" required>
      <input type="email" id="email" placeholder="Email" required>
      <input type="text" id="phone" placeholder="Phone">
      <input type="text" id="course" placeholder="Course">
      <button type="submit">Register / Update</button>
    </form>
  </div>

  <!-- Registered Students Heading -->
  <div style="display: flex; justify-content: center;">
    <h2 class="section-heading">Registered Students</h2>
  </div>

  <!-- List of Students -->
  <div class="students-container">
    <ul id="studentList"></ul>
  </div>

  <script>
    const apiUrl = 'http://127.0.0.1:5000/students';

    document.getElementById('studentForm').addEventListener('submit', function (e) {
      e.preventDefault();

      const id = document.getElementById('student_id').value;
      const student = {
        first_name: document.getElementById('first_name').value,
        last_name: document.getElementById('last_name').value,
        email: document.getElementById('email').value,
        phone: document.getElementById('phone').value,
        course: document.getElementById('course').value,
      };

      const method = id ? 'PUT' : 'POST';
      const endpoint = id ? `${apiUrl}/${id}` : apiUrl;

      fetch(endpoint, {
        method: method,
        body: JSON.stringify(student),
        headers: { 'Content-Type': 'application/json' }
      })
      .then(res => res.json())
      .then(data => {
        alert(data.message || data.error);
        loadStudents();
        document.getElementById('studentForm').reset();
        document.getElementById('student_id').value = '';
      })
      .catch(error => alert("Error: " + error));
    });

    function loadStudents() {
      fetch(apiUrl)
        .then(res => res.json())
        .then(data => {
          const list = document.getElementById('studentList');
          list.innerHTML = '';
          data.forEach(s => {
            const item = document.createElement('li');
            item.innerHTML = `
              ${s.first_name} ${s.last_name} (${s.course}) - ${s.email}
              <div class="actions">
                <button onclick="editStudent(${s.id})">Edit</button>
                <button onclick="deleteStudent(${s.id})">Delete</button>
              </div>
            `;
            list.appendChild(item);
          });
        });
    }

    function editStudent(id) {
      fetch(apiUrl)
        .then(res => res.json())
        .then(data => {
          const student = data.find(s => s.id === id);
          document.getElementById('student_id').value = student.id;
          document.getElementById('first_name').value = student.first_name;
          document.getElementById('last_name').value = student.last_name;
          document.getElementById('email').value = student.email;
          document.getElementById('phone').value = student.phone;
          document.getElementById('course').value = student.course;
        });
    }

    function deleteStudent(id) {
      if (confirm("Are you sure you want to delete this student?")) {
        fetch(`${apiUrl}/${id}`, {
          method: 'DELETE'
        })
        .then(res => res.json())
        .then(data => {
          alert(data.message || data.error);
          loadStudents();
        })
        .catch(error => {
          alert("Failed to delete student");
        });
      }
    }

    window.onload = loadStudents;
  </script>
</body>
</html>
