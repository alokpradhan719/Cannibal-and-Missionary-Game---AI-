# Cannibals & Missionary Problem — AI Game

A classic AI puzzle game exploring **state-space search** and **constraint satisfaction problems** using **Breadth-First Search (BFS)**.

## Problem

N missionaries and N cannibals must cross a river using a single boat (capacity: 2 people max). The boat cannot cross empty—someone must row. Cannibals must never outnumber missionaries on either bank.

## Features

- **Interactive Gameplay**: Manually solve the puzzle or watch the AI auto-solve
- **AI Auto-Solve**: Optimal solution using BFS algorithm
- **Multiple Difficulty Levels**: Adjust N (number of missionaries/cannibals)
- **Rule Validation**: Real-time constraint checking
- **Responsive Design**: Dark and light theme support

## Technologies

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Algorithm**: Breadth-First Search (BFS)
- **Deployment**: Vercel

## How to Play

1. Visit: [Live Game](https://your-deployment-url.com) (or run locally)
2. Choose game size (default: 3 missionaries, 3 cannibals)
3. Move people across the river using the boat
4. Ensure cannibals never outnumber missionaries
5. Get everyone to the other bank!

## Local Setup

```bash
# Clone the repo
git clone https://github.com/alokpradhan719/Cannibal-and-Missionary-Game---AI-.git
cd Cannibal-and-Missionary-Game---AI-

# Run local server
node -e "const http = require('http'); const fs = require('fs'); const path = require('path'); const server = http.createServer((req, res) => { let filePath = req.url === '/' ? '/index.html' : req.url; filePath = path.join(__dirname, filePath); const ext = path.extname(filePath); const mimeTypes = { '.html': 'text/html', '.css': 'text/css', '.js': 'application/javascript' }; const contentType = mimeTypes[ext] || 'text/plain'; fs.readFile(filePath, (err, data) => { if (err) res.writeHead(404).end(); else res.writeHead(200, { 'Content-Type': contentType }).end(data); }); }); server.listen(8080, () => console.log('http://localhost:8080'));"
```

Open `http://localhost:8080` in your browser.

## Algorithm

**Breadth-First Search (BFS)**
- Explores states level-by-level
- Guarantees shortest solution path
- Time Complexity: O(V + E)
- Space Complexity: O(V)

## File Structure

```
.
├── index.html       # Introduction & rules
├── game.html        # Game interface
├── vercel.json      # Deployment config
└── README.md        # This file
```

## Author

[Alok Pradhan](https://github.com/alokpradhan719)

## License

MIT
