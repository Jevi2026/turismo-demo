# Ruta Lenga · Demo de landing turística

Página de presentación para un destino turístico (Patagonia austral, entre Chile y Argentina). Es una **demo para mostrar a clientes**: solo presentación, sin backend, sin reservas, sin formularios y sin base de datos.

"Ruta Lenga" es una marca inventada. No representa a ninguna agencia ni oficina de turismo real.

## Qué incluye

- Portada a pantalla completa con foto, titular y botón principal (azul cobalto).
- Seis experiencias en tarjetas.
- Tres bloques de texto + foto.
- Itinerario de ejemplo de 7 días.
- "Cuándo ir": las cuatro estaciones.
- Galería de fotos.
- Contacto con enlace a WhatsApp y correo (son enlaces normales, no guardan nada).
- Pie de página con aviso de que es una demo.

Funciona en celular (probado a 390 px de ancho, sin scroll horizontal) y respeta la opción del sistema "reducir movimiento".

## Cómo abrirla

No necesita instalar nada. Doble clic en `index.html` y se abre en el navegador.

Para que las fotos y la fuente carguen hace falta internet, porque vienen de Unsplash y Google Fonts. Si una foto no carga, queda un fondo gris oscuro en su lugar.

## Estructura

```
turismo-demo/
├── index.html   ← toda la página en un solo archivo
└── README.md
```

Dentro de `index.html`:

- `<style>` (arriba, en el `<head>`): colores, tipografía y diseño.
- El contenido: textos, fotos y enlaces.
- `<script>` (al final): menú del celular, barra que se esmerila al bajar y animaciones suaves.

Va todo en un solo archivo para que se vea bien en cualquier lado: al abrirlo con doble clic, en vistas previas que solo leen el HTML o si se lo mandas a alguien suelto por WhatsApp o correo.

## Cómo adaptarla para un cliente

Casi todo se cambia en `index.html`:

1. **Nombre de la marca:** busca `Ruta Lenga` y reemplázalo (aparece en el `<title>`, la barra superior y el pie).
2. **WhatsApp:** busca `wa.me/50400000000` (aparece 2 veces) y pon el número real con código de país, sin `+` ni espacios. Ejemplo para Honduras: `wa.me/50499998888`. El texto después de `?text=` es el mensaje que llega prellenado.
3. **Correo:** busca `hola@ejemplo.com` (2 veces: el enlace `mailto:` y el texto del botón).
4. **Textos:** titular, experiencias, itinerario y temporadas son texto normal dentro del HTML.
5. **Fotos:** cada `<img>` usa un enlace de Unsplash. Para cambiarla, pega el enlace de la nueva foto en `src` y actualiza el `alt` (descripción de la foto). Si el cliente tiene fotos propias, crea una carpeta `img/` y usa `src="img/mi-foto.jpg"`.
6. **Colores:** al inicio del bloque `<style>`, dentro de `:root`, están las variables (`--onyx`, `--graphite`, `--cobalt`, etc.). Cambiar `--cobalt` cambia el color del botón principal.
7. **Aviso de demo:** cuando sea el sitio real del cliente, cambia o quita el párrafo `class="disclaimer"` del pie.

Regla del diseño: solo **un** botón azul relleno por página (el principal). Los demás botones son de contorno.

Si vas a cambiar de destino, revisa que cada foto muestre de verdad lo que dice su texto, y no inventes reseñas, precios ni calificaciones.

## Cómo publicarla gratis

### Opción 1: GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `turismo-demo`) y sube el contenido de esta carpeta:
   ```bash
   git init
   git add .
   git commit -m "Demo landing turismo"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/turismo-demo.git
   git push -u origin main
   ```
2. En GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)`, y **Save**.
3. En uno o dos minutos queda en `https://TU_USUARIO.github.io/turismo-demo/`.

### Opción 2: Netlify Drop

Entra a <https://app.netlify.com/drop> y arrastra la carpeta `turismo-demo`. Te da un enlace público al instante. Sin cuenta el enlace es temporal; con una cuenta gratis queda guardado.

## Créditos

Fotografías de [Unsplash](https://unsplash.com), cargadas directamente desde su servidor. Tipografía Inter (Google Fonts). Estilo visual basado en una referencia de diseño oscuro con un solo color de acción.
