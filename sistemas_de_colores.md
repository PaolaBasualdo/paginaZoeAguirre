




















































































































































# 🎨 Guía Sencilla de Sistemas de Colores en CSS
### *Cómo entiende y pinta los colores una computadora*

---

## 💡 ¿Por qué hay distintas formas de escribir un color en CSS?

Cuando diseñamos una página web, podemos decirle al navegador qué color usar de varias maneras. Algunas son súper fáciles de recordar y otras nos dan un control total sobre la transparencia o el brillo.

---

## 1. Nombres Palabras Clave (Named Colors)

Es la forma más simple. Escribimos el nombre del color directamente en inglés.

```css
p {
  color: red;              /* Rojo */
  background-color: blue;  /* Azul */
}
```

- **Ventajas**: Muy fácil de entender y recordar.
- **Desventajas**: Solo hay unos 140 colores oficiales (`red`, `blue`, `green`, `black`, `white`, `yellow`, `purple`, etc.). No podés elegir un tono exacto.

---

## 2. Sistema Hexadecimal (HEX)

Es el formato **más usado en diseño web**. Comienza siempre con un signo de numeral `#` seguido de 6 caracteres (números y letras).

Ejemplo: `#ff0000` (Rojo puro)

### ¿Cómo funciona?
El código de 6 dígitos se divide en **3 parejas**:

```text
 #  FF   00   00
    R    G    B
  Rojo Verde Azul
```

- Las primeras dos letras/números son para el **Rojo (Red)**.
- Las del medio para el **Verde (Green)**.
- Las últimas dos para el **Azul (Blue)**.

### ¿Qué significan los números y letras?
Utiliza caracteres del **`0` al `9`** y de la **`A` a la `F`**:
- **`0`** significa *"nada de color"*.
- **`F`** (o `FF`) significa *"el máximo de color"*.

### Ejemplos Fáciles de Recordar:
- `#000000` ➔ **Negro** (Nada de luz).
- `#ffffff` ➔ **Blanco** (Todas las luces al máximo).
- `#ff0000` ➔ **Rojo puro** (Máximo rojo, cero verde, cero azul).
- `#00ff00` ➔ **Verde puro**.
- `#0000ff` ➔ **Azul puro**.

> 💡 **Tip corto**: Si los 6 caracteres son idénticos en parejas, se puede abreviar: `#ffffff` se puede escribir como `#fff`.

---

## 3. Sistema RGB (Red, Green, Blue)

Funciona igual que el sistema Hexadecimal pero usa **números normales** del **0 al 255** para mezclar luces de Rojo, Verde y Azul.

```css
h1 {
  color: rgb(255, 0, 0);   /* Rojo puro */
  color: rgb(0, 255, 0);   /* Verde puro */
  color: rgb(0, 0, 255);   /* Azul puro */
  color: rgb(0, 0, 0);     /* Negro */
  color: rgb(255, 255, 255);/* Blanco */
}
```

- **0** = Sin color.
- **255** = Máxima intensidad.

---

## 4. Sistema RGBA (Con Transparencia)

Es una variante de RGB que agrega una **cuarta letra**: la **A** de **Alpha** (Transparencia u opacidad).

```css
div {
  /* Fondo rojo con 50% de transparencia */
  background-color: rgba(255, 0, 0, 0.5);
}
```

El valor Alpha va de **`0` a `1`**:
- `0` ➔ Totalmente invisible (100% transparente).
- `0.5` ➔ Semitransparente (50% transparente).
- `1` ➔ Totalmente sólido (0% transparente).

> 💡 **Útil para**: Crear vidrio esmerilado, fondos semitransparentes, sombreados suaves y menús flotantes.

---

## 5. Sistema HSL (Hue, Saturation, Lightness)

A muchos diseñadores les encanta HSL porque es **más intuitivo para los humanos** que mezclar luces RGB.

Sustituye la mezcla de colores por tres conceptos:

```css
button {
  color: hsl(217, 91%, 60%);
}
```

1. **H (Hue / Tono)**: Es la posición del color en un **círculo cromático de 0° a 360°**.
   - `0°` = Rojo
   - `120°` = Verde
   - `240°` = Azul
2. **S (Saturation / Saturación)**: Qué tan "vivo" o "apagado" es el color.
   - `0%` = Gris sin vida.
   - `100%` = Color súper vívido e intenso.
3. **L (Lightness / Luminosidad)**: Qué tan claro u oscuro es.
   - `0%` = Negro absoluto.
   - `50%` = Color normal.
   - `100%` = Blanco absoluto.

> 💡 **Ventaja en clase**: Si tenés un color Azul en HSL y querés hacer una versión más oscura para cuando el usuario pase el mouse (`:hover`), ¡solo tenés que bajarle el porcentaje de Luminosidad!

---

## 📊 Tabla Comparativa Resumen para Estudiantes

| Sistema | Sintaxis / Ejemplo | ¿Cuándo conviene usarlo? |
| :--- | :--- | :--- |
| **Nombres** | `color: red;` | Para hacer pruebas rápidas en clase. |
| **HEX** | `color: #2563eb;` | El estándar más común en la industria. |
| **RGB** | `color: rgb(37, 99, 235);` | Cuando querés mezclar canales numéricos. |
| **RGBA** | `color: rgba(0, 0, 0, 0.5);` | Cuando necesitás transparencia/opacidad. |
| **HSL** | `color: hsl(217, 91%, 60%);` | Para ajustar fácilmente tonos oscuros o claros. |
