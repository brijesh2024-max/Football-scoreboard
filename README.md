# Football Scorecard

A simple, single-page football scorecard built with HTML, CSS, and vanilla JavaScript. It displays Home and Guest scores and provides quick +1/+2/+3 increment buttons for each team.

## Features
- Large, high-contrast score display for easy viewing.
- Dedicated +1, +2, +3 buttons for Home and Guest.
- Responsive layout that adapts to smaller screens.

## Getting Started

1. Save the provided `index.html` file (and optionally `scorecard.js` if you separated the script).
2. Open `index.html` in any modern browser.

## File Structure (single-file version)
- `index.html` — contains the markup, styles, and JavaScript.

If you separated the JavaScript:
- `index.html` — markup and styles, includes the script via `<script src="scorecard.js"></script>`.
- `scorecard.js` — click handlers and score logic.

## How It Works
- Each button has `data-team` (home/guest) and `data-val` (+1, +2, +3).
- A click event listener reads those attributes and updates the corresponding score display.

## Customization
- Colors: Adjust CSS variables at the top of the `<style>` block (`--bg`, `--board`, `--text`, etc.).
- Button set: Add more buttons with different `data-val` values if needed.
- Reset: Add a “Reset” button:
  ```html
  <div class="btn-row">
    <button id="reset">Reset</button>
  </div>
  ```
  And in JS:
  ```js
  document.getElementById("reset").addEventListener("click", () => {
    scores.home = scores.guest = 0;
    els.home.textContent = "0";
    els.guest.textContent = "0";
  });
  ```

## Browser Support
Tested on modern evergreen browsers (Chrome, Edge, Firefox). No external dependencies.

## License
MIT (feel free to use and modify).
