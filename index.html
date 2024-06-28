<?php
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "crms";


$conn = new mysqli($servername, $username, $password);


if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}


$sql_create_db = "CREATE DATABASE IF NOT EXISTS $dbname";
$conn->query($sql_create_db);


$conn->select_db($dbname);


$sql_create_table = "CREATE TABLE IF NOT EXISTS employees (
    id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL,
    birthday DATE NOT NULL
)";
$conn->query($sql_create_table);


function sendBirthdayReminders($conn) {
    $today = date('m-d');
    $sql = "SELECT name, email FROM employees WHERE DATE_FORMAT(birthday, '%m-%d') = '$today'";
    $result = $conn->query($sql);

    if ($result->num_rows > 0) {
        while ($row = $result->fetch_assoc()) {
            $name = $row['name'];
            $email = $row['email'];

            echo '<div class="alert alert-info" role="alert">Birthday message sent to ' . $name . ' (' . $email . ')</div>';
        }
    } else {
        echo '<div class="alert alert-info" role="alert">No birthdays today.</div>';
    }
}

if ($_SERVER["REQUEST_METHOD"] == "POST" && isset($_POST['add_employee'])) {
    $name = $_POST['name'];
    $email = $_POST['email'];
    $birthday = $_POST['birthday'];

    $sql = "INSERT INTO employees (name, email, birthday) VALUES ('$name', '$email', '$birthday')";

    if ($conn->query($sql) === TRUE) {
        echo '<div class="alert alert-success" role="alert">New employee added successfully</div>';
    } else {
        echo '<div class="alert alert-danger" role="alert">Error adding employee: ' . $conn->error . '</div>';
    }
}
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Insurance Company CRM - Employee Birthday Reminder</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
</head>
<body>

<div class="container mt-5">
    <div class="row">
        <div class="col-md-4">
            <div class="card">
                <div class="card-header">
                    Add Employee
                </div>
                <div class="card-body">
                    <form method="post" action="<?php echo $_SERVER['PHP_SELF'];?>">
                        <input type="hidden" name="add_employee" value="1">
                        <div class="form-group">
                            <label for="name">Name:</label>
                            <input type="text" class="form-control" id="name" name="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email:</label>
                            <input type="email" class="form-control" id="email" name="email" required>
                        </div>
                        <div class="form-group">
                            <label for="birthday">Birthday:</label>
                            <input type="date" class="form-control" id="birthday" name="birthday" required>
                        </div>
                        <button type="submit" class="btn btn-primary btn-block">Add Employee</button>
                    </form>
                </div>
            </div>
        </div>

        <div class="col-md-4">
            <div class="card">
                <div class="card-header">
                    Send Birthday Reminders
                </div>
                <div class="card-body">
                    <form method="get" action="<?php echo $_SERVER['PHP_SELF'];?>">
                        <input type="hidden" name="send_reminders" value="1">
                        <button type="submit" class="btn btn-success btn-block">Send Birthday Reminders</button>
                    </form>
                </div>
            </div>
        </div>

        <div class="col-md-4">
            <div class="card">
                <div class="card-header">
                    Employees List
                </div>
                <div class="card-body">
                    <table class="table">
                        <thead>
                            <tr>
                                <th>Name</th>
                                <th>Email</th>
                                <th>Birthday</th>
                            </tr>
                        </thead>
                        <tbody>
                            <?php
                            $sql_employees = "SELECT * FROM employees";
                            $result_employees = $conn->query($sql_employees);

                            if ($result_employees->num_rows > 0) {
                                while ($row = $result_employees->fetch_assoc()) {
                                    echo "<tr>";
                                    echo "<td>" . htmlspecialchars($row['name']) . "</td>";
                                    echo "<td>" . htmlspecialchars($row['email']) . "</td>";
                                    echo "<td>" . htmlspecialchars($row['birthday']) . "</td>";
                                    echo "</tr>";
                                }
                            } else {
                                echo '<tr><td colspan="3">No employees found</td></tr>';
                            }
                            ?>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>
</div>

