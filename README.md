# Mini Calendar

This is a simple HTML, CSS, and JavaScript code snippet for creating a mini calendar with the current month, day, day of the week, day number, and year displayed.


# All in one code
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Mini Calendar</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: sans-serif;
        }

        body {
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: cyan;
        }

        .calendar {
            background-color: white;
            width: 40%;
            text-align: center;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            overflow: hidden;
        }

        .month {
            margin: 0;
            background-color: blue;
            color: #fff;
            font-weight: bold;
            padding: 10px;
            margin-bottom: 10px;
        }

        .day {
            font-size: 20px;
            color: darkgray;
        }

        .day-number {
            font-size: 80px;
            margin: 0;
            font-weight: bold;
        }

        .year {
            margin: 20px 0;
            font-size: 20px;
            color: darkgray;
            font-weight: 500;
        }
    </style>
</head>

<body>
    <div class="calendar">
        <p class="month" id="month">April</p>
        <p class="day" id="day">Sunday</p>
        <p class="day-number" id="day-number">12</p>
        <p class="year" id="year">2021</p>
    </div>

    <script>
        const monthEl = document.getElementById("month");
        const dayNameEl = document.getElementById("day");
        const dayNumEl = document.getElementById("day-number");
        const yearEl = document.getElementById("year");

        const date = new Date();

        const month = date.getMonth();

        monthEl.innerHTML = date.toLocaleDateString("en", {
            month: "long",
        });

        dayNameEl.innerHTML = date.toLocaleDateString("en", {
            weekday: "long",
        });

        dayNumEl.innerHTML = date.getDate();
        yearEl.innerHTML = date.getFullYear();
    </script>
</body>
</html>
