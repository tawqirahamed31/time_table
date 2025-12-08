# Ex02 Time Table
# Date:
8-12-2025
# AIM
To write a html webpage page to display your slot timetable.

# ALGORITHM
## STEP 1
Create a Django-admin Interface.

## STEP 2
Create a static folder and inert HTML code.

## STEP 3
Create a simple table using `<table>` tag in html.

## STEP 4
Add header row using `<th>` tag.

## STEP 5
Add your timetable using `<td>` tag.

## STEP 6
Execute the program using runserver command.

# PROGRAM
    {% load static %}
    <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>{{ title }}</title>
      <meta name="viewport" content="width=device-width,initial-scale=1">
      <link rel="stylesheet" href="{% static 'css/style.css' %}">
    </head>
    <body>
      <div class="page">
        <header class="page-header">
        <img class="college-logo" src="{% static 'images/logo.png' %}" alt="college logo">
        </header>
    
        <main>
          <h1 class="main-title">SLOT TIMETABLE - TAWQIR AHAMED SAYEED L - 25003294</h1>
    
          <section class="timetable-wrap">
            <div class="timetable-card">
              <table class="timetable">
                <thead>
                  <tr>
                    <th>Day/Time</th>
                    <th>Monday</th>
                    <th>Tuesday</th>
                    <th>Wednesday</th>
                    <th>Thursday</th>
                    <th>Friday</th>
                    <th>Saturday</th>
                  </tr>
                </thead>
                <tbody>
                  {% for row in timetable %}
                  <tr>
                    <td class="slot">{{ row.slot }}</td>
                    <td>{{ row.Monday }}</td>
                    <td>{{ row.Tuesday }}</td>
                    <td>{{ row.Wednesday }}</td>
                    <td>{{ row.Thursday }}</td>
                    <td>{{ row.Friday }}</td>
                    <td>{{ row.Saturday|default:'' }}</td>
                  </tr>
                  {% endfor %}
                </tbody>
              </table>
            </div>
          </section>
    
          <section class="subjects-wrap">
            <h2>Subjects</h2>
            <table class="subjects">
              <thead>
                <tr><th>S.No</th><th>Subject Code</th><th>Subject name</th></tr>
              </thead>
              <tbody>
                {% for s in subjects %}
                <tr>
                  <td>{{ s.no }}</td>
                  <td>{{ s.code }}</td>
                  <td>{{ s.name }}</td>
                </tr>
                {% endfor %}
              </tbody>
            </table>
          </section>
        </main>
      </div>
    </body>
    </html>


# OUTPUT
<img width="1919" height="938" alt="image" src="https://github.com/user-attachments/assets/b4e12219-0bcc-4e88-9c97-78bcdb56d41d" />

# RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
