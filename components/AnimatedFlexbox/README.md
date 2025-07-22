# 🧩 AnimatedFlexbox React Component

The `AnimatedFlexbox` is a customizable and reusable React component that displays content and images in a responsive two-column layout with smooth scroll-based animation effects using the [`react-intersection-observer`](https://www.npmjs.com/package/react-intersection-observer) hook.

## ✨ Features

- Animated entry on scroll using `IntersectionObserver`
- Image and text content layout with flexible positioning
- Props-based customization
- Responsive and easy to integrate

## 📦 Installation

Install the required dependency:

```bash
npm install react-intersection-observer
```

Then add the component and its CSS to your project.

## 🧠 Usage

```jsx
import React from 'react';
import AnimatedFlexbox from './AnimatedFlexbox';
import './AnimatedFlexbox.css';

const content = [
  { title: 'Feature One', description: 'This is the first feature.' },
  { title: 'Feature Two', description: 'This is the second feature.' },
];

const App = () => (
  <AnimatedFlexbox
    imageSrc="/path/to/image.jpg"
    imageAlt="Descriptive alt text"
    contentItems={content}
    imagePosition="left" // or "right"
  />
);

export default App;
```

## 🧾 Props

| Prop Name     | Type       | Description                                             | Default   |
|---------------|------------|---------------------------------------------------------|-----------|
| `imageSrc`     | `string`   | URL/path of the image to display                        | **Required** |
| `imageAlt`     | `string`   | Alt text for the image                                  | **Required** |
| `contentItems` | `Array`    | Array of `{ title, description }` objects               | **Required** |
| `imagePosition`| `string`   | `"left"` or `"right"` to position image in layout       | `"left"`  |

## 🎨 Styling

The component expects styles from `AnimatedFlexbox.css`. Here's a basic starter CSS you can expand:

```css
.animated-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: stretch;
  gap: 2rem;
  margin: 2rem 0;
}

.animated-column {
  flex: 1;
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}

.animated-column.is-visible {
  opacity: 1;
  transform: translateY(0);
}

.text-box {
  margin-bottom: 1rem;
}

img {
  max-width: 100%;
  height: auto;
  border-radius: 8px;
}
```

## 📁 File Structure

```
components/
├── AnimatedFlexbox.jsx
├── AnimatedFlexbox.css
```

## ✅ Example

You can preview this component in action [here](https://react-portfolio-one-plum.vercel.app/) (if included in your portfolio or demo site).

## 🛠️ License

MIT — Feel free to use, modify, and distribute.

## 🙋‍♂️ Author

Made by [Prajot Patil](https://github.com/prajot-patil) 🚀