# Analog Clock

An elegant and fully functional analog clock created using **HTML**, **CSS**, and **JavaScript**. This project demonstrates how to dynamically render a real-time analog clock in a web browser, utilizing basic web development techniques and animations.

---

## Features

- **Dynamic Time Update**: Displays the current time with hour, minute, and second hands.
- **Smooth Animation**: Utilizes CSS transitions for smooth movement of the clock hands.
- **Customizable Design**: Easy to update the clock’s appearance using CSS.
- **Lightweight**: No external libraries or frameworks required.

---

## Live Demo

[Live Demo Link](#) (Replace with your deployment link)

---

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/analog-clock.git
   ```

2. **Navigate to the Project Directory**:
   ```bash
   cd analog-clock
   ```

3. **Open the `index.html` File in a Browser**:
   ```bash
   open index.html
   ```
   Or double-click on the `index.html` file to view the clock in your browser.

---

## File Structure

```
analog-clock/
├── index.html   # HTML structure of the clock
├── style.css    # Styling for the clock
├── script.js    # JavaScript logic for functionality
└── README.md    # Project documentation
```

---

## How It Works

1. **HTML**:
   - Provides the basic structure for the clock, including a container for the clock face and clock hands.

2. **CSS**:
   - Styles the clock face and hands.
   - Adds transitions for smooth movement of the hands.

3. **JavaScript**:
   - Retrieves the current time using the `Date` object.
   - Calculates the rotation angles for each clock hand.
   - Updates the hands in real-time using `setInterval`.

---

## Customization

You can customize the clock design by modifying the `style.css` file:

- **Clock Face**:
  - Background color, border, and size.
- **Clock Hands**:
  - Width, length, and color.
- **Animations**:
  - Transition effects for smoother hand movement.

---

## Example Code

### HTML (Basic Structure):
```html
<div class="clock">
  <div class="hand hour" id="hour"></div>
  <div class="hand minute" id="minute"></div>
  <div class="hand second" id="second"></div>
</div>
```

### CSS (Clock Styling):
```css
.clock {
  position: relative;
  width: 200px;
  height: 200px;
  border: 5px solid black;
  border-radius: 50%;
  background: white;
}
.hand {
  position: absolute;
  width: 50%;
  height: 2px;
  background: black;
  transform-origin: 100%;
  transform: rotate(90deg);
  transition: transform 0.05s ease-in-out;
}
```

### JavaScript (Dynamic Updates):
```javascript
setInterval(() => {
  const now = new Date();
  const seconds = now.getSeconds();
  const minutes = now.getMinutes();
  const hours = now.getHours();

  const secondHand = document.getElementById('second');
  const minuteHand = document.getElementById('minute');
  const hourHand = document.getElementById('hour');

  secondHand.style.transform = `rotate(${seconds * 6}deg)`;
  minuteHand.style.transform = `rotate(${minutes * 6 + seconds / 10}deg)`;
  hourHand.style.transform = `rotate(${hours * 30 + minutes / 2}deg)`;
}, 1000);
```

---

## Contribution

Contributions are welcome! If you have suggestions or improvements, feel free to open an issue or submit a pull request.

---

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute this project as per the license terms.

---

## Contact

For any queries or feedback, contact:
- **Email**: your-email@example.com
- **GitHub**: [IamAffaanNadeem001](https://github.com/IamAffaanNadeem001)

