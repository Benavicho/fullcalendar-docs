<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FullCalendar Demo</title>
    <!-- FullCalendar CSS -->
    <link href="https://cdn.jsdelivr.net/npm/fullcalendar@5.10.2/main.min.css" rel="stylesheet">
    <!-- FullCalendar JS -->
    <script src="https://cdn.jsdelivr.net/npm/fullcalendar@5.10.2/main.min.js"></script>
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #f4f7f9;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        #calendar {
            max-width: 900px;
            margin: 20px auto;
            padding: 20px;
            background-color: #ffffff;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }

        .fc-toolbar {
            background-color: #3b82f6;
            color: #ffffff;
            border-radius: 8px 8px 0 0;
        }

        .fc-button {
            background-color: #3b82f6;
            color: white;
            border: none;
            margin: 5px;
            border-radius: 5px;
            padding: 5px 10px;
        }

        .fc-button:hover {
            background-color: #2563eb;
        }

        .fc-daygrid-day {
            transition: background-color 0.3s ease;
        }

        .fc-daygrid-day:hover {
            background-color: #e0f2fe;
        }

        .fc-event {
            background-color: #3b82f6;
            color: white;
            border: none;
            padding: 5px;
            border-radius: 5px;
            text-align: center;
        }

        .fc-bg-event {
            background-color: rgba(59, 130, 246, 0.3);
        }
    </style>
</head>
<body>

    <div id="calendar"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            var calendarEl = document.getElementById('calendar');

            var calendar = new FullCalendar.Calendar(calendarEl, {
                initialDate: '2014-11-10',
                initialView: 'timeGridWeek',
                events: [
                    {
                        start: '2014-11-10T10:00:00',
                        end: '2014-11-10T16:00:00',
                        display: 'background'
                    }
                ]
            });

            calendar.render();
        });
    </script>

</body>
</html>
