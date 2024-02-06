#!/usr/bin/perl

use strict;
use warnings;

print "Content-type: text/html\n\n";

print <<HTML;
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Task Scheduler</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
    </style>
</head>
<body>
    <h1>Task Scheduler</h1>

    <form action="/cgi-bin/schedule_task.cgi" method="post">
        <label for="taskDescription">Task Description:</label>
        <input type="text" name="taskDescription" required>
        
        <label for="dueDate">Due Date (YYYY-MM-DD):</label>
        <input type="text" name="dueDate" required>
        
        <button type="submit">Schedule Task</button>
    </form>

    <h2>Upcoming Tasks:</h2>
    <!-- Display upcoming tasks here -->

    <script>
        // You can add JavaScript for handling AJAX requests to interact with the server
    </script>
</body>
</html
