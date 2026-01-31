# GCQL Playground

A **CTF (Capture The Flag) challenge** built as an interactive **GCQL Playground**. You write GCQL queries in a query editor, run them against simulated log data, and use the results to find hidden flags.

The app is a single, self-contained HTML file—no backend, no build step, no dependencies. Everything runs in your browser.

## What’s in the project

- **Query editor** – Write and run GCQL queries (e.g. full-text search, filters like `level:ERROR`, pipes like `| stats by (workload) count()`).
- **Results** – Tables and logs for query results.
- **CTF flow** – Hints and flags tied to solving query challenges.

Example queries you might use:

- `timeout` — search the content field  
- `level:ERROR workload:api*` — filter by level and workload  
- `* | stats by (workload) count()` — aggregate and group  

## How to get the code (pull)

**Prerequisites:** [Git](https://git-scm.com/) installed.

**Clone the repo (SSH):**

```bash
git clone git@github.com:johndexteriv/gcql_playground.git
cd gcql_playground
```

**Or clone with HTTPS:**

```bash
git clone https://github.com/johndexteriv/gcql_playground.git
cd gcql_playground
```

To **update** an existing clone later:

```bash
cd gcql_playground
git pull origin main
```

## How to run it locally

1. Open the project folder and double‑click **`playground.html`**,  
   **or**
2. From the project directory, start a simple local server (optional, avoids some browser file restrictions):

   **Python 3:**

   ```bash
   python3 -m http.server 8000
   ```

   **Node (npx):**

   ```bash
   npx serve -p 8000
   ```

   Then in your browser go to: **http://localhost:8000/playground.html**

No install, no `npm install`, no build—just open the HTML file or serve it and play.
