# YOU SEEM PRETTY SAD

**Videojuego 3D narrativo con toques de terror psicológico, hecho en Unity 6 y jugable en el navegador (WebGL).** Proyecto final de Game Development.

- **Jugar / página del juego:** https://denistae.github.io/YouSeemPrettySad/

## Historia

**Arivelle** siente que su habitación se ha vuelto más pequeña: hay demasiadas cosas que no consigue ordenar, y no son solo objetos. Una noche abre su diario y cada recuerdo se convierte en un capítulo jugable. Su reflejo, **El Eco**, la acompaña (y la persigue) en todos.

| Capítulo | Nombre | Género | Qué se hace |
|---|---|---|---|
| Prólogo / epílogo | La habitación | Exploración | Explorar el cuarto, abrir el diario y encontrar notas. |
| 1 | LESS | Tablero de casillas | Carrera contra El Eco sobre un tablero flotante con dados, bifurcaciones, portales y un minijuego de rompecabezas de 40 s. |
| 2 | THE CURE | Exploración y sigilo | Atravesar un hospital con linterna, ahuyentar fantasmas y abrir puertas. |
| 3 | STUPID SONG | Corredor infinito | Correr por una Nueva York nocturna en tres carriles: saltar, agacharse y cambiar de carril. |
| 4 | CIGARETTE SMOKE | Carrera de autos | Pista con forma de corazón: esquivar obstáculos, derrapar y llegar a la meta. |

## Controles

| Contexto | Teclas |
|---|---|
| Exploración (prólogo, nivel 2) | `WASD` mover · mouse mirar · `E` interactuar · `F` linterna · `Shift` correr |
| Nivel 1 (tablero) | clic en el dado o `Espacio` · `←` `→` + `Enter` elegir camino · `V` mapa |
| Nivel 3 (corredor) | `A`/`D` carril · `Espacio` saltar · `Ctrl` agacharse |
| Nivel 4 (carrera) | `W` acelerar · `S` frenar · `A`/`D` girar · `Espacio` derrapar |
| Siempre | `J` registro de recuerdos · `Esc` pausa y ajustes |

## Mecánicas principales

1. **Tres vidas por capítulo.** Al perderlas, el capítulo se reinicia.
2. **Registro de recuerdos.** Las notas halladas se guardan y completan la historia.
3. **El Eco como rival.** Cambia de comportamiento en cada nivel.
4. **Minijuego de rompecabezas** con límite de tiempo en las casillas de recuerdo.

El juego es **100 % procedural**: modelos, escenarios, texturas y efectos se generan por código C#.

## Estructura del repositorio

```
.
├── index.html     Página del juego: historia, niveles, personajes, galería, tráiler y autores
├── juego/         Compilación WebGL (Unity 6) y su cargador
├── img/           Capturas e ilustraciones de los escenarios
├── trailer/       Tráiler del juego (MP4, 61 s)
└── docs/          Documento de diseño actualizado y evidencias del Hito 6 (PDF)
```

## Cómo se exportó a la web

1. Unity 6 (6000.6.1f1) con URP, plataforma **WebGL**.
2. Menú `YSPS ▸ Exportar Web (WebGL)`: compresión **Gzip** con `decompressionFallback` (GitHub Pages no envía la cabecera `Content-Encoding` de los archivos comprimidos). Durante la exportación se apagan las sombras de luces adicionales, que WebGL2 no admite con este pipeline.
3. La página crea el reproductor solo al pulsar **START**, para cargar rápido.

## Probar en local

```bash
python -m http.server 8000
# abrir http://localhost:8000/
```

## Autores

- **Denis Medrano Carrasco** — [github.com/DenisTae](https://github.com/DenisTae)
- **Ariana Patzi Gonzales** — [github.com/aritozs673-maker](https://github.com/aritozs673-maker)

Tecnologías: **Unity 6, C#, URP, WebGL, HTML, CSS, JavaScript y GitHub Pages**.
