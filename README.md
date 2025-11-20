### NAME: SURYA P <br>
### REG NO: 212224230280 <br> 
### Date: 11/09/2025

## EX. No. 3 : SLOT TIME TABLE 

## AIM :

To write a html webpage page to display your slot timetable.

## ALGORITHM :

### STEP 1 
Create a Django-admin Interface.

### STEP 2
Create a static folder and inert HTML code.

### STEP 3
Create a simple table using ```<table>``` tag in html.

### STEP 4
Add header row using ```<th>``` tag.

### STEP 5
Add your timetable using ```<td>``` tag.

### STEP 6
Execute the program using runserver command.

## PROGRAM : 

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>SURYA 212224230280 EX3</title>

<style>
  :root{
    --card-bg: #ffffff;
    --page-bg-from: #fff4e6;
    --page-bg-to: #ffe6f0;
    --header: #40312f;
    --accent: #ffb366;
    --accent-2: #ffd699;
    --muted: #666;
  }

  body{
    margin:0;
    padding:18px;
    font-family: "Segoe UI", Roboto, Arial, sans-serif;
    background: linear-gradient(135deg, var(--page-bg-from), var(--page-bg-to));
    -webkit-font-smoothing:antialiased;
  }

  .container{
    max-width:1100px;
    margin: 8px auto;
    background: var(--card-bg);
    border-radius:12px;
    padding:18px;
    box-shadow: 0 8px 30px rgba(0,0,0,0.12);
  }

  .logo {
    display:block;
    margin: 6px auto 10px auto;
    max-width:420px;
    height:auto;
  }

  h2{
    margin:3px 0 2px;
    text-align:center;
    color: var(--header);
    font-size:22px;
    text-decoration:underline;
  }

  h3{
    margin:0 0 12px 0;
    text-align:center;
    color:var(--muted);
    font-weight:600;
    font-size:14px;
  }

  .table-wrapper{
    overflow-x:auto;
    -webkit-overflow-scrolling:touch;
    margin-bottom:12px;
  }

  .main-table{
    width:100%;
    border-collapse:collapse;
    table-layout: fixed;
    font-size:13px;
  }

  .main-table thead th{
    background: var(--accent);
    color:#111;
    font-weight:700;
    padding:8px 6px;
    border:1px solid rgba(0,0,0,0.08);
  }

  .main-table tbody td{
    border:1px solid rgba(0,0,0,0.06);
    padding:6px 6px;
    vertical-align:middle;
    color:#222;
    line-height:1.2;
  }

  .time-col{
    width:170px;
    white-space:nowrap;
    font-weight:700;
    text-align:center;
  }

  .lunch{
    background: var(--accent-2);
    font-weight:700;
    text-align:center;
    padding:4px !important;
    height:20px;
    line-height:20px;
  }

  caption{
    caption-side:top;
    text-align:center;
    font-weight:800;
    margin:8px 0 6px;
    font-size:16px;
    text-decoration:underline;
    color:var(--header);
  }

  /* SUBJECT TABLE — Fixed center alignment */
  .subject-table{
    width:60%;
    max-width:700px;
    margin: 12px auto 0 auto;
    border-collapse:collapse;
    font-size:13px;
    table-layout:auto;
  }

  .subject-table th,
  .subject-table td{
    border:1px solid rgba(0,0,0,0.15);
    padding:6px 6px;
    text-align:center;       /* Center-align EVERYTHING */
    vertical-align:middle;
    white-space:nowrap;
  }

  .subject-table th{
    background: var(--accent-2);
    font-weight:700;
  }

  .subject-table td:nth-child(3){
    white-space:normal;       /* Allow longer subjects to wrap neatly */
  }

  .subject-table caption{
    caption-side:top;
    text-align:center;
    font-weight:800;
    margin:8px 0 8px;
    font-size:15px;
    text-decoration:underline;
    color:var(--header);
  }

  @media (max-width:900px){
    .subject-table{ width:80%; }
    .time-col{ width:140px; font-size:12px; }
    .main-table{ font-size:12px; }
  }

  @media (max-width:520px){
    .subject-table{ width:95%; }
    .time-col{ width:120px; }
    .main-table{ font-size:11px; }
  }
</style>
</head>
<body>

<div class="container">
  <img class="logo" src="logo.png" alt="Logo - Surya P">

  <h2>SLOT TIME TABLE</h2>
  <h3>SURYA P (212224230280)</h3>

  <div class="table-wrapper">
    <table class="main-table">
      <thead>
        <tr>
          <th class="time-col">Time</th>
          <th>Sunday</th>
          <th>Monday</th>
          <th>Tuesday</th>
          <th>Wednesday</th>
          <th>Thursday</th>
          <th>Friday</th>
          <th>Saturday</th>
        </tr>
      </thead>

      <tbody>
        <tr>
          <td class="time-col">8:00 AM – 10:00 AM</td>
          <td></td>
          <td></td>
          <td>Computer Networks</td>
          <td></td>
          <td>Operating System</td>
          <td>Quantitative Ability I</td>
          <td></td>
        </tr>

        <tr>
          <td class="time-col">10:00 AM – 12:00 PM</td>
          <td></td>
          <td>Computer Architecture</td>
          <td>Statistics & Numerical Methods</td>
          <td>Statistics & Numerical Methods</td>
          <td>Web Application Development</td>
          <td>Computer Architecture</td>
          <td></td>
        </tr>

        <tr class="lunch">
          <td class="time-col">12:00 PM – 1:00 PM</td>
          <td colspan="7">LUNCH BREAK</td>
        </tr>

        <tr>
          <td class="time-col">1:00 PM – 3:00 PM</td>
          <td></td>
          <td>HRM & Team Building</td>
          <td>HRM & Team Building</td>
          <td>Mentor Meet</td>
          <td>Introduction to MEMS</td>
          <td>Operating System</td>
          <td></td>
        </tr>

        <tr>
          <td class="time-col">3:00 PM – 5:00 PM</td>
          <td></td>
          <td>Introduction to MEMS</td>
          <td></td>
          <td>Reasoning Ability</td>
          <td>Computer Networks</td>
          <td></td>
          <td></td>
        </tr>
      </tbody>
    </table>
  </div>

  <table class="subject-table">
    <caption>SUBJECT CODE LIST</caption>
    <thead>
      <tr>
        <th>S. No.</th>
        <th>Subject Code</th>
        <th>Subject Name</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>1</td><td>19AI414</td><td>Fundamentals of Web Application Development</td></tr>
      <tr><td>2</td><td>19CS305</td><td>Computer Architecture</td></tr>
      <tr><td>3</td><td>19CS405</td><td>Operating System</td></tr>
      <tr><td>4</td><td>19CS406</td><td>Computer Networks</td></tr>
      <tr><td>5</td><td>19EC602</td><td>Introduction to Micro Electro Mechanical Systems</td></tr>
      <tr><td>6</td><td>19EY709</td><td>Reasoning Ability</td></tr>
      <tr><td>7</td><td>19EY710</td><td>Quantitative Ability I</td></tr>
      <tr><td>8</td><td>19MA211</td><td>Statistics and Numerical Methods</td></tr>
      <tr><td>9</td><td>19MS156</td><td>Human Resource Management & Team Building</td></tr>
    </tbody>
  </table>

</div>

</body>
</html>

```

## OUTPUT : 

<img width="1919" height="1031" alt="image" src="https://github.com/user-attachments/assets/0adf7b9d-0b5f-4ecd-8859-aa370f0d5d33" />

## RESULT :
The program for creating slot timetable using basic HTML tags is executed successfully.
