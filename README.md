# Gastos VIP 😅 | Registro Minimalista de Gastos Innecesarios

https://gastosvip.netlify.app/ 
[![Licencia MIT](https://img.shields.io/badge/Licencia-MIT-blue.svg)](LICENSE.md)

> *"¿Cuánto gastas realmente en lo que no necesitas?"* 

> *"Un experimento en simplicidad extrema y consciencia financiera."*

## 🎯 Motivación
Como trabajador de la cultura reconvertido a desarrollador, necesitaba:
- Una herramienta **sin distracciones** para mis gastos impulsivos.
- Dominar **JavaScript puro** sin frameworks.
- Comprender cómo los conceptos básicos pueden resolver problemas reales.



## El corazón de la app (solo 5 líneas clave)
```javascript

const inputGasto = document.getElementById("inputGasto");
inputGasto.addEventListener('keypress', (e) => {
    /*   
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

    /* Usamos todo el poder de las funciones nombradas para mostrar los mensajes de error */

     function showError(message) {
      errorMessage.textContent = message;
      errorMessage.classList.add("show");
      
      setTimeout(() => {
        errorMessage.classList.remove("show");
      }, 3000);
    }

```


## Características

   1. Single-Purpose: Solo registra gastos innecesarios

   2. Online-First: Luego usa localStorage (no necesita internet)

   3. Dark Mode: CSS Variables + Toggle JavaScript

   4. Feedback Inmediato: Sonidos con Web Audio API

   5. Peso Ligero: 18KB (vs 2MB+ de apps tradicionales)

## Tecnologías Usadas

    JavaScript Vanilla (ES6+):

        - localStorage

        - addEventListener

        - AudioContext

    CSS Moderno:

        Variables (:root)

        Animaciones con keyframes

        Diseño Responsive (@media)

    0 Dependencias


    🚀 Cómo Usarlo

    Clona el repositorio:

    Abre una terminal en tu PC y en la línea de comandos sitúate en el directorio donde copiarás el proyecto.

    Escribe:
    git clone https://github.com/TeewsPepper/gastos-vip-app.git

    Una vez finalizada la descarga abre el directorio de destino y busca el archivo index.html

    Sobre el index.html haz click derecho con el botón del mouse y elige la opción abrir.

    La aplicación se abrirá en el navegador wweb de tu preferencia.

    Escribe el monto y presiona Enter.

    📚 Aprendizajes Clave

    Conceptos Básicos Poderosos:

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