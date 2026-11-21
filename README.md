# 🎨 Dibuja y Adivina — Pictionary local para 2 jugadores

Juego de **dibujar y adivinar** para jugar entre dos personas pasando el mismo teléfono o tablet. Funciona completamente en el navegador, **sin servidores, sin cuentas y sin conexión a internet** una vez cargado.

Inspirado en la mecánica clásica de dibujar y adivinar por turnos: elegís una palabra de una categoría, dibujás contrarreloj, y la otra persona trata de adivinar en voz alta.

## ✨ Características

- 🖊️ Lienzo táctil con colores, grosor de trazo ajustable y goma de borrar
- ⏱️ Cronómetro configurable (45 / 60 / 90 / 120 segundos por turno)
- 🏆 Meta de puntos configurable (10 / 15 / 20 / 30 puntos para ganar)
- 📚 Más de 200 palabras en español repartidas en 4 categorías:
  - Personas, animales y lugares
  - Objetos
  - Acciones
  - Difícil
- 🔄 Pantalla de "pasale el teléfono" para que el otro jugador no vea la palabra antes de tiempo
- 📱 100% responsivo, pensado para celulares Android
- 🚫 Sin backend, sin base de datos, sin login — todo corre en el cliente

## 📂 Estructura del proyecto

```
.
├── index.html          # Estructura de las pantallas del juego
├── css/
│   └── style.css       # Estilos (tema papel/tiza)
├── js/
│   ├── words.js        # Banco de palabras por categoría
│   └── game.js         # Lógica del juego (estado, turnos, lienzo, cronómetro)
├── assets/              # (reservado para íconos o imágenes futuras)
├── .gitignore
├── LICENSE
└── README.md
```

## ▶️ Cómo jugarlo

### Opción 1 — Abrir el archivo directo
Descargá o cloná el repositorio y abrí `index.html` con cualquier navegador (Chrome en Android funciona perfecto).

### Opción 2 — GitHub Pages (jugarlo desde un link, sin instalar nada)
1. Subí este repositorio a tu cuenta de GitHub.
2. Andá a **Settings → Pages**.
3. En "Branch" elegí `main` y la carpeta `/root`, guardá.
4. GitHub te va a dar un link tipo `https://tu-usuario.github.io/tu-repo/` — abrilo desde el navegador del celular.

### Opción 3 — Clonarlo y servirlo localmente
```bash
git clone https://github.com/tu-usuario/tu-repo.git
cd tu-repo
python3 -m http.server 8080
# abrir http://localhost:8080 en el navegador
```

## 🕹️ Cómo se juega

1. En la pantalla inicial, cargá los nombres de los dos jugadores, elegí la meta de puntos, el tiempo por turno y las categorías activas.
2. Pasale el teléfono a quien le toca dibujar.
3. Quien dibuja ve la palabra (puede cambiarla si no le gusta) y arranca el cronómetro.
4. Dibuja en el lienzo sin usar letras, números ni gestos — la otra persona adivina en voz alta.
5. Si acierta, tocá **"¡Lo adivinó!"**; si se acaba el tiempo o se rinden, tocá **"Pasar palabra"**.
6. El turno pasa al otro jugador. Gana quien llegue primero a la meta de puntos.

## 🛠️ Personalizar

- **Agregar más palabras**: editá `js/words.js` y sumá strings al array `words` de la categoría que quieras.
- **Cambiar colores del lienzo**: editá el bloque `.tools .swatch` en `index.html` (atributo `data-color`) y los `style="background:..."`.
- **Cambiar la paleta visual**: todas las variables de color están en `:root` al principio de `css/style.css`.

## 📄 Licencia

Este proyecto se distribuye bajo licencia MIT — ver [LICENSE](LICENSE). Es un juego propio de dibujar-y-adivinar, no afiliado ni asociado a Mattel, Hasbro, Etermax ni a ninguna marca comercial de juegos de mesa.
