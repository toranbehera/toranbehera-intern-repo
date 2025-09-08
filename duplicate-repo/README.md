Follow the Tailwind docs to set up Tailwind CSS for a Vite project: https://tailwindcss.com/docs/installation/using-vite

1. Create a Vite project by running `npm create vite@latest your-project`. Select your framework and compiler of choice, along with whether you want to work with TypeScript or JavaScript.
2. Navigate to your project's folder by running `cd your-project`
3. Install tailwindcss and @tailwindcss/vite via running `npm install tailwindcss @tailwindcss/vite`
4. Open the vite.config.ts file in your project folder and add `import tailwindcss from '@tailwindcss/vite'` and `tailwindcss()` as shown below
![[Pasted image 20250908103408.png]]
5. Add `@import "tailwindcss"` to the global CSS file that imports Tailwind CSS. In the case of a Vite + React default project template, that is the index.css file, although importing in the App.css file also works, as both apply CSS styles globally to all components.
![[Pasted image 20250908103555.png]]
6. Start your build process by running `npm run dev`. 
7. Start using Tailwind in the HTML of your components. Default Tailwind styles should automatically apply to certain elements like input and button.
![[Pasted image 20250908104416.png]]
