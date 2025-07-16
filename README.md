# Tailwind CSS v3 + React + Vite Template

A clean, modern template for React projects with Tailwind CSS v3 and Vite. This template eliminates the common setup headaches and gets you building beautiful UIs immediately.

## 🚀 Quick Start

### Use This Template

Click "Use this template" or clone directly:

```bash
git clone https://github.com/Grizak/tailwind-react-vite-template.git my-project
cd my-project
git checkout tailwind-v3.x.x
npm install
npm run dev
```

### What's Included

- ⚡ **Vite** - Fast build tool and dev server
- ⚛️ **React 18** - Latest React with modern features
- 🎨 **Tailwind CSS v3** - Stable, production-ready utility-first CSS framework
- 🔧 **PostCSS** - Seamless CSS processing
- 📦 **All configured** - Ready to use, no setup required

## 📁 Project Structure

```
├── src/
│   ├── App.jsx          # Main app component
│   ├── index.css        # Tailwind CSS imports
│   └── main.jsx         # React entry point
├── tailwind.config.js   # Tailwind configuration
├── postcss.config.js    # PostCSS configuration
├── vite.config.js       # Vite configuration
└── package.json
```

## 🎯 Key Features

### Single Command Development

```bash
npm run dev
```

No need to manage multiple terminal windows or separate build processes. Everything runs together with hot reload.

### Production Ready

```bash
npm run build
```

Automatically purges unused CSS and optimizes for production. Your final bundle only includes the Tailwind classes you actually use.

### Battle-Tested Tailwind v3

This template uses Tailwind CSS v3, the stable and widely-adopted version with excellent ecosystem support.

## 🔧 Configuration Details

### Tailwind v3 Setup

**postcss.config.js**

```javascript
export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
};
```

**src/index.css**

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Content Configuration

The template is configured to scan all your React files:

```javascript
// tailwind.config.js
/** @type {import('tailwindcss').Config} */
export default {
  content: ["./index.html", "./src/**/*.{js,ts,jsx,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

## 🎨 Example Usage

The template includes a sample component demonstrating various Tailwind features:

```jsx
function App() {
  return (
    <div className="min-h-screen bg-gray-100 flex items-center justify-center">
      <div className="bg-white p-8 rounded-lg shadow-lg">
        <h1 className="text-3xl font-bold text-gray-800 mb-4">
          Hello Tailwind!
        </h1>
        <p className="text-gray-600 mb-6">Your template is ready to use!</p>
        <button className="bg-blue-500 hover:bg-blue-600 text-white font-medium py-2 px-4 rounded transition-colors">
          Get Started
        </button>
      </div>
    </div>
  );
}
```

## 🆚 Why Tailwind v3?

Tailwind CSS v3 offers several advantages for production projects:

| Feature              | Benefit                                                       |
| -------------------- | ------------------------------------------------------------- |
| **Stability**        | Mature, well-tested codebase with extensive community support |
| **Plugin Ecosystem** | Large selection of official and community plugins             |
| **JIT Compiler**     | Just-in-time compilation for faster builds and smaller CSS    |
| **Arbitrary Values** | Use custom values like `w-[300px]` or `text-[#50d71e]`        |
| **Documentation**    | Comprehensive docs and tutorials                              |

## 🛠️ Customization

### Adding Custom Styles

Extend the theme in `tailwind.config.js`:

```javascript
/** @type {import('tailwindcss').Config} */
export default {
  content: ["./index.html", "./src/**/*.{js,ts,jsx,tsx}"],
  theme: {
    extend: {
      colors: {
        "custom-blue": "#1e40af",
        brand: {
          50: "#eff6ff",
          500: "#3b82f6",
          900: "#1e3a8a",
        },
      },
      fontFamily: {
        custom: ["Inter", "sans-serif"],
      },
      spacing: {
        18: "4.5rem",
        88: "22rem",
      },
    },
  },
  plugins: [],
};
```

### Adding Tailwind Plugins

Install popular Tailwind v3 plugins:

```bash
npm install -D @tailwindcss/forms @tailwindcss/typography @tailwindcss/aspect-ratio
```

```javascript
// tailwind.config.js
import forms from "@tailwindcss/forms";
import typography from "@tailwindcss/typography";
import aspectRatio from "@tailwindcss/aspect-ratio";

/** @type {import('tailwindcss').Config} */
export default {
  content: ["./index.html", "./src/**/*.{js,ts,jsx,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [forms, typography, aspectRatio],
};
```

### Using Custom Components

Create reusable components with `@apply`:

```css
/* src/index.css */
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
  .btn-primary {
    @apply bg-blue-500 hover:bg-blue-600 text-white font-medium py-2 px-4 rounded transition-colors;
  }

  .card {
    @apply bg-white p-6 rounded-lg shadow-lg;
  }
}
```

## 📚 Helpful Resources

- [Tailwind CSS v3 Documentation](https://tailwindcss.com/docs)
- [Tailwind CSS v3 Playground](https://play.tailwindcss.com/)
- [Vite Documentation](https://vitejs.dev/)
- [React Documentation](https://react.dev/)
- [Tailwind UI Components](https://tailwindui.com/)

## 🐛 Troubleshooting

### Styles Not Applying?

1. Check that classes are spelled correctly
2. Ensure `src/index.css` is imported in `main.jsx`
3. Verify the `@tailwind` directives are in your CSS file
4. Restart the dev server: `npm run dev`

### Purging Issues?

Make sure your `content` array in `tailwind.config.js` includes all files where you use Tailwind classes:

```javascript
content: [
  "./index.html",
  "./src/**/*.{js,ts,jsx,tsx}",
  "./components/**/*.{js,ts,jsx,tsx}",
],
```

### Need to Upgrade to Tailwind v4?

```bash
npm uninstall tailwindcss
npm install -D tailwindcss@next @tailwindcss/postcss
```

Then update your configs to use v4 syntax.

## 🤝 Contributing

Found an issue or want to improve the template? Pull requests are welcome!

## 📄 License

This template is available under the [MIT License](LICENSE).

---

**Happy coding!** 🎉

Start building beautiful UIs with Tailwind CSS v3 without the setup headaches.
