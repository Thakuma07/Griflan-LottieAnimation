# ✨ Guiding Light

> "Interaction that whispers, light that guides."

**Guiding Light** is a minimal, immersive web experience built with a focus on subtle user interaction. It features a reactive spotlight that follows the cursor, illuminating content only when approached, accompanied by a dynamic Lottie fire animation that trails the mouse movement with a smooth, eased follow-up.

---

## 📽️ Visual Experience

<img width="1920" height="1080" alt="Screenshot (346)" src="https://github.com/user-attachments/assets/5da9e8ea-bc42-4176-b50c-15562164492c" />

---

## 🚀 Key Features

- 🌫️ **Interactive Spotlight Mask**: A dynamic CSS radial gradient mask that reveals the content as the user moves their mouse.
- 🔥 **Lottie Cursor Trail**: A high-quality "Fire" animation (Lottie) that follows the cursor using custom easing logic.
- 🌊 **Smooth Scrolling**: Integrated with **Lenis** for a premium, buttery-smooth scrolling experience.
- 🎨 **Aesthetic Typography**: Uses the "Amarante" font for a mystical, elegant feel.
- 📱 **Responsive Design**: Fluid typography and layouts that adapt across different screen sizes.

---

## 🛠️ Tech Stack

- **HTML5/CSS3**: Core structure and advanced masking techniques.
- **JavaScript (ES6+)**: Custom mouse tracking and state management.
- **[Lenis](https://github.com/darkroomengineering/lenis)**: For smooth scrolling.
- **[Lottie-web](https://github.com/airbnb/lottie-web)**: For rendering high-performance vector animations.

---

## 📂 Project Structure

```text
Guiding Light/
├── fonts/               # Custom Amarante typography
├── Fire.json            # Lottie animation data
├── index.html           # Main structure
├── styles.css           # Styling & Masking logic
├── script.js            # Animation loop & Interactive logic
└── README.md            # You are here!
```

---

## ⚙️ How It Works

### 1. The Spotlight Mask
The "invisibility" is achieved through a CSS `radial-gradient` acting as a mask.
```css
.spotlight-mask {
    mask: radial-gradient(
        circle 220px at var(--mouse-x) var(--mouse-y),
        transparent 0%,
        transparent 40%,
        black 80%
    );
}
```
The `--mouse-x` and `--mouse-y` variables are updated in real-time via the JavaScript `animate()` loop.

### 2. Cursor Tracking Logic
To ensure smooth movement, the cursor position is calculated with easing:
```javascript
pos.mouse.current.x += (pos.mouse.target.x - pos.mouse.current.x) * 0.1;
pos.mouse.current.y += (pos.mouse.target.y - pos.mouse.current.y) * 0.1;
```
This prevents the "Fire" animation from snapping to the mouse, giving it a weightier, more fluid feel.

---

## ⚡ Setup & Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/guiding-light.git
   ```
2. **Open the project**:
   Simply open `index.html` in your favorite web browser.

No build tools or heavy dependencies required!

---

## 🖌️ Customization

- **Change Spotlight Size**: Modify the `220px` value in `styles.css` under `.spotlight-mask`.
- **Change Animation Speed**: Adjust the `0.1` multiplier in `script.js` inside the `animate()` function.
- **Switch Animations**: Replace `Fire.json` with any other Lottie JSON file in the root directory.

---

## 📜 Credits

- Smooth Scroll by **Lenis**.
- Animations powered by **Lottie-web**.
- Developed by **thakuma.dev**.
