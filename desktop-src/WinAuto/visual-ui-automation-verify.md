---
title: Comprobación de automatización de la interfaz de usuario visual
description: Comprobación de automatización de la interfaz de usuario visual (comprobación de Visual UIA) es un Windows \ 32; Controlador de GUI para la biblioteca de pruebas de UIA diseñado para realizar pruebas manuales de la automatización de la interfaz de usuario.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e224a52d243427af86c6cd27a3add3be03d9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779308"
---
# <a name="visual-ui-automation-verify"></a>Comprobación de automatización de la interfaz de usuario visual

La comprobación de la automatización de la interfaz de usuario visual (comprobación de Visual UIA) es un controlador de GUI de Windows para la biblioteca de pruebas de UIA diseñado para realizar pruebas manuales de la automatización de la interfaz de usuario. Proporciona una interfaz para la funcionalidad de biblioteca de pruebas de UIA que elimina la sobrecarga de codificación de una herramienta de línea de comandos.

-   [Comandos de menú](#menu-commands)
-   [Paneles funcionales](#functional-panes)
    -   [Panel del árbol de elementos de automatización](#automation-elements-tree-pane)
    -   [Panel pruebas](#tests-pane)
    -   [Panel Resultados de prueba](#test-results-pane)
    -   [Panel Propiedades](#properties-pane)

La comprobación de Visual UIA solo admite el registrador XML de UIA verify (WUIALoggerXml.dll) de forma nativa. Las transformaciones XML seleccionables por el usuario se incorporan en Visual UIA Verify para presentar diversas vistas del informe de registrador XML en el panel **resultados de pruebas** .

De forma predeterminada, visual UIA Verify carga el proveedor del lado cliente de automatización de la interfaz de usuario que se incluye con la versión original de la automatización de la interfaz de usuario. Puede optar por no cargar este proveedor agregando **/NOCLIENTSIDEPROVIDER** en la opción de línea de comandos de VisualUIVerifyNative.exe.

En la captura de pantalla siguiente se muestran las principales áreas funcionales de la interfaz de usuario de verify visual UIA.

![principales áreas funcionales de la interfaz de usuario de verify visual UIA](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a>Comandos de menú

En la tabla siguiente se describen los comandos del menú comprobar de Visual UIA.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Menú</th>
<th>Get-Help</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Archivo</strong></td>
<td><strong>Salir</strong></td>
<td>Salga de Visual UIA verify.</td>
</tr>
<tr class="even">
<td><strong>Vista</strong></td>
<td><strong>Resaltado</strong></td>
<td>Resalte el rectángulo delimitador del elemento seleccionado en el panel de <strong>árbol de elementos de automatización</strong> . Están disponibles las opciones siguientes:
<ul>
<li><strong>Rectángulo</strong>: una línea roja sólida.</li>
<li><strong>Rectángulo de difuminación</strong>: una línea roja sólida que desaparece después de unos segundos.</li>
<li><strong>Rayos y rectángulo</strong>: una línea roja sólida con líneas de resaltado azules adicionales que intervienen de cada esquina del rectángulo delimitador.</li>
<li><strong>Ninguno</strong>: sin resaltado visible.</li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><strong>Árbol de elementos de automatización</strong>$ {Remove} $<br />
</td>
<td><strong>Actualizar elemento seleccionado</strong></td>
<td>Actualice los elementos secundarios del elemento seleccionado en el panel de <strong>árbol de elementos de automatización</strong> . La lista de elementos es estática y no se actualiza dinámicamente (automáticamente) si cambia el árbol de elementos.</td>
</tr>
<tr class="even">
<td><strong>Navegación</strong></td>
<td>Desplácese por la jerarquía del árbol de elementos a uno de los siguientes elementos.
<ul>
<li><strong>Parent</strong>: ir a elemento primario.</li>
<li><strong>Primer elemento secundario</strong>: ir al primer elemento secundario.</li>
<li><strong>Siguiente relacionado</strong>: ir al primer elemento del mismo nivel.</li>
<li><strong>Relacionado anterior</strong>: ir al elemento anterior del mismo nivel.</li>
<li><strong>Último elemento secundario</strong>: ir al último elemento secundario.</li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><strong>Modo</strong>$ {Remove} $<br />
</td>
<td><strong>Always On superior</strong></td>
<td>La ventana comprobar de Visual UIA permanece en la parte superior del orden z del escritorio.</td>
</tr>
<tr class="even">
<td><strong>Modo de desplazamiento (usar Ctrl)</strong></td>
<td>Cuando se presiona la tecla Ctrl, el elemento situado debajo del cursor del mouse se identifica como el elemento de interés. Se actualiza el panel de <strong>árbol de elementos de automatización</strong> y se resalta el elemento correspondiente en la lista de elementos.</td>

</tr>
<tr class="odd">
<td><strong>Seguimiento del foco</strong></td>
<td>A medida que cambia el foco, el elemento con el foco se identifica como el elemento de interés. Se actualiza el panel de <strong>árbol de elementos de automatización</strong> y se resalta el elemento correspondiente en la lista de elementos.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>Pruebas</strong>$ {Remove} $<br />
</td>
<td><strong>Ir a la izquierda</strong></td>
<td>Mueve un nodo a la izquierda en el árbol de <strong>pruebas</strong> .</td>
</tr>
<tr class="odd">
<td><strong>Hacia arriba</strong></td>
<td>Subir un nodo en el árbol de <strong>pruebas</strong> .</td>

</tr>
<tr class="even">
<td><strong>Bajar</strong></td>
<td>Bajar un nodo en el árbol de <strong>pruebas</strong> .</td>

</tr>
<tr class="odd">
<td><strong>Ir a la derecha</strong></td>
<td>Mueve un nodo a la derecha en el árbol de <strong>pruebas</strong> .</td>

</tr>
<tr class="even">
<td><strong>Ejecutar pruebas seleccionadas en el elemento seleccionado</strong></td>
<td>Ejecuta las pruebas seleccionadas desde el árbol de <strong>pruebas</strong> en el elemento seleccionado.</td>

</tr>
<tr class="odd">
<td><strong>Filtrar problemas conocidos</strong></td>
<td>Filtre los errores conocidos de automatización de la interfaz de usuario de los resultados de pruebas.</td>

</tr>
<tr class="even">
<td><strong>Ayuda</strong></td>
<td><strong>Acerca de la comprobación de automatización de la interfaz de usuario</strong></td>
<td>Muestra la versión de software y la información de copyright de Visual UIA verify.</td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a>Paneles funcionales

En esta sección se describen los paneles funcionales de la interfaz de usuario de verify visual UIA.

-   [Panel del árbol de elementos de automatización](#automation-elements-tree-pane)
-   [Panel pruebas](#tests-pane)
-   [Panel Resultados de prueba](#test-results-pane)
-   [Panel Propiedades](#properties-pane)

### <a name="automation-elements-tree-pane"></a>Panel del árbol de elementos de automatización

El panel de **árbol de elementos de automatización** contiene una instantánea jerárquica de los objetos de elemento de automatización que están disponibles para las pruebas. El elemento superior del árbol representa el escritorio.

Esta vista es una colección estática que se compila cuando se inicia visual UIA verify. Para actualizar la vista en el nodo seleccionado, use el comando de menú **Actualizar elemento seleccionado** o el botón de la barra de herramientas.

En la captura de pantalla siguiente se muestra el panel del **árbol elementos de automatización** .

![panel del árbol de elementos de automatización de Visual UIA verify](images/automation-elements-tree-pane.png)

Un nodo atenuado (no disponible) en el **árbol de elementos de automatización** indica que el elemento es miembro de la vista sin formato de automatización de la interfaz de usuario, pero no cumple las condiciones necesarias para que se considere un miembro de la vista de contenido o la vista de control. Sin embargo, todavía se puede probar el elemento desde la comprobación de la automatización de la interfaz de usuario visual. Para obtener más información, vea [información general del árbol de automatización](uiauto-treeoverview.md)de la interfaz de usuario.

Los comandos disponibles en la barra de herramientas del **árbol de elementos de automatización** incluyen:

-   **Actualizar**: actualice el nodo seleccionado y sus elementos secundarios. Este comando no actualiza todo el árbol de elementos a menos que se seleccione el nodo raíz.
-   **Primario (Ctrl + Mayús + F6)**: ir al elemento primario del nodo actual.
-   **Primer elemento secundario (Ctrl + Mayús + F7)**: ir al primer elemento secundario del nodo actual..
-   **Siguiente relacionado (Ctrl + Mayús + F8)**: ir al siguiente elemento secundario del mismo nivel del nodo actual.
-   **Relacionado anterior (Ctrl + Mayús + F9)**: ir al elemento anterior del mismo nivel del nodo actual.
-   **Último elemento secundario (Ctrl + Mayús + F10)**: va al último elemento secundario del nodo actual.
-   **Seguimiento de foco**: alternar la selección de nodo activada o desactivada en función del seguimiento del foco.

### <a name="tests-pane"></a>Panel pruebas

El **Panel pruebas** contiene una lista de pruebas de automatización de la interfaz de usuario organizadas por tipo de prueba (**elemento de automatización**, **control** y **patrón**) y prioridad (**comprobación de compilación**, **prioridad 0**, **prioridad 1**, **prioridad 2** y **prioridad 3**). Esta lista se genera basándose en el tipo de control del elemento seleccionado en el panel de **árbol de elementos de automatización** . Para obtener más información, consulta [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

En la captura de pantalla siguiente se muestra el panel **pruebas** .

![panel prueba](images/test-pane.png)

Los comandos disponibles en la barra de herramientas **pruebas** incluyen:

-   **Show**: especifica las pruebas de automatización de la interfaz de usuario que se van a mostrar. es decir, se muestran todas las pruebas o solo las pruebas adecuadas para el tipo de control del elemento seleccionado en el **árbol de elementos de automatización** (valor predeterminado).
-   **Tipo**: especifica los tipos de prueba que se van a mostrar: **elemento de automatización**, **patrón** o **control**.
-   **Prioridades**: especifica las prioridades de prueba que se van a mostrar: **comprobación de compilación**, **prioridad 0**, **prioridad 1**, **prioridad 2** o **prioridad 3**.
-   **Ir** a la izquierda: vaya al elemento primario del nodo actual.
-   **Subir: ir** al elemento anterior del mismo nivel del nodo actual.
-   **Bajar**: ir al siguiente elemento del mismo nivel del nodo actual.
-   **Ir** a la derecha: ir al primer elemento secundario del nodo actual.
-   **Ejecutar pruebas seleccionadas**: ejecuta las pruebas en el elemento seleccionado en el **árbol de elementos de automatización**.

### <a name="test-results-pane"></a>Panel Resultados de prueba

El panel de **resultados de pruebas** contiene la funcionalidad de comprobación de registro de Visual UIA. En la captura de pantalla siguiente se muestra el panel **resultados de pruebas** .

![panel de resultados de pruebas](images/test-results-pane.png)

Los comandos disponibles en la barra de herramientas de **resultados de pruebas** incluyen:

-   **Atrás**: página hacia atrás en el historial de visualización del informe.
-   **Avanzar**: página hacia delante en el historial de visualización del informe.
-   **General**: muestra un resumen de los resultados de la prueba (**superado**, **error** e **inesperado**). El resultado de la prueba se vincula a la vista **todos los resultados** . El comando **General** muestra una tabla como la siguiente.

    ![tabla de resultados de pruebas generales](images/overall-test-results.png)

-   **Todos los resultados**: muestra un registro detallado de cada resultado de la prueba, como se muestra en las tablas siguientes.

    ![detalle del resultado del registro de ejemplo en la vista todos los resultados](images/all-results-log.png)

    El nombre de la prueba de la tabla **todos los resultados** se vincula a una descripción del caso de prueba para el elemento, como en la tabla siguiente.

    ![detalles del caso de prueba](images/test-case-detail.png)

-   **Registro completo**: muestra una vista alternativa del registro detallado de cada resultado de la prueba, como se muestra en la siguiente captura de pantalla.

    ![Vista alternativa de los detalles de un caso de prueba](images/alt-view-of-test-case-detail.png)

-   **XML**: muestra el XML sin formato generado por el registrador XML.
-   Búsqueda **rápida**: búsqueda de texto simple de la vista actual en el panel de **resultados de pruebas** .
-   **Abrir en nueva ventana**: abre la vista actual en una nueva instancia de Internet Explorer.

### <a name="properties-pane"></a>Panel Propiedades

El panel **propiedades** contiene una lista de propiedades de automatización de la interfaz de usuario y valores de propiedad organizados por tipo de propiedad: **accesibilidad general**, **identificación**, **patrones** (patrones de control), **Estado** y **visibilidad**. Los valores de propiedad se rellenan dinámicamente basándose en el tipo de control del objeto seleccionado en el panel de **árbol elementos de automatización** . En la captura de pantalla siguiente se muestra el panel de **propiedades** .

![panel Propiedades](images/properties-pane.png)

Si el control seleccionado admite un patrón de control concreto, visual UIA Verify proporciona la capacidad de llamar a los métodos admitidos por ese patrón de control. Por ejemplo, el [tipo de control window](uiauto-supportwindowcontroltype.md) es compatible con el [patrón de control window](uiauto-implementingwindow.md), que tiene un método [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) que se puede invocar desde el panel **propiedades** , como se muestra en la siguiente captura de pantalla. Para obtener más información, consulta [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

![método Close del patrón de control window invocado desde el panel de propiedades](images/close-invoked-from-properties-pane.png)

Los comandos disponibles en la barra de herramientas de **propiedades** incluyen:

-   **Actualizar**: actualice el árbol de **propiedades** .
-   **Expandir todo**: expande todos los nodos del árbol de **propiedades** .

 

 




