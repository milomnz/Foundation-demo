# Taller Práctico: Foundation UI Framework - Grupo 4

Este repositorio contiene una demostración práctica de maquetación y diseño de interfaces de usuario utilizando **Foundation for Sites**. 

**Desarrollado por el Grupo 4:**
* Juan Camilo
* Santiago Bonilla
* Camila Mendez

---

Foundation es uno de los frameworks CSS front-end responsivos más avanzados y robustos del ecosistema de desarrollo web.

## Arquitectura de la Demo

El proyecto está estructurado con un enfoque didáctico tipo "Página Viva" (Living Page), donde la interfaz gráfica renderizada sirve también como documentación y catálogo de componentes.

- **`index.html`**: Es el núcleo del proyecto. Contiene la implementación práctica de múltiples componentes (navbar, tipografía, tarjetas, formularios y botones), unificados en una sola vista con una explicación teórica al lado de cada implementación.
- **`css/foundation.css`**: Archivo base del framework Foundation.
- **`css/app.css`**: Archivo para las hojas de estilo en cascada personalizadas. Esta demo se utiliza para cargar y aplicar globalmente la tipografía *Outfit* desde Google Fonts, la cual Foundation hereda de manera inteligente en todos sus submódulos.
- **`js/vendor/` y `js/app.js`**: Dependencias JavaScript (incluyendo jQuery y el core de Foundation) para inicializar componentes interactivos como la Top Bar, modales y acordeones.

## Conceptos Teóricos Claves de Foundation
### 1. Sistema de Grid (XY Grid)
El corazón estructural de Foundation es su **XY Grid**, un motor de cuadrículas construido íntegramente sobre Flexbox.
- Se utilizan las clases `.grid-x` (para controlar el flujo horizontal o las filas) y `.cell` (para definir las columnas).
- Se complementa con clases para controlar los canalones (gutters) como `.grid-padding-x`.
- El sistema utiliza nomenclatura Mobile-First: `small-12`, `medium-6`, `large-4` para definir el comportamiento responsivo de las celdas en diferentes tamaños de pantalla.

### 2. Estados y Paleta Semántica
A diferencia de crear docenas de estilos manuales, Foundation provee clases de estado que cambian radicalmente la estética de los elementos (como callouts, botones o etiquetas) basándose en una semántica de intención:
- **`primary`** (Principal/Defecto)
- **`secondary`** (Secundario/Neutro)
- **`success`** (Éxito/Positivo)
- **`warning`** (Advertencia)
- **`alert`** (Peligro/Error)

### 3. Componentes Modulares y Ensamblables
Foundation trata los componentes de interfaz como bloques de construcción flexibles:
- **Top Bar (Barra de Navegación):** Construida sobre el componente menú, permitiendo submenús expansibles, áreas izquierda (`.top-bar-left`) y derecha (`.top-bar-right`).
- **Tarjetas (Cards):** Utilizan un contenedor maestro `.card`, combinado con contenedores interiores `.card-divider` (para generar secciones contrastantes como encabezados) y `.card-section` (para contener el texto asegurando el *padding* correcto).
- **Botones:** Generados mediante la clase base `.button` y alterados estructuralmente sumando clases de modificadores de tamaño (`.large`, `.small`), estado (`.success`, `.alert`) o diseño (`.hollow` para botones delineados, `.expanded` para botones de ancho completo 100%).
- **Formularios Semánticos:** Foundation mantiene el HTML asombrosamente limpio. En lugar de requerir que agregues múltiples clases a cada campo, asume la estilización global de inputs. Al anidar los `input` dentro de `label`, Foundation automáticamente crea un flujo vertical limpio y alineado.

### 4. Utilidades Tipográficas
Foundation elimina la necesidad de crear estilos CSS manuales para el control del texto, proveyendo clases nativas:
- **`.lead`**: Para resaltar y aumentar levemente el tamaño de párrafos importantes.
- **`.subheader`**: Para atenuar y cambiar el peso visual de subtítulos de apoyo.
- **Clases de alineación**: Como `.text-center`, `.text-left`, `.text-right`.

## Instrucciones de Uso

Para ejecutar y estudiar esta demostración:
1. Asegúrate de tener clonado o descargado el proyecto en tu entorno local.
2. Simplemente abre el archivo `index.html` haciendo doble clic en él en tu sistema, o usa una extensión como *Live Server* en VSCode.
3. Lee las explicaciones en la página mientras tienes tu editor de código abierto al lado, para poder observar de primera mano la relación entre las clases HTML y el resultado visual.
