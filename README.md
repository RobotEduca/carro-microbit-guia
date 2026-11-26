# Carro controlado por radio con micro:bit · Guía interactiva

Aplicación web interactiva autocontenida (`index.html`, sin paso de compilación ni dependencias externas) pensada para estudiantes de primaria (9–12 años) y docentes.

## Qué incluye

- **10 piezas y herramientas** del manual con tapete de trabajo interactivo en SVG y lista de chequeo sincronizada.
- **Placas clicables** (puente H L298N y placa de expansión de la micro:bit con columnas `0–8`).
- **5 pasos de armado** con comprobación obligatoria que desbloquea el siguiente paso, estrellas, confeti y **Modo docente** (desbloquea todos los pasos y guarda notas de clase).
- **11 conexiones exactas** con fichas de color accesibles, diagrama SVG resaltable y **revisión de 10 puntos** antes de encender.
- **Programación MakeCode** con enlaces directos al programa del control, del carro y del código original opcional (`GRUPO 60`, `UMBRAL 500`, parada a `400 ms`).
- **Simulador físico en vivo** con matrices LED 5×5, pines `P0/P1/P2/P8`, prioridad de botones sobre inclinación, ajuste de `UMBRAL`, apagado del control para probar la parada de seguridad a los 400 ms, control por teclado/táctil y consola en tiempo real.
- **14 pruebas finales** (6 del control + 8 del carro) con insignia desbloqueable y **diploma imprimible** personalizable.
- **Solución de problemas** (7 síntomas), **glosario emergente** (7 términos técnicos), espacios `<Foto>` para las fotos del manual y **modo de impresión**.

---

## Uso local (sin instalar nada)

1. Abre la carpeta del proyecto.
2. Haz doble clic en `index.html` para abrirlo directamente en Chrome, Edge o Firefox.
3. El progreso de cada estudiante se guarda automáticamente en `localStorage` del navegador.

---

## Despliegue en Vercel (en menos de 1 minuto)

### Opción A · Desde GitHub (recomendada)
1. Sube esta carpeta (`index.html` y `README.md`) a un repositorio en GitHub.
2. Entra a [vercel.com](https://vercel.com) e inicia sesión.
3. Haz clic en **Add New → Project** y selecciona tu repositorio.
4. Deja la configuración por defecto (**Framework Preset: Other**, sin comando de build, directorio raíz `./`).
5. Haz clic en **Deploy**. En pocos segundos tendrás la URL pública lista para el salón.

### Opción B · Con Vercel CLI
```bash
npm i -g vercel
vercel
```
Sigue las preguntas en pantalla (acepta los valores por defecto) y para producción ejecuta:
```bash
vercel --prod
```

---

## Cómo agregar las fotos reales del manual

En `index.html` hay cinco bloques `<foto-manual data-foto="...">` (`paso-1`, `paso-2`, `paso-3`, `paso-5` y `cableado-completo`). Para colocar las fotos reales:

1. Crea una carpeta `fotos/` junto a `index.html` y guarda tus imágenes (`paso-1.jpg`, `paso-2.jpg`, etc.).
2. Dentro de cada etiqueta `<foto-manual>`, agrega una etiqueta `<img>`, por ejemplo:

```html
<foto-manual data-foto="paso-1">
  <img src="fotos/paso-1.jpg" alt="Motorreductores y rueda loca montados en el chasis" style="max-width:100%; border-radius:12px;" />
</foto-manual>
```
