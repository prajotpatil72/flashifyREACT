# ⚡ FlashScreen Component

A customizable full-screen splash screen React component with animation, typing effects, and styling options.

## 📁 Files

- `FlashScreen.jsx` – Main component
- `FlashScreen.css` – Animation and layout styles
- `README.md` – Documentation

## 🔧 Props

| Prop Name            | Type      | Default      | Description |
|----------------------|-----------|---------------|-------------|
| `name`               | `string`  | `"MyWebsite"` | Text to display. |
| `duration`           | `number`  | `5000`        | Duration of display (ms). |
| `onComplete`         | `func`    | `() => {}`    | Callback on finish. |
| `backgroundColor`    | `string`  | `"#000000"`   | Background color. |
| `textColor`          | `string`  | `"#ffffff"`   | Text color. |
| `fontSize`           | `string`  | `"4xl"`       | Tailwind font size class. |
| `fontWeight`         | `string`  | `"bold"`      | Tailwind font weight. |
| `fontFamily`         | `string`  | `"sans-serif"`| Custom font. |
| `flowAnimation`      | `bool`    | `false`       | Typewriter effect toggle. |
| `flowSpeed`          | `number`  | `200`         | Typing speed (ms). |
| `timeBasedExecution` | `bool`    | `true`        | Auto-dismiss on time. |
| `showUnderline`      | `bool`    | `true`        | Show underline below text. |
| `underlineColor`     | `string`  | `"#ffffff"`   | Color of underline. |
| `animationType`      | `string`  | `"fade"`      | Animation type (`fade`, `pulse`, `bounce`). |
| `customStyles`       | `object`  | `{}`          | Extra CSS styles. |

## 💡 Usage Example

```jsx
import FlashScreen from './FlashScreen';

<FlashScreen
  name="Welcome!"
  duration={4000}
  backgroundColor="#111827"
  textColor="#FACC15"
  fontSize="5xl"
  flowAnimation={true}
  animationType="bounce"
  onComplete={() => console.log("Flash done!")}
/>
