# Registro de cambios — Proyecto Mort (Para Tammie)

## 1. Tarjetas bloqueadas (index.html)

### CSS — Estilo de tarjetas bloqueadas
- Se añadió la clase `.card-locked` que aplica:
  - **Blur + grayscale + brightness** a las imágenes de las tarjetas (`filter:blur(14px) grayscale(0.8) brightness(0.45)`)
  - **Blur + opacidad** al fallback de color (`filter:blur(10px);opacity:0.6`)
  - **Icono de candado 🔒** centrado sobre la imagen (`::after` con `content:'🔒'`)
- Las tarjetas bloqueadas no muestran sus fotos reales ni sus títulos reales para evitar spoilers.

### JS — Bloqueo automático de tarjetas
- Script que detecta todas las tarjetas con `href="#"` y `onclick` que contenga `alert`.
- A cada tarjeta bloqueada le aplica:
  - Clase `.card-locked`
  - **Sin alert** — se eliminó el `alert('Estamos trabajando en ello ❤️')`, ahora solo `return false`
  - **Título** → "Próximamente"
  - **Descripción** → "Algo especial se está preparando para ti."
  - **Arrow** → "Próximamente →"
  - **Alt de imagen** → "Próximamente"
- Las tarjetas con páginas reales (Inicio, Cumpleaños, San Valentín) no se ven afectadas.

---

## 2. Menú de filtros (index.html)

### Filtros deshabilitados
- Solo el botón **"Todas"** queda funcional con `onclick="filterCards('all',this)"`.
- Los demás filtros (Principal, Amor, Recuerdos, Especiales, Celebración) se marcaron como **"Próximamente"**:
  - Se eliminó su `onclick`.
  - Se añadió la clase `.filter-coming-soon` con `opacity:0.45`, `cursor:not-allowed`, `pointer-events:none`.
  - Su texto ahora dice "Principal · Próximamente", "Amor · Próximamente", etc.

---

## 3. Carta de inicio (inicioM.html)

### Contenido
- **Eliminado:** Referencias a la lámpara de rosa/zorro y la agenda (regalos que no se dieron).
- **Eliminado:** Quote sobre "jugar con fuego".
- **Nuevo título:** "Una segunda oportunidad" con ornamento decorativo dorado.
- **Nuevo subtítulo:** "y la promesa de no soltarla nunca más."
- **Mensaje 1:** Personas que marcan tu vida, cuyo regreso hace encajar el mundo (con letra capital dorada).
- **Mensaje 2:** La segunda oportunidad que ella dio, su valentía de decidir que lo de ustedes merecía otra historia.
- **Mensaje 3:** El anillo de promesa — la promesa más sincera, estar para quedarse.
- **Mensaje 4:** Felicidad de estar juntos nuevamente, recuperar el tiempo, los 3 años juntos (con nota: "aunque tú digas que son dos").
- **Quote nueva:** "A veces el amor no se trata de encontrar a la persona correcta, sino de que ella te encuentre de nuevo, en el momento exacto, y decida quedarse." con firma.
- **Footer:** "Con todo mi amor, hoy y siempre."

### Diseño mejorado
- **Ornamento decorativo** bajo el título (líneas doradas con ✦).
- **Letra capital** dorada en el primer mensaje (`.message-first-letter::first-letter`).
- **Quote con comillas tipográficas** reales (""), bordes laterales dorados y firma (`.quote-author`).
- **Subtítulo en cursiva** para más elegancia.
- **Énfasis con `<em>`** en color rosa para frases clave.
- **Espaciado y letter-spacing** refinados en los mensajes.

---

## 4. Botones de regreso (referencias rotas)

### inicioM.html
- Botón "Volver al menú": `menu_adi_v2.html` → `index.html`

### birthdayM/Cumpleaños.html
- Botón "Regresar": `../menu_adi_v2.html` → `../index.html`

### Nota
- El archivo `menu_adi_v2.html` fue eliminado. Todas las referencias se redirigen a `index.html`.
- No había archivos con "adi" en el nombre por renombrar (ya fue eliminado).

---

## 5. Archivos afectados

| Archivo | Cambios |
|---|---|
| `index.html` | CSS tarjetas bloqueadas, JS bloqueo automático, menú de filtros deshabilitado, sin alert |
| `inicioM.html` | Carta reescrita (anillo de promesa, segunda oportunidad, 3 años), diseño mejorado, botón de regreso corregido |
| `birthdayM/Cumpleaños.html` | Botón de regreso corregido |
