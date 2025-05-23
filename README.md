# Random Cat Viewer ✨

A fun and stylish web application that displays random cat images fetched from Reddit's r/cats subreddit. It features a cool glowing "cyberpunk" aesthetic and a playful "cuteness warning" popup on entry.

## 🚀 Features

*   **Random Cat Images:** Fetches and displays random cat images from the r/cats subreddit.
*   **Eye-Catching UI:** Modern, responsive design with a "cyberpunk" glow aesthetic using CSS variables, gradients, and animations.
*   **Cuteness Warning Popup:** An initial modal warns users of the extreme cuteness ahead, requiring acceptance to proceed.
*   **Loading Indicator:** Displays a "Loading cuteness..." message while fetching images.
*   **Error Handling:** Provides user-friendly messages if an image fails to load or if the API encounters an issue.
*   **"Fetch New Cat!" Button:** Allows users to easily load a new random cat image.
*   **Responsive Design:** Adapts to different screen sizes for a good experience on desktop and mobile.

## 🛠️ Technologies Used

*   **HTML5:** For the basic structure of the web page.
*   **CSS3:** For styling, including:
    *   CSS Custom Properties (Variables)
    *   Flexbox & Grid (implied for layout)
    *   Gradients
    *   Text Shadows & Box Shadows for glow effects
    *   Keyframe Animations (for pulsating glow)
    *   Transitions
    *   Responsive design with Media Queries
*   **JavaScript (Vanilla JS):**
    *   DOM Manipulation
    *   `fetch` API for making asynchronous requests to the Reddit API
    *   `async/await` for cleaner asynchronous code
    *   Event Handling
*   **Google Fonts:**
    *   Orbitron (for headings)
    *   Poppins (for body text)
*   **Reddit API:** Unofficial, public JSON endpoint for `r/cats/hot.json` to source images.

## ⚙️ How It Works

1.  **Initial Popup:** On page load, a modal dialog ("Paws for a Cuteness Warning!") is displayed. Users must click "I Accept" to continue.
2.  **Fetching Images:**
    *   After the popup is closed, or when the "Fetch New Cat!" button is clicked, an asynchronous `fetch` request is made to `https://www.reddit.com/r/cats/hot.json?limit=100`.
    *   The JSON response is parsed.
    *   Posts are filtered to include only those with direct image URLs (ending in `.jpg`, `.jpeg`, `.png`, or `.gif`).
    *   A random post is selected from the filtered list.
3.  **Displaying Image:**
    *   The `src` attribute of the main image element (`#img`) is set to the selected image URL.
    *   The `alt` attribute is set to the post title or a default "cute cat" message.
    *   Loading and error states are handled, updating the UI accordingly (showing/hiding loader, displaying error messages in `alt` text).
    *   CSS classes (`.loaded`, `.loading-error`) are used to manage the visual state and transitions of the image.

## 📂 Project Structure

```
└── index.html       # The single HTML file containing all markup, styles, and scripts.
```

## 🚀 Getting Started

Since this is a front-end only project, setting it up is straightforward:

1.  **Clone the repository (or download the `index.html` file):**
    ```bash
    git clone https://github.com/KerimDemirkaynak/Random-Cat-Viewer.git
    cd Random-Cat-Viewer
    ```
2.  **Open `index.html` in your web browser:**
    *   Simply double-click the `index.html` file, or right-click and choose "Open with" your preferred browser.

No build steps or special dependencies are required beyond a modern web browser.

## 🔮 Potential Improvements & To-Do

*   [ ] **Use a dedicated Cat API:** The Reddit API can sometimes be unreliable or change. Using an API like [TheCatAPI](https://thecatapi.com/) would be more robust.
*   [ ] **Image Preloading:** Preload the next image in the background for a smoother transition when "Fetch New Cat!" is clicked.
*   [ ] **More Image Sources:** Allow users to select different subreddits (e.g., `r/MEOW_IRL`, `r/IllegallySmolCats`).
*   [ ] **Caching:** Cache image URLs or images to reduce API calls and improve loading times for previously seen images.
*   [ ] **Accessibility (A11y) Enhancements:** Further review and improve ARIA attributes and keyboard navigation.
*   [ ] **Separate CSS and JS:** For larger projects, it would be better to move CSS to a separate `.css` file and JavaScript to a `.js` file.
*   [ ] **Error Handling for API Rate Limits:** Implement more specific error handling if Reddit API rate limits are hit.
*   [ ] **Theming:** Allow users to choose different color themes.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/KerimDemirkaynak/Random-Cat-Viewer/issues) (if you create one).

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## 📜 License

This project is open source and available under the [MIT License](LICENSE.md) (You'll need to create a LICENSE.md file with the MIT license text if you want this link to work).

---

Made with ❤️ and 🐈 by Kerim Demirkaynak
