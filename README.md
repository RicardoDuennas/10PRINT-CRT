# 10PRINT CRT
Prototipo de visualización generativa inspirado en el algoritmo clásico 10PRINT, con simulación de pantalla CRT y controles interactivos. Desarrollado para exploración visual en el curso Automatización del pregrado Creación Digital UdeA (HTML + iframe). Desarrollado con IA.
Herramienta simple en HTML, CSS y JavaScript puro para generar patrones diagonales dinámicos con estética de terminal retro.

## Funcionalidad
Generación procedural de patrón tipo 10PRINT
Diagonales perfectas a 45° sin espacios
Simulación de persistencia de fósforo (CRT)
Animación continua con variación aleatoria
Control en tiempo real de parámetros visuales
Botón de encendido / pausa (simulación de apagado)
Interfaz lateral separada del canvas
Integración mediante iframe

## Estructura
10print.html: archivo principal del generador

## Uso
### 1. Abrir herramienta

Abrir directamente en navegador o servir desde entorno local.

### 2. Integrar con iframe
<iframe 
  src="10print.html" 
  width="800" 
  height="500" 
  style="border:none;">
</iframe>

## Controles

### Botón Play / Pausa
Simula encendido y apagado de pantalla
Al pausar: elimina persistencia (pantalla limpia)
Al reanudar: restaura estado anterior

### Persistencia
Controla el efecto de “ghosting” CRT
0 = sin persistencia
Máximo = arrastre visual fuerte

### Tamaño celda
Define la resolución de la celda

### Velocidad
Controla el intervalo de actualización

### Cambio aleatorio
Probabilidad de variación por celda

### Grosor de línea
Define el peso visual de las diagonales

### Glow
Simula el brillo del fósforo CRT

## Características técnicas

Sin dependencias externas (100% vanilla JS)
Canvas 2D para renderizado eficiente
Grid discreto con celdas cuadradas perfectas
Uso de getBoundingClientRect() para compatibilidad en iframe
Encapsulamiento mediante IIFE (sin contaminación global)
Render basado en setInterval
Simulación de persistencia mediante alpha compositing

## Referencia conceptual

Basado en el programa clásico:

10 PRINT CHR$(205.5+RND(1)); : GOTO 10

Popularizado en sistemas como Commodore 64, donde generaba patrones laberínticos mediante caracteres diagonales.
