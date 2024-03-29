# Coderhouse SASS Framework

Creación de framework propio con SASS

## Comandos

```sh
npm install   # Instala todas las dependencias del proyecto

npm run dev   # Inicia servidor de desarrollo con `Hot Reloading`
npm run build # Crea una version minificada lista para produccion en la carperta `dist/`
```

## Variables `CSS` disponibles

```scss
:root {
  // FONT
  --rr-coder-font-primary: Inter var, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
  --rr-coder-font-secondary: ui-serif, Georgia, Cambria, "Times New Roman", Times, serif;

  --rr-coder-font-size-base: 16px;
  --rr-coder-font-weight-base: 400;
  --rr-coder-line-height-base: 1.5;

  // COLORS
  --rr-coder-body-bg-color: #f1f5f9
  --rr-coder-body-text-color: #64748b;
  --rr-coder-heading-text-color: #334155;

  --rr-coder-color-primary: #3b82f6;
  --rr-coder-color-primary-hover: #60a5fa;
  --rr-coder-color-primary-contrast: #eff6ff;

  --rr-coder-color-secondary: #64748b;
  --rr-coder-color-secondary-hover: #94a3b8;
  --rr-coder-color-secondary-contrast: #f8fafc;

  --rr-coder-color-focus: #94a3b8;

  --rr-coder-shadow-color: 51 65 85;

  // HEADER
  --rr-coder-header-bg-color: #f8fafc;
  --rr-coder-header-border-color: #e2e8f0;

  // HERO
  --rr-coder-hero-text-color: #f1f5f9;
  --rr-coder-hero-gradient-start: #334155;
  --rr-coder-hero-gradient-end: #0f172a;

  // FOOTER
  --rr-coder-footer-bg-color: #e2e8f0;
  --rr-coder-footer-text-color: #64748b;

  // ACCORDIONS
  --rr-coder-accordion-title-color: #475569;
  --rr-coder-accordion-title-bg: #f8fafc;
  --rr-coder-accordion-title-hover-bg: #f1f5f9;
  --rr-coder-accordion-title-border: #e2e8f0;
  --rr-coder-accordion-content-bg: #FFFFFF;

  // BUTTONS
  --rr-coder-btn-radius: 8px;

  // CARDS
  --rr-coder-card-bg: #FFFFFF;
  --rr-coder-card-radius: 12px;
  --rr-coder-card-border: #e2e8f0;

  // INPUTS
  --rr-coder-input-bg-color: #FFFFFF;
  --rr-coder-input-text-color: #64748b;
  --rr-coder-input-border-color: #cbd5e1;
  --rr-coder-input-focus-border-color: #94a3b8;
  --rr-coder-input-invalid-color: #f87171;

  // SELECT
  --rr-coder-select-bg-color: #f8fafc;
  --rr-coder-select-hover-color: #FFFFFF;
  --rr-coder-select-text-color: #64748b;
  --rr-coder-select-border-color: #94a3b8;
  --rr-coder-select-focus-color: #64748b;

  // UTILS
  --rr-coder-chevron: url("data:image/svg+xml, <svg xmlns='http://www.w3.org/2000/svg' width='24' height='24' viewBox='0 0 24 24' fill='none' stroke='rgb(100, 116, 139)' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'><polyline points='6 9 12 15 18 9'></polyline></svg>");
}
```

> ⚠️ El prefijo **`coder`** usado en todas las variables `CSS` puede ser cambiado facilmente sobreescribiendo la variable global SCSS **`$prefix`**


## Clases `utiles` disponibles

```html
<!-- CONTENEDORES -->
<div class="container"></div>
<div class="flex-container"></div>

<!-- APLICA ESTILOS CON TRANSICIONES A TODOS LOS HIJOS -->
<body class="animate-all"></body>

<!-- `margin` EN TODAS LAS DIRECCIONES DEL `0` AL `16` -->
<div class="m-0"></div>
<div class="mt-8"></div>
<div class="my-4"></div>
<div class="mx-auto"></div>

<!-- `padding` EN TODAS LAS DIRECCIONES DEL `0` AL `16` -->
<div class="p-0"></div>
<div class="pt-8"></div>
<div class="py-4"></div>
<div class="px-auto"></div>
```


## `Mixins` utiles disponibles

```SCSS
// GENERA UNA VARIACION DE COLOR PARA BOTONES
@include btnColorVariation($class, $color, $color-light, $color-contrast);


// GENERA UN SELECTOR PADRE CON EL ATRIBUTO `data-theme`
@include theme($theme) {
  // ...
}


// GENERA UN MEDIA QUERY CON EL BREAKPOINT SELECCIONADO
@include break-up($breakpoint) {
  // ...
}

// ATAJO O ALIAS PARA `breakup(sm)`
@include sm() {
  // ...
}
// ATAJO O ALIAS PARA `breakup(md)`
@include md() {
  // ...
}
// ATAJO O ALIAS PARA `breakup(lg)`
@include lg() {
  // ...
}
// ATAJO O ALIAS PARA `breakup(xl)`
@include xl() {
  // ...
}


// GENERA CLASES UTILITARIAS PARA ESPACIADOS
@include generate-spacing($prop, $short);
```

## `Temas` disponibles


| Light `default`  | RR-Coder `dark` |
| -------------- | -------------- |
| [![Light Theme](./src/assets/screenshot-light.png)](./src/assets/screenshot-light.png) | [![RR-Coder Theme](./src/assets/screenshot-dark.png)](./src/assets/screenshot-dark.png) |
