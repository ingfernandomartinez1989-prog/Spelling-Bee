# 🐝 Spelling Bee — práctica de 45 palabras en inglés

App web estática (un solo `index.html`) para que un niño de 10 años practique **escuchar** y
**deletrear** 45 palabras en inglés. Sin frameworks, sin backend, sin build step.

## Qué incluye

- **🎤 Practicar deletreo** (modo principal): la app dice la palabra en voz alta (`en-US`), el niño la
  escribe y recibe feedback inmediato. Si falla, muestra la palabra deletreada letra por letra.
- **Dos niveles**, elegibles en Inicio y cambiables a mitad de ronda con el botón de arriba:
  - `👀 Fácil` (aprender) — la palabra se ve en pantalla y se escucha. **Sin escribir ni
    calificación**: sólo mirar, oír y avanzar.
  - `🎤 Examen` (evaluarse) — la palabra no se ve; el niño la escribe y la app la califica,
    con marcador y racha (como en el concurso real).
- **🔁 Repetir palabra** y **🔤 Deletrear letra por letra** (formato real de spelling bee):
  mientras la voz dicta cada letra, esa letra **se ilumina** en la palabra.
- **🔤 Panel de abecedario** al lado de la página (debajo, en celular): cada letra A–Z muestra
  **debajo cómo se pronuncia** escrito a la española (`A → ei`, `W → dábliu`). Tócala para
  escucharla, o usa **🎵 Decir el abecedario** para oír A→Z resaltando cada letra
  (**⏹ Parar** lo detiene).
- **📖 Repaso libre**: las 45 palabras visibles, con audio individual y buscador. Sin examen.
- Marcador de ✅ aciertos, ❌ fallos, 🔥 racha y 🏆 mejor racha.
- Resumen final con las palabras falladas y la opción de **repasar solo esas**.
- Responsive, botones grandes, tipografía grande.

## Cómo usarlo

Doble clic en `index.html` (funciona desde `file://`) o abrir la URL de GitHub Pages.
El audio siempre se activa con un clic — los navegadores bloquean el audio automático.

Recomendado: **Chrome** o **Edge**. Si el navegador no soporta la Web Speech API, la app avisa y
sigue funcionando como práctica escrita. En iPhone/iPad, el equipo no debe estar en modo silencio.

## Publicar en GitHub Pages (sin instalar nada)

1. Entra a <https://github.com/new>. Nombre del repositorio: `spelling-bee`.
   Visibilidad: **Public**. Clic en **Create repository**.
2. En la página del repo vacío, clic en el enlace **uploading an existing file**.
3. Arrastra `index.html` (y este `README.md`) y clic en **Commit changes**.
4. Ve a **Settings → Pages**. En *Source* elige **Deploy from a branch**,
   Branch: **main**, carpeta **/ (root)**, y clic en **Save**.
5. Espera ~1 minuto y recarga. La URL pública queda así:
   `https://TU-USUARIO.github.io/spelling-bee/`

## Cómo agregar o quitar palabras

Edita **solo** el arreglo `PALABRAS_ORIGEN` al inicio del `<script>` en `index.html`
(una palabra por línea, entre comillas y separadas por comas). Todo lo demás se ajusta solo:
contadores, barra de progreso y repaso libre.

Desde GitHub: abre `index.html` → ícono ✏️ (*Edit this file*) → edita el arreglo →
**Commit changes**. GitHub Pages se actualiza automáticamente.

> Nota: la lista original entregada trae 46 entradas porque `congratulations` aparece dos veces.
> El arreglo se dejó tal cual, y la app elimina el duplicado al cargar → **45 palabras únicas**.
