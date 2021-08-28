---
title: Comprobación de Automatización de la interfaz de usuario visual
description: Visual Automatización de la interfaz de usuario Verify (Comprobación de Visual UIA) es un Windows \ 32; Controlador GUI para la biblioteca de pruebas de UIA diseñada para realizar pruebas manuales de automatización de la interfaz de usuario.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e8c6118914c791e04226dfa11d2c3bd9548368
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466852"
---
# <a name="visual-ui-automation-verify"></a>Comprobación de Automatización de la interfaz de usuario visual

Visual Automatización de la interfaz de usuario Verify (Visual UIA Verify) es un controlador de interfaz gráfica de usuario de Windows para la biblioteca de pruebas de UIA que está diseñado para pruebas manuales de automatización de la interfaz de usuario. Proporciona una interfaz a la funcionalidad de la biblioteca de pruebas de UIA que elimina la sobrecarga de codificación de una herramienta de línea de comandos.

-   [Comandos de menú](#menu-commands)
-   [Paneles funcionales](#functional-panes)
    -   [Panel árbol de elementos de Automation](#automation-elements-tree-pane)
    -   [Panel Pruebas](#tests-pane)
    -   [Panel Resultados de prueba](#test-results-pane)
    -   [Panel Propiedades](#properties-pane)

Visual UIA Verify solo admite el registrador XML de comprobación de UIA (WUIALoggerXml.dll) de forma nativa. Las transformaciones XML seleccionables por el usuario se incorporan en Visual UIA Verify para presentar varias vistas del informe **del registrador** XML en el Resultados de pruebas datos.

De forma predeterminada, Visual UIA Verify carga Automatización de la interfaz de usuario proveedor del lado cliente que se incluye con la versión original de Automatización de la interfaz de usuario. Puede optar por no cargar este proveedor agregando **/NOCLIENTSIDEPROVIDER** en la opción de línea de comandos de VisualUIVerifyNative.exe.

En la captura de pantalla siguiente se muestran las áreas funcionales principales de la interfaz de usuario de Visual UIA Verify.

![principales áreas funcionales de la interfaz de usuario de comprobación visual](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a>Comandos de menú

En la tabla siguiente se describen los comandos del menú Comprobar de Visual UIA.




| Menú | Comando | Descripción | 
|------|---------|-------------|
| <strong>Archivo</strong> | <strong>Salir</strong> | Salga de Visual UIA Verify. | 
| <strong>Vista</strong> | <strong>Resaltado</strong> | Resalte el rectángulo delimitador del elemento seleccionado en el panel <strong>Árbol de elementos de</strong> Automation. Están disponibles las opciones siguientes:<ul><li><strong>Rectángulo:</strong>línea roja sólida.</li><li><strong>Rectángulo de desvanecimiento:</strong>línea roja sólida que desaparece después de unos segundos.</li><li><strong>Rayas y rectángulo:</strong>línea roja sólida con líneas de resaltado azul adicionales que se radian desde cada esquina del rectángulo delimitador.</li><li><strong>Ninguno:</strong>sin resaltado visible.</li></ul> | 
| <strong>Árbol de elementos de Automation</strong>${REMOVE}$<br /> | <strong>Elemento Refresh Selected</strong> | Actualice los elementos secundarios del elemento seleccionado en el panel <strong>Árbol de elementos de</strong> Automation. La lista de elementos es estática y no se actualiza dinámicamente (automáticamente) si cambia el árbol de elementos. | 
| <strong>Navegación</strong> | Navegue por la jerarquía de árbol de elementos hasta uno de los elementos siguientes.<ul><li><strong>Primario</strong>: vaya al elemento primario.</li><li><strong>Primer elemento</strong>secundario : vaya al primer elemento secundario.</li><li><strong>Siguiente elemento relacionado</strong>: vaya al primer elemento relacionado.</li><li><strong>Anterior relacionado</strong>: vaya al elemento relacionado anterior.</li><li><strong>Último elemento</strong>secundario : vaya al último elemento secundario.</li></ul> | 
| <strong>Modo</strong>${REMOVE}$<br /> | <strong>Always On Superior</strong> | La ventana Comprobar de Visual UIA permanece en la parte superior del pedido z del escritorio. | 
| <strong>Modo de mantener el puntero (usar Ctrl)</strong> | Cuando se presiona la tecla Ctrl, el elemento situado debajo del cursor del mouse se identifica como el elemento de interés. Se actualiza el panel <strong>Árbol de</strong> elementos de Automation y se resalta el elemento correspondiente de la lista de elementos. | 
| <strong>Seguimiento de foco</strong> | A medida que cambia el foco, el elemento con el foco se identifica como el elemento de interés. Se actualiza el panel <strong>Árbol de</strong> elementos de Automation y se resalta el elemento correspondiente de la lista de elementos. | 
| <strong>Prueba</strong>${REMOVE}$<br /> | <strong>Ir a la izquierda</strong> | Mueva un nodo a la izquierda en el <strong>árbol Pruebas.</strong> | 
| <strong>Hacia arriba</strong> | Mueva un nodo hacia arriba en el <strong>árbol Pruebas.</strong> | 
| <strong>Bajar</strong> | Mueva un nodo hacia abajo en el <strong>árbol Pruebas.</strong> | 
| <strong>Ir a la derecha</strong> | Mueva un nodo a la derecha en el <strong>árbol Pruebas.</strong> | 
| <strong>Ejecutar pruebas seleccionadas en el elemento seleccionado</strong> | Ejecute las pruebas seleccionadas desde el <strong>árbol Pruebas</strong> del elemento seleccionado. | 
| <strong>Filtrar problemas conocidos</strong> | Filtre los errores Automatización de la interfaz de usuario conocidos de los resultados de la prueba. | 
| <strong>Ayuda</strong> | <strong>Acerca de Visual Automatización de la interfaz de usuario Verify</strong> | Muestra la versión de software y la información de copyright de Visual UIA Verify. | 




 

## <a name="functional-panes"></a>Paneles funcionales

En esta sección se describen los paneles funcionales de la interfaz de usuario de Comprobación de Visual UIA.

-   [Panel árbol de elementos de Automation](#automation-elements-tree-pane)
-   [Panel Pruebas](#tests-pane)
-   [Panel Resultados de prueba](#test-results-pane)
-   [Panel Propiedades](#properties-pane)

### <a name="automation-elements-tree-pane"></a>Panel árbol de elementos de Automation

El **panel Árbol de elementos de** Automation contiene una instantánea jerárquica de objetos de elementos de automatización que están disponibles para pruebas. El elemento superior del árbol representa el escritorio.

Esta vista es una colección estática que se compila cuando se inicia Visual UIA Verify. Para actualizar la vista en el nodo seleccionado, use el botón de barra de herramientas o el comando de menú **Actualizar elemento** seleccionado.

En la siguiente captura de pantalla se muestra el **panel Árbol de elementos de** Automation.

![panel de árbol de elementos de automatización de la comprobación de uia visual](images/automation-elements-tree-pane.png)

Un nodo atenuado (no disponible) en el árbol de elementos de **Automation** indica que el elemento es miembro de la vista sin formato de Automatización de la interfaz de usuario, pero no cumple las condiciones necesarias para considerarse miembro de la vista de contenido o vista de control. Sin embargo, el elemento todavía se puede probar desde Visual Automatización de la interfaz de usuario Verify. Para obtener más información, vea la información [general Automatización de la interfaz de usuario árbol de archivos](uiauto-treeoverview.md).

Los comandos disponibles en la barra de **herramientas árbol de elementos de Automation** incluyen:

-   **Actualizar:** actualice el nodo seleccionado y sus elementos secundarios. Este comando no actualiza todo el árbol de elementos a menos que se seleccione el nodo raíz.
-   **Primario (Ctrl+Mayús+F6):** vaya al elemento primario del nodo actual.
-   **Primer elemento secundario (Ctrl+Mayús+F7):** vaya al primer elemento secundario del nodo actual.
-   **Siguiente relacionado (Ctrl+Mayús+F8):** vaya al siguiente elemento secundario del mismo nivel del nodo actual.
-   **Anterior relacionado (Ctrl+Mayús+F9):** vaya al nodo anterior del nodo actual.
-   **Último elemento secundario (Ctrl+Mayús+F10):** vaya al último elemento secundario del nodo actual.
-   **Seguimiento de foco:** active o desactive la selección de nodos en función del seguimiento del foco.

### <a name="tests-pane"></a>Panel Pruebas

El **panel** Pruebas contiene una lista de pruebas de Automatización de la interfaz de usuario organizadas por tipo de prueba (elemento de **Automation**, **control** y patrón **)** y prioridad **(** Comprobación de compilación, Prioridad **0,** Prioridad **1,** Prioridad **2** y **Prioridad 3).** Esta lista se genera en función del tipo de control del elemento seleccionado en el panel **Árbol de elementos de** Automation. Para obtener más información, consulta [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

En la siguiente captura de pantalla se muestra **el panel** Pruebas.

![panel de prueba](images/test-pane.png)

Los comandos disponibles en la barra de **herramientas Pruebas** incluyen:

-   **Mostrar**: especifica las Automatización de la interfaz de usuario que se mostrarán; es decir, mostrar todas las pruebas o solo las pruebas adecuadas para el tipo de control del elemento seleccionado en el árbol de **elementos de Automation** (valor predeterminado).
-   **Tipo**: especifica los tipos de prueba que se mostrarán: **Elemento de Automation,** **Patrón** o **Control**.
-   **Prioridades**: especifica las prioridades de prueba que se mostrarán: **Comprobación** de compilación, **Prioridad 0,** **Prioridad 1,** **Prioridad 2** o **Prioridad 3.**
-   **Ir a la** izquierda: vaya al elemento primario del nodo actual.
-   **Subir :** vaya al nodo anterior del nodo actual.
-   **Bajar:** vaya al siguiente nodo relacionado del nodo actual.
-   **Ir a la** derecha: vaya al primer elemento secundario del nodo actual.
-   **Ejecutar pruebas seleccionadas:** ejecuta las pruebas en el elemento seleccionado en el árbol **de elementos de Automation**.

### <a name="test-results-pane"></a>Panel Resultados de prueba

El **Resultados de pruebas** contiene la funcionalidad de registro De comprobación de Visual UIA. En la siguiente captura de pantalla se **muestra Resultados de pruebas** panel.

![panel de resultados de pruebas](images/test-results-pane.png)

Los comandos disponibles en la barra de herramientas **Resultados de pruebas** incluyen:

-   **Atrás:** página atrás en el historial de visualización de informes.
-   **Reenviar**: avance de página en el historial de visualización de informes.
-   **General:** muestra un resumen de los resultados de las **pruebas (superados,** **con** errores y **con un error inesperado).** El resultado de la prueba está vinculado a la **vista Todos los** resultados. El **comando** General muestra una tabla como la siguiente.

    ![tabla general de resultados de pruebas](images/overall-test-results.png)

-   **Todos los** resultados: muestra un registro detallado para cada resultado de la prueba, como se muestra en las tablas siguientes.

    ![detalles de resultados del registro de ejemplo de la vista de todos los resultados](images/all-results-log.png)

    El nombre de la prueba de **la tabla Todos** los resultados está vinculado a una descripción del caso de prueba para el elemento, como en la tabla siguiente.

    ![detalles del caso de prueba](images/test-case-detail.png)

-   **Registro completo:** muestra una vista alternativa del registro detallado para cada resultado de la prueba, como se muestra en la siguiente captura de pantalla.

    ![Vista alternativa de los detalles de un caso de prueba](images/alt-view-of-test-case-detail.png)

-   **XML**: muestra el XML sin formato generado por el registrador XML.
-   **Búsqueda rápida:** búsqueda de texto simple de la vista actual en **Resultados de pruebas** panel.
-   **Abrir en nueva ventana:** abre la vista actual en una nueva instancia de Internet Explorer.

### <a name="properties-pane"></a>Panel Propiedades

El **panel Propiedades** contiene una lista de propiedades Automatización de la interfaz de usuario y valores de propiedad organizados por tipo de propiedad: Accesibilidad **general,** **Identificación,** Patrones **(patrones** de control), **Estado** y **Visibilidad.** Los valores de propiedad se rellenan dinámicamente en función del tipo de control del objeto seleccionado en el panel **Árbol de elementos de** Automation. En la siguiente captura de pantalla se muestra **el panel** Propiedades.

![panel de propiedades](images/properties-pane.png)

Si el control seleccionado admite un patrón de control específico, Visual UIA Verify proporciona la capacidad de llamar a métodos compatibles con ese patrón de control. Por ejemplo, el tipo de [control Ventana](uiauto-supportwindowcontroltype.md) admite el patrón de control  [Ventana](uiauto-implementingwindow.md), que tiene un método [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) que se puede invocar desde el panel Propiedades, como se muestra en la siguiente captura de pantalla. Para obtener más información, consulta [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

![Método close del patrón de control de ventana invocado desde el panel de propiedades](images/close-invoked-from-properties-pane.png)

Los comandos disponibles en la barra **de herramientas Propiedades** incluyen:

-   **Actualizar**: actualice el **árbol De** propiedades.
-   **Expandir todo**: expande todos los nodos del **árbol Propiedades.**

 

 




