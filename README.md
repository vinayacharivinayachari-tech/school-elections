school-election/
│
├── index.html           <-- Main landing + login selection
├── admin.html           <-- Admin dashboard
├── teacher.html         <-- Teacher dashboard
├── voter.html           <-- Voter login page
├── vote.html            <-- Voting page
├── results.html         <-- Live results page
│
├── css/
│   └── style.css        <-- Styling for all pages
│
├── js/
│   └── app.js           <-- Handles login, votes, live update, backup/restore
│
├── data/                <-- JSON data storage (optional: simulate DB)
│   ├── candidates.json
│   ├── voters.json
│   ├── teachers.json
│   └── votes.json
│
└── images/              <-- Photos & school logo
    └── school-logo.png
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>G M H P S GILLESUGUR Election</title>
<link rel="stylesheet" href="css/style.css">
</head>
<body>
<header>
    <img src="images/school-logo.png" alt="School Logo" class="logo">
    <h1>G M H P S GILLESUGUR, Tq/Dist – RAICHUR</h1>
</header>

<main>
    <h2>Login</h2>
    <div class="login-options">
        <a href="admin.html" class="btn">Admin / Teacher</a>
        <a href="voter.html" class="btn">Student</a>
    </div>

    <h2>Live Candidate Votes</h2>
    <div id="live-votes">
        <!-- Candidate cards dynamically loaded via JS -->
    </div>
</main>

<script src="js/app.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Admin Dashboard</title>
<link rel="stylesheet" href="css/style.css">
</head>
<body>
<header>
    <img src="images/school-logo.png" alt="School Logo" class="logo">
    <h1>Admin Dashboard</h1>
</header>

<main>
    <section>
        <h2>Manage Candidates</h2>
        <button onclick="addCandidate()">Add Candidate</button>
        <div id="candidate-list"></div>
    </section>

    <section>
        <h2>Manage Voters</h2>
        <button onclick="addVoter()">Add Voter</button>
        <div id="voter-list"></div>
    </section>

    <section>
        <h2>Manage Teachers</h2>
        <button onclick="addTeacher()">Add Teacher</button>
        <div id="teacher-list"></div>
    </section>

    <section>
        <h2>Other Actions</h2>
        <button onclick="uploadLogo()">Upload School Logo</button>
        <button onclick="resetAll()">Reset All Data</button>
        <button onclick="exportBackup()">Export Backup</button>
        <button onclick="importBackup()">Import Backup</button>
    </section>

    <section>
        <h2>Live Results</h2>
        <div id="live-results"></div>
    </section>
</main>

<script src="js/app.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Teacher Dashboard</title>
<link rel="stylesheet" href="css/style.css">
</head>
<body>
<header>
    <h1>Teacher Dashboard</h1>
</header>
<main>
    <h2>Class Voter List</h2>
    <div id="class-voters"></div>

    <h2>Class Live Results</h2>
    <div id="class-results"></div>
</main>
<script src="js/app.js"></script>
</body>
</html>


