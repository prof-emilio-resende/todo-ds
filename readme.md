# 1: Criar arquivos

-   mkdir htmlApp
-   design.html
-   design.css

# 2: Iniciar projeto npm

```node
npm init
```

> (continuar até finalizar CLI)

# 3: Configurar tailwindcss

```node
npm install -D tailwindcss
npx tailwindcss init

```

```typescript
// tailwind.config.js
/** @type {import('tailwindcss').Config} */
module.exports = {
    content: ["./src/**/*.{html,js}"],
    theme: {
        extend: {},
    },
    plugins: [],
};
```

```css
/* src/design.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

# 4: Iniciar tailwindcss para gerar css continuamente

```node
htmlApp npx tailwindcss -i ./src/design.css -o ./design.css --watch
```

# 5: Implementação dos principais componentes

## Título principal

```html
<h1 class="text-3xl">Título 1</h1>
<h2 class="text-2xl">Título 2</h2>
<h3 class="text-1xl">Título 3</h3>
```

## Busque o template para o campo de input em:

[shadcn](https://ui.shadcn.com/docs/components/input)

```html
<input
    type="text"
    class="flex h-10 w-full rounded-md border border-input bg-background px-3 py-2 text-base ring-offset-background file:border-0 file:bg-transparent file:text-sm file:font-medium file:text-foreground placeholder:text-muted-foreground focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:cursor-not-allowed disabled:opacity-50 md:text-sm"
/>
```

## Busque o template para o campo de text em:
[shadcn](https://ui.shadcn.com/docs/components/textarea)
```html
<textarea
  class="flex min-h-[80px] w-full rounded-md border border-input bg-background px-3 py-2 text-base ring-offset-background placeholder:text-muted-foreground focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:cursor-not-allowed disabled:opacity-50 md:text-sm" />
```

## Busque o template para o componente Button em:

[shadcn](https://ui.shadcn.com/docs/components/button)

```html
<button
    type="button"
    class="inline-flex items-center justify-center gap-2 whitespace-nowrap rounded-md text-sm font-medium ring-offset-background transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 [&_svg]:pointer-events-none [&_svg]:size-4 [&_svg]:shrink-0 bg-slate-700 text-slate-300 hover:bg-slate-700/90 h-10 px-4 py-2"
>
    primary
</button>
```

Para ter variações, basta aplicar direrentes classes:

```css
bg-red-700 text-slate-100 hover:bg-red-700/90
bg-blue-700 text-slate-100 hover:bg-blue-700/90
```

# 6: Cards

## Busque o template para o componente card (container) em:
[shadcn](https://ui.shadcn.com/docs/components/card)

## E busque o template para o componente badge em:
[shadcn](https://ui.shadcn.com/docs/components/badge)

## O ícone da lixeira pode ser encontrado em:
[radix](https://www.radix-ui.com/icons)

```html
<div class="rounded-lg border bg-card text-card-foreground shadow-sm w-8/12">
    <div class="flex flex-col space-y-1.5 p-5">
        <div class="flex flex-row justify-between align-middle">
            <h1>Atividade 1</h1>
            <svg
                width="24"
                height="24"
                viewBox="0 0 16 16"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
            >
                <path
                    d="M5.5 1C5.22386 1 5 1.22386 5 1.5C5 1.77614 5.22386 2 5.5 2H9.5C9.77614 2 10 1.77614 10 1.5C10 1.22386 9.77614 1 9.5 1H5.5ZM3 3.5C3 3.22386 3.22386 3 3.5 3H5H10H11.5C11.7761 3 12 3.22386 12 3.5C12 3.77614 11.7761 4 11.5 4H11V12C11 12.5523 10.5523 13 10 13H5C4.44772 13 4 12.5523 4 12V4L3.5 4C3.22386 4 3 3.77614 3 3.5ZM5 4H10V12H5V4Z"
                    fill="currentColor"
                    fill-rule="evenodd"
                    clip-rule="evenodd"
                ></path>
            </svg>
        </div>
        <div>
            <p class="text-slate-500 font-medium">Descrição simples</p>
        </div>
        <div class="flex flex-row justify-end">
            <div
                class="inline-flex items-center rounded-md border px-2.5 py-0.5 text-xs font-light transition-colors focus:outline-none focus:ring-2 focus:ring-ring focus:ring-offset-2 bg-green-500 text-whiteh"
            >
                Finalizado
            </div>
        </div>
    </div>
</div>
```
