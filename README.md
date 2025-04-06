# Gastos VIP 😅 | Registro Minimalista de Gastos Innecesarios

[![Demo en Vivo](#)](#) <!-- Reemplazar con link real si tienes deploy -->
[![Licencia MIT](https://img.shields.io/badge/Licencia-MIT-blue.svg)](LICENSE)

> *"¿Cuánto gastas realmente en lo que no necesitas?"*  
> Un experimento en simplicidad extrema y consciencia financiera.

## 🎯 Motivación
Como ex-artista reconvertido a desarrollador, necesitaba:
- Una herramienta **sin distracciones** para mis gastos impulsivos
- Dominar **JavaScript puro** sin frameworks
- Comprender cómo los conceptos básicos pueden resolver problemas reales

```javascript
// El corazón de la app (solo 5 líneas clave)

inputGasto.addEventListener('keypress', (e) => {

/*  
   * [CÓDIGO CLAVE] - Explicación extendida:
   * 
   * 1. Este bloque detecta cuando el usuario presiona una tecla
   *    dentro del campo de input (inputGasto).
   * 
   * 2. La condición IF hace dos verificaciones importantes:
   *    - e.key === 'Enter': Revisa si la tecla presionada fue Enter
   *    - !isNaN(parseFloat(e.target.value)): Convierte el texto ingresado a número
   *      y verifica que NO sea "Not a Number" (NaN)
   *
   * 3. Cuando se cumplen ambas condiciones:
   *    - parseFloat(e.target.value): Convierte el texto del input a número decimal
   *    - total += ...: Suma el nuevo gasto al acumulado total
   *    - localStorage.setItem(): Guarda el total actualizado en el almacenamiento
   *      local del navegador (persiste al cerrar/abrir la página)
   *
   * Notas técnicas:
   * - Usamos parseFloat() en lugar de Number() para permitir decimales
   * - !isNaN() es nuestra validación contra valores no numéricos
   * - localStorage solo almacena strings (pero JS hace conversión implícita)
   */
  if (e.key === 'Enter' && !isNaN(parseFloat(e.target.value))) {
    total += parseFloat(e.target.value);
    localStorage.setItem('gastos', total);
  }
});


✨ Características

    Single-Purpose: Solo registra gastos innecesarios

    Offline-First: Usa localStorage (no necesita internet)

    Dark Mode: CSS Variables + Toggle JavaScript

    Feedback Inmediato: Sonidos con Web Audio API

    Peso Ligero: 18KB (vs 2MB+ de apps tradicionales)

🛠️ Tecnologías Usadas

    JavaScript Vanilla (ES6+):

        localStorage

        addEventListener

        AudioContext

    CSS Moderno:

        Variables (:root)

        Animaciones con keyframes

        Diseño Responsive

    0 Dependencias


    🚀 Cómo Usarlo

    Clona el repositorio:
    bash
    Copy

    git clone https://github.com/tuusuario/gastos-vip.git

    Abre index.html en tu navegador (¡no necesita servidor!)

    Escribe el monto y presiona Enter.

📚 Aprendizajes Clave

    Conceptos Básicos Poderosos:
    javascript
    Copy

    // Variables, Eventos, Condicionales y localStorage
    let total = 0;
    elemento.addEventListener('click', () => { ... });
    if (condición) { ... }
    localStorage.getItem('clave');

    UX Minimalista:

        1 input → 1 acción → 1 resultado

        Sin formularios complejos

    Performance Real:

        Carga instantánea incluso en dispositivos antiguos

🌍 Contexto Personal

    "Este proyecto nació de mi transición de la cultura al desarrollo web a los 50 años. Quería probar que los conceptos más simples pueden generar el mayor impacto en la vida real."