# PROYECTO PRACTICO EXPERIMENTAL 4 - Semana 16

## 1. Introducción
El presente documento detalla la evolución y mejora de una aplicación de escritorio para la gestión de tareas diarias, desarrollada en **Python** con la biblioteca **Tkinter**. Esta versión, correspondiente a la Semana 16, se enfoca en la incorporación de atajos de teclado para optimizar la interacción del usuario, manteniendo la estricta adherencia a una arquitectura modular por capas, previamente establecida en la Semana 15.

## 2. Arquitectura del Sistema
La aplicación conserva su estructura modular, garantizando la separación de responsabilidades y facilitando el mantenimiento y la escalabilidad. Las capas principales son:

| Capa | Archivo | Responsabilidad |
| :--- | :--- | :--- |
| **Modelo** | `modelos/tarea.py` | Define la entidad `Tarea` y sus atributos (ID, descripción, estado de completado). |
| **Servicio** | `servicios/tarea_servicio.py` | Encapsula la lógica de negocio para la gestión de tareas (CRUD) en memoria. |
| **Interfaz (UI)** | `ui/app_tkinter.py` | Gestiona la presentación visual, la captura de eventos de usuario (ratón y teclado) y la actualización de la interfaz. |
| **Orquestador** | `main.py` | Punto de entrada de la aplicación, encargado de inicializar las dependencias y arrancar el bucle principal de Tkinter. |

## 3. Implementación Técnica

### 3.1. Capa de Modelo
La clase `Tarea` (`modelos/tarea.py`) permanece sin cambios, sirviendo como la representación fundamental de una tarea con `id`, `descripcion` y `estado_completado`.

### 3.2. Capa de Servicio
La clase `TareaServicio` (`servicios/tarea_servicio.py`) mantiene su funcionalidad original, proporcionando los métodos para `agregar_tarea`, `completar_tarea`, `eliminar_tarea` y `listar_tareas`. La lógica de negocio sigue siendo independiente de la interfaz de usuario.

### 3.3. Capa de Interfaz de Usuario (GUI)
La clase `AppTkinter` (`ui/app_tkinter.py`) ha sido mejorada para incorporar una interacción más rica a través de atajos de teclado, además de los eventos de ratón ya existentes. Las mejoras clave incluyen:

*   **Manejo de Eventos Avanzados**:
    *   **Teclado (`<Return>`)**: Al presionar la tecla `Enter` en el campo de entrada, se añade una nueva tarea, replicando la funcionalidad del botón "Añadir Tarea".
    *   **Teclado (`<c>`)**: Al presionar la tecla `C`, la tarea actualmente seleccionada en el `Treeview` se marca como completada.
    *   **Teclado (`<d>` o `<Delete>`)**: Al presionar la tecla `D` o `Delete`, la tarea seleccionada se elimina de la lista.
    *   **Teclado (`<Escape>`)**: Al presionar la tecla `Escape`, la aplicación se cierra de manera controlada.
    *   **Ratón (`<Double-1>`)**: Se mantiene la funcionalidad de doble clic sobre un elemento del `Treeview` para marcar una tarea como completada.

*   **Feedback Visual**: Se conserva y mejora el feedback visual, donde las tareas completadas se muestran con texto gris y tachado, facilitando la distinción entre tareas pendientes y finalizadas.

## 4. Conclusión
La evolución de la aplicación de la Semana 15 a la Semana 16 demuestra cómo una arquitectura modular permite la incorporación de nuevas funcionalidades, como los atajos de teclado, sin comprometer la estructura o la lógica subyacente. Estas mejoras no solo aumentan la eficiencia y la usabilidad de la aplicación, sino que también refuerzan los principios de diseño de software robusto y mantenible.



---

---
**Autor:** MINAYA GARCIA CRISTOPHER (MinWare)

**Fecha:** 1 de abril de 2026


