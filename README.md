# Deployment Instructions for Streamlit Community Cloud

This folder contains everything you need to deploy your PyPSA-Earth visualization app for free on Streamlit Community Cloud.

## Steps to Deploy

1.  **Create a GitHub Repository**:
    *   Go to [GitHub](https://github.com) and create a new repository (e.g., `pypsa-viz-app`).
    *   Make it **Public** (required for free Streamlit Cloud, unless you have a paid plan).

2.  **Upload Files**:
    *   Upload ALL the files in this `viz_deployment` folder to your new GitHub repository.
    *   You can do this via the web interface ("Upload files") or using git commands if you are familiar with them.
    *   **Important**: Ensure `viz_app.py`, `requirements.txt`, and the `.nc` / `.geojson` files are in the root of the repository.

3.  **Deploy on Streamlit Cloud**:
    *   Go to [Streamlit Community Cloud](https://share.streamlit.io/).
    *   Sign in with GitHub.
    *   Click **"New app"**.
    *   Select your new repository (`pypsa-viz-app`).
    *   **Main file path**: Enter `viz_app.py`.
    *   Click **"Deploy!"**.

## Troubleshooting

*   **File Size**: GitHub has a limit of 100MB per file. Your network file is small (~6MB) and profile files are ~30MB, so they will upload fine.
*   **Memory**: Streamlit Cloud gives you around 1GB of RAM. If your app crashes with "Argh, the app is having trouble loading", it might be running out of memory. 
    *   *Solution*: Try to use smaller network files if possible, or optimize the code to load less data at once.
