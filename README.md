# PassX – Personal Password Manager

PassX is a simple, browser-based password manager built with **HTML, CSS, and vanilla JavaScript**. It lets users save website credentials, view saved entries, copy website names/usernames/passwords, and delete entries.

> **Important security notice:** This project stores passwords in the browser's `localStorage` as plain text. It does not encrypt passwords and is intended for learning/demo purposes only. Do not use it to store real, sensitive, or production passwords. Anyone with access to the same browser profile or device may be able to inspect the saved data.

## Features

- Add a website, username, and password.
- Save entries in browser `localStorage`.
- Display saved credentials in a table.
- Mask passwords in the displayed table.
- Copy website names, usernames, and passwords using the copy icons.
- Delete saved entries.

## Tech Stack

- **HTML5** – page structure
- **CSS3** – styling and layout
- **JavaScript (Vanilla)** – application logic and browser storage
- **Browser APIs** – `localStorage` and Clipboard API

## Project Structure

```text
passx-password-manager/
├── index.html
├── style.css
├── script.js
├── copy.svg
└── README.md
```

## Run Locally

No build tools or package installation are required.

1. Clone the repository:

   ```bash
   git clone https://github.com/<your-username>/<your-repository-name>.git
   ```

2. Open the project folder:

   ```bash
   cd <your-repository-name>
   ```

3. Open `index.html` in your browser.

   Alternatively, use the **Live Server** extension in Visual Studio Code.

## Deploy on Vercel

PassX is a static frontend project, so it can be deployed on Vercel without a backend or build command.

1. Push the project to a GitHub repository.
2. Sign in to [Vercel](https://vercel.com/) using your GitHub account.
3. Select **Add New → Project**.
4. Import your PassX GitHub repository.
5. In project configuration, use:
   - **Framework Preset:** Other
   - **Root Directory:** `./` (or the folder containing `index.html`)
   - **Build Command:** leave empty
   - **Output Directory:** leave empty / use `.` if Vercel requires a value
   - **Install Command:** leave empty
6. Select **Deploy**.
7. Once deployment finishes, open the Vercel-provided URL to test the application.

If the project files are inside a subfolder in the repository, set that subfolder as the Vercel **Root Directory**.

## Data Storage and Limitations

- Password entries are stored in the browser's `localStorage` under the key `passwords`.
- Data is local to the browser and origin. It is not synced between devices or browsers.
- Clearing browser site data can remove saved entries.
- Deploying the site to Vercel does not create a database or provide server-side storage.
- Passwords are currently stored without encryption. Masking them in the table only changes how they are displayed; it does not protect the stored values.
- Clipboard access generally requires a secure context (such as HTTPS) or localhost and may depend on browser permissions.

## Future Improvements

- Encrypt credentials before storing them.
- Add a master-password-based unlock flow.
- Add show/hide password controls.
- Add search and edit functionality.
- Add stronger input validation and safer DOM rendering.
- Add secure server-side storage and authentication if the project is extended beyond a local demo.

## Contributing

This is a beginner-friendly learning project. Feel free to fork the repository, experiment with the code, and submit improvements.

## License

No license has been specified yet. Add a license file if you want to define how others may use, modify, and distribute this project.
