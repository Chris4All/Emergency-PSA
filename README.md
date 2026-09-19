# Emergency-PSA

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chris's PSA - The Offline Library</title>
    <style>
        :root {
            --bg-color: #120924;
            --card-bg: #1e1336;
            --text-main: #ffffff;
            --text-muted: #b5a9cc;
            --accent-red: #8b0000;
            --accent-green: #2e5a44;
            --accent-purple: #4a2868;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            display: flex;
            justify-content: center;
            padding: 20px;
            min-height: 100vh;
        }

        .container {
            width: 100%;
            max-width: 600px;
            padding: 20px 10px;
        }

        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding-bottom: 15px;
            margin-bottom: 40px;
        }

        .logo {
            font-size: 1.1rem;
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .nav-back {
            font-size: 0.75rem;
            color: var(--text-muted);
            text-decoration: none;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .subtitle {
            color: var(--text-muted);
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 10px;
        }

        h1 {
            font-size: 3.5rem;
            font-weight: 900;
            text-transform: uppercase;
            line-height: 0.9;
            margin-bottom: 30px;
            letter-spacing: -1px;
        }

        h1 span {
            color: #7d50a3;
            display: block;
        }

        .description {
            color: var(--text-muted);
            font-size: 1.1rem;
            line-height: 1.5;
            margin-bottom: 40px;
        }

        .btn-stack {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-bottom: 40px;
        }

        .btn {
            width: 100%;
            padding: 16px;
            border-radius: 30px;
            text-align: center;
            text-transform: uppercase;
            font-weight: bold;
            font-size: 0.9rem;
            letter-spacing: 2px;
            cursor: pointer;
            text-decoration: none;
            display: block;
            transition: opacity 0.2s ease;
        }

        .btn:hover {
            opacity: 0.9;
        }

        .btn-red {
            background-color: var(--accent-red);
            color: var(--text-main);
            border: none;
        }

        .btn-outline-purple {
            background-color: transparent;
            border: 2px solid var(--accent-purple);
            color: var(--text-main);
        }

        .btn-outline-green {
            background-color: transparent;
            border: 2px solid var(--accent-green);
            color: var(--text-main);
        }

        footer {
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            padding-top: 20px;
            color: var(--text-muted);
            font-size: 0.9.5rem;
            line-height: 1.6;
        }

        footer a {
            color: var(--text-main);
            font-weight: bold;
            text-decoration: none;
        }

        /* Hidden dynamic interactive area */
        .hidden-list {
            display: none;
            background-color: var(--card-bg);
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 25px;
        }

        .hidden-list.active {
            display: block;
        }

        .hidden-list h3 {
            margin-bottom: 10px;
            font-size: 1rem;
            color: #b5a9cc;
            text-transform: uppercase;
        }

        .hidden-list ul {
            list-style: none;
            padding-left: 0;
        }

        .hidden-list li {
            margin-bottom: 8px;
        }

        .hidden-list a {
            color: #00ffcc;
            text-decoration: none;
            font-size: 0.95rem;
        }
    </style>
</head>
<body>

    <div class="container">
        <header>
            <div class="logo">Chris's PSA</div>
            <a href="#" class="nav-back">Back to the home page</a>
        </header>

        <main>
            <div class="subtitle">The Offline Library</div>
            <h1>Just In<br><span>Case</span></h1>

            <p class="description">
                89 free PDFs from FEMA, the EPA, the National Weather Service, the Red Cross, 
                the USDA, the Geological Survey and the Consumer Product Safety Commission. 
                Every link was checked on 18 September 2026. Download them while the internet works, 
                because the whole point of having them is the day it doesn't.
            </p>

            <div class="btn-stack">
                <button class="btn btn-red" onclick="toggleMenu('phone-kit')">Start With The Phone Kit</button>
                
                <div id="phone-kit" class="hidden-list">
                    <h3>Essential Mobile Archives</h3>
                    <ul>
                        <li><a href="#">➔ Emergency Contacts Ledger Template.pdf</a></li>
                        <li><a href="#">➔ Compact First Aid & Triage Guide.pdf</a></li>
                        <li><a href="#">➔ Offline Map Calibration Standards.pdf</a></li>
                    </ul>
                </div>

                <button class="btn btn-outline-purple" onclick="toggleMenu('whole-list')">Show Me The Whole List</button>

                <div id="whole-list" class="hidden-list">
                    <h3>All 89 Agency Resource Links</h3>
                    <ul>
                        <li><a href="#">➔ FEMA - Comprehensive Family Disaster Plan.pdf</a></li>
                        <li><a href="#">➔ EPA - Safe Emergency Water Purification.pdf</a></li>
                        <li><a href="#">➔ NWS - Severe Weather Safety Master Protocol.pdf</a></li>
                        <li><a href="#">➔ Red Cross - Emergency Food Supply Logistics.pdf</a></li>
                    </ul>
                </div>

                <a href="https://gutenberg.org" target="_blank" class="btn btn-outline-green">Grab Some Free Books Too</a>
            </div>
        </main>

        <footer>
            While you are at it - <a href="https://gutenberg.org" target="_blank">Project Gutenberg</a> (gutenberg.org) has more than 79,000 free books, the classics and everything else whose copyright has run out.
        </footer>
    </div>

    <script>
        function toggleMenu(menuId) {
            const selectedMenu = document.getElementById(menuId);
            selectedMenu.classList.toggle('active');
        }
    </script>
</body>
</html>
