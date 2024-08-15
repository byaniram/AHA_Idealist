# AHA_Idealist
Repository for assets related to AHA ideas

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>API Call with Bearer Token</title>
</head>
<body>
    <h1>API Call with Bearer Token</h1>
    <form id="apiForm">
        <label for="userInput">Enter your org email address:</label>
        <input type="text" id="email" name="email" required>
        <button type="submit">Submit</button>
    </form>

    <div id="response"></div>

    <script>
        document.getElementById('apiForm').addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent the form from submitting the traditional way

            const userInput = document.getElementById('userInput').value;
            const url = `https://uat.elastic.snaplogic.com/api/1/rest/slsched/feed/QA/RB_Temp_Space/AHA_Report_Final_/GetIdeasByOrganization_Exec.csv?param=${encodeURIComponent(userInput)}`;
            const bearerToken = 'ZuNJBSjoyCAc7SDBJI11zbLGHwFC2mMV'; // Replace with your actual bearer token

            fetch(url, {
                method: 'GET',
                headers: {
                    'Authorization': `Bearer ${bearerToken}`,
                    'Content-Type': 'application/json'
                }
            })
     </script>
</body>
</html>
