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
# <a name="visual-ui-automation-verify"></a><span data-ttu-id="e53d9-103">Comprobación de automatización de la interfaz de usuario visual</span><span class="sxs-lookup"><span data-stu-id="e53d9-103">Visual UI Automation Verify</span></span>

<span data-ttu-id="e53d9-104">La comprobación de la automatización de la interfaz de usuario visual (comprobación de Visual UIA) es un controlador de GUI de Windows para la biblioteca de pruebas de UIA diseñado para realizar pruebas manuales de la automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e53d9-104">Visual UI Automation Verify (Visual UIA Verify) is a Windows GUI driver for the UIA Test Library that is designed for manual testing of UI automation.</span></span> <span data-ttu-id="e53d9-105">Proporciona una interfaz para la funcionalidad de biblioteca de pruebas de UIA que elimina la sobrecarga de codificación de una herramienta de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="e53d9-105">It provides an interface to UIA Test Library functionality that eliminates the coding overhead of a command-line tool.</span></span>

-   [<span data-ttu-id="e53d9-106">Comandos de menú</span><span class="sxs-lookup"><span data-stu-id="e53d9-106">Menu Commands</span></span>](#menu-commands)
-   [<span data-ttu-id="e53d9-107">Paneles funcionales</span><span class="sxs-lookup"><span data-stu-id="e53d9-107">Functional Panes</span></span>](#functional-panes)
    -   [<span data-ttu-id="e53d9-108">Panel del árbol de elementos de automatización</span><span class="sxs-lookup"><span data-stu-id="e53d9-108">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
    -   [<span data-ttu-id="e53d9-109">Panel pruebas</span><span class="sxs-lookup"><span data-stu-id="e53d9-109">Tests Pane</span></span>](#tests-pane)
    -   [<span data-ttu-id="e53d9-110">Panel Resultados de prueba</span><span class="sxs-lookup"><span data-stu-id="e53d9-110">Test Results Pane</span></span>](#test-results-pane)
    -   [<span data-ttu-id="e53d9-111">Panel Propiedades</span><span class="sxs-lookup"><span data-stu-id="e53d9-111">Properties Pane</span></span>](#properties-pane)

<span data-ttu-id="e53d9-112">La comprobación de Visual UIA solo admite el registrador XML de UIA verify (WUIALoggerXml.dll) de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="e53d9-112">Visual UIA Verify supports only the UIA Verify XML logger (WUIALoggerXml.dll) natively.</span></span> <span data-ttu-id="e53d9-113">Las transformaciones XML seleccionables por el usuario se incorporan en Visual UIA Verify para presentar diversas vistas del informe de registrador XML en el panel **resultados de pruebas** .</span><span class="sxs-lookup"><span data-stu-id="e53d9-113">User-selectable XML transformations are incorporated into Visual UIA Verify to present various views of the XML logger report in the **Test Results** pane.</span></span>

<span data-ttu-id="e53d9-114">De forma predeterminada, visual UIA Verify carga el proveedor del lado cliente de automatización de la interfaz de usuario que se incluye con la versión original de la automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e53d9-114">By default, Visual UIA Verify loads the UI Automation client-side provider that shipped with the original release of UI Automation.</span></span> <span data-ttu-id="e53d9-115">Puede optar por no cargar este proveedor agregando **/NOCLIENTSIDEPROVIDER** en la opción de línea de comandos de VisualUIVerifyNative.exe.</span><span class="sxs-lookup"><span data-stu-id="e53d9-115">You can choose not to load this provider by adding **/NOCLIENTSIDEPROVIDER** in the command-line option of VisualUIVerifyNative.exe.</span></span>

<span data-ttu-id="e53d9-116">En la captura de pantalla siguiente se muestran las principales áreas funcionales de la interfaz de usuario de verify visual UIA.</span><span class="sxs-lookup"><span data-stu-id="e53d9-116">The following screen shot shows the main functional areas of the Visual UIA Verify user interface.</span></span>

![principales áreas funcionales de la interfaz de usuario de verify visual UIA](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a><span data-ttu-id="e53d9-118">Comandos de menú</span><span class="sxs-lookup"><span data-stu-id="e53d9-118">Menu Commands</span></span>

<span data-ttu-id="e53d9-119">En la tabla siguiente se describen los comandos del menú comprobar de Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="e53d9-119">The following table describes the commands in the Visual UIA Verify menu.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e53d9-120">Menú</span><span class="sxs-lookup"><span data-stu-id="e53d9-120">Menu</span></span></th>
<th><span data-ttu-id="e53d9-121">Get-Help</span><span class="sxs-lookup"><span data-stu-id="e53d9-121">Command</span></span></th>
<th><span data-ttu-id="e53d9-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e53d9-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e53d9-123"><strong>Archivo</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-123"><strong>File</strong></span></span></td>
<td><span data-ttu-id="e53d9-124"><strong>Salir</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-124"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="e53d9-125">Salga de Visual UIA verify.</span><span class="sxs-lookup"><span data-stu-id="e53d9-125">Exit Visual UIA Verify.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e53d9-126"><strong>Vista</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-126"><strong>View</strong></span></span></td>
<td><span data-ttu-id="e53d9-127"><strong>Resaltado</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-127"><strong>Highlighting</strong></span></span></td>
<td><span data-ttu-id="e53d9-128">Resalte el rectángulo delimitador del elemento seleccionado en el panel de <strong>árbol de elementos de automatización</strong> .</span><span class="sxs-lookup"><span data-stu-id="e53d9-128">Highlight the bounding rectangle of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="e53d9-129">Están disponibles las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="e53d9-129">The following options are available.</span></span>
<ul>
<li><span data-ttu-id="e53d9-130"><strong>Rectángulo</strong>: una línea roja sólida.</span><span class="sxs-lookup"><span data-stu-id="e53d9-130"><strong>Rectangle</strong>—A solid red line.</span></span></li>
<li><span data-ttu-id="e53d9-131"><strong>Rectángulo de difuminación</strong>: una línea roja sólida que desaparece después de unos segundos.</span><span class="sxs-lookup"><span data-stu-id="e53d9-131"><strong>Fading Rectangle</strong>—A solid red line that disappears after a few seconds.</span></span></li>
<li><span data-ttu-id="e53d9-132"><strong>Rayos y rectángulo</strong>: una línea roja sólida con líneas de resaltado azules adicionales que intervienen de cada esquina del rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="e53d9-132"><strong>Rays and Rectangle</strong>—A solid red line with additional blue highlight lines that radiate from each corner of the bounding rectangle.</span></span></li>
<li><span data-ttu-id="e53d9-133"><strong>Ninguno</strong>: sin resaltado visible.</span><span class="sxs-lookup"><span data-stu-id="e53d9-133"><strong>None</strong>—No visible highlight.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="e53d9-134"><strong>Árbol de elementos de automatización</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="e53d9-134"><strong>Automation Elements Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="e53d9-135"><strong>Actualizar elemento seleccionado</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-135"><strong>Refresh Selected Element</strong></span></span></td>
<td><span data-ttu-id="e53d9-136">Actualice los elementos secundarios del elemento seleccionado en el panel de <strong>árbol de elementos de automatización</strong> .</span><span class="sxs-lookup"><span data-stu-id="e53d9-136">Refresh the children of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="e53d9-137">La lista de elementos es estática y no se actualiza dinámicamente (automáticamente) si cambia el árbol de elementos.</span><span class="sxs-lookup"><span data-stu-id="e53d9-137">The list of elements is static and does not refresh dynamically (automatically) if the element tree changes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e53d9-138"><strong>Navegación</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-138"><strong>Navigation</strong></span></span></td>
<td><span data-ttu-id="e53d9-139">Desplácese por la jerarquía del árbol de elementos a uno de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="e53d9-139">Navigate through the element tree hierarchy to one of the following elements.</span></span>
<ul>
<li><span data-ttu-id="e53d9-140"><strong>Parent</strong>: ir a elemento primario.</span><span class="sxs-lookup"><span data-stu-id="e53d9-140"><strong>Parent</strong>—Go to parent element.</span></span></li>
<li><span data-ttu-id="e53d9-141"><strong>Primer elemento secundario</strong>: ir al primer elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="e53d9-141"><strong>First Child</strong>—Go to first child element.</span></span></li>
<li><span data-ttu-id="e53d9-142"><strong>Siguiente relacionado</strong>: ir al primer elemento del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="e53d9-142"><strong>Next Sibling</strong>—Go to first sibling element.</span></span></li>
<li><span data-ttu-id="e53d9-143"><strong>Relacionado anterior</strong>: ir al elemento anterior del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="e53d9-143"><strong>Previous Sibling</strong>—Go to previous sibling element.</span></span></li>
<li><span data-ttu-id="e53d9-144"><strong>Último elemento secundario</strong>: ir al último elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="e53d9-144"><strong>Last Child</strong>—Go to last child element.</span></span></li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="e53d9-145"><strong>Modo</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="e53d9-145"><strong>Mode</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="e53d9-146"><strong>Always On superior</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-146"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="e53d9-147">La ventana comprobar de Visual UIA permanece en la parte superior del orden z del escritorio.</span><span class="sxs-lookup"><span data-stu-id="e53d9-147">The Visual UIA Verify window remains at the top of the desktop z-order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e53d9-148"><strong>Modo de desplazamiento (usar Ctrl)</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-148"><strong>Hover Mode (Use Ctrl)</strong></span></span></td>
<td><span data-ttu-id="e53d9-149">Cuando se presiona la tecla Ctrl, el elemento situado debajo del cursor del mouse se identifica como el elemento de interés.</span><span class="sxs-lookup"><span data-stu-id="e53d9-149">When the Ctrl key is pressed, the element under the mouse cursor is identified as the element of interest.</span></span> <span data-ttu-id="e53d9-150">Se actualiza el panel de <strong>árbol de elementos de automatización</strong> y se resalta el elemento correspondiente en la lista de elementos.</span><span class="sxs-lookup"><span data-stu-id="e53d9-150">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e53d9-151"><strong>Seguimiento del foco</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-151"><strong>Focus Tracking</strong></span></span></td>
<td><span data-ttu-id="e53d9-152">A medida que cambia el foco, el elemento con el foco se identifica como el elemento de interés.</span><span class="sxs-lookup"><span data-stu-id="e53d9-152">As the focus changes, the element with the focus is identified as the element of interest.</span></span> <span data-ttu-id="e53d9-153">Se actualiza el panel de <strong>árbol de elementos de automatización</strong> y se resalta el elemento correspondiente en la lista de elementos.</span><span class="sxs-lookup"><span data-stu-id="e53d9-153">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="e53d9-154"><strong>Pruebas</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="e53d9-154"><strong>Tests</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="e53d9-155"><strong>Ir a la izquierda</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-155"><strong>Go Left</strong></span></span></td>
<td><span data-ttu-id="e53d9-156">Mueve un nodo a la izquierda en el árbol de <strong>pruebas</strong> .</span><span class="sxs-lookup"><span data-stu-id="e53d9-156">Move one node left in the <strong>Tests</strong> tree.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e53d9-157"><strong>Hacia arriba</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-157"><strong>Go Up</strong></span></span></td>
<td><span data-ttu-id="e53d9-158">Subir un nodo en el árbol de <strong>pruebas</strong> .</span><span class="sxs-lookup"><span data-stu-id="e53d9-158">Move one node up in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e53d9-159"><strong>Bajar</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-159"><strong>Go Down</strong></span></span></td>
<td><span data-ttu-id="e53d9-160">Bajar un nodo en el árbol de <strong>pruebas</strong> .</span><span class="sxs-lookup"><span data-stu-id="e53d9-160">Move one node down in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e53d9-161"><strong>Ir a la derecha</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-161"><strong>Go Right</strong></span></span></td>
<td><span data-ttu-id="e53d9-162">Mueve un nodo a la derecha en el árbol de <strong>pruebas</strong> .</span><span class="sxs-lookup"><span data-stu-id="e53d9-162">Move one node right in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e53d9-163"><strong>Ejecutar pruebas seleccionadas en el elemento seleccionado</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-163"><strong>Run Selected Test(s) On Selected Element</strong></span></span></td>
<td><span data-ttu-id="e53d9-164">Ejecuta las pruebas seleccionadas desde el árbol de <strong>pruebas</strong> en el elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e53d9-164">Run the selected tests from the <strong>Tests</strong> tree on the selected element.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e53d9-165"><strong>Filtrar problemas conocidos</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-165"><strong>Filter Known Problems</strong></span></span></td>
<td><span data-ttu-id="e53d9-166">Filtre los errores conocidos de automatización de la interfaz de usuario de los resultados de pruebas.</span><span class="sxs-lookup"><span data-stu-id="e53d9-166">Filter known UI Automation bugs from the test results.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e53d9-167"><strong>Ayuda</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-167"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="e53d9-168"><strong>Acerca de la comprobación de automatización de la interfaz de usuario</strong></span><span class="sxs-lookup"><span data-stu-id="e53d9-168"><strong>About Visual UI Automation Verify</strong></span></span></td>
<td><span data-ttu-id="e53d9-169">Muestra la versión de software y la información de copyright de Visual UIA verify.</span><span class="sxs-lookup"><span data-stu-id="e53d9-169">Display the software version and copyright information for Visual UIA Verify.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a><span data-ttu-id="e53d9-170">Paneles funcionales</span><span class="sxs-lookup"><span data-stu-id="e53d9-170">Functional Panes</span></span>

<span data-ttu-id="e53d9-171">En esta sección se describen los paneles funcionales de la interfaz de usuario de verify visual UIA.</span><span class="sxs-lookup"><span data-stu-id="e53d9-171">This section describes the functional panes in the Visual UIA Verify user interface.</span></span>

-   [<span data-ttu-id="e53d9-172">Panel del árbol de elementos de automatización</span><span class="sxs-lookup"><span data-stu-id="e53d9-172">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
-   [<span data-ttu-id="e53d9-173">Panel pruebas</span><span class="sxs-lookup"><span data-stu-id="e53d9-173">Tests Pane</span></span>](#tests-pane)
-   [<span data-ttu-id="e53d9-174">Panel Resultados de prueba</span><span class="sxs-lookup"><span data-stu-id="e53d9-174">Test Results Pane</span></span>](#test-results-pane)
-   [<span data-ttu-id="e53d9-175">Panel Propiedades</span><span class="sxs-lookup"><span data-stu-id="e53d9-175">Properties Pane</span></span>](#properties-pane)

### <a name="automation-elements-tree-pane"></a><span data-ttu-id="e53d9-176">Panel del árbol de elementos de automatización</span><span class="sxs-lookup"><span data-stu-id="e53d9-176">Automation Elements Tree Pane</span></span>

<span data-ttu-id="e53d9-177">El panel de **árbol de elementos de automatización** contiene una instantánea jerárquica de los objetos de elemento de automatización que están disponibles para las pruebas.</span><span class="sxs-lookup"><span data-stu-id="e53d9-177">The **Automation Elements Tree** pane contains a hierarchical snapshot of automation element objects that are available for testing.</span></span> <span data-ttu-id="e53d9-178">El elemento superior del árbol representa el escritorio.</span><span class="sxs-lookup"><span data-stu-id="e53d9-178">The top element in the tree represents the desktop.</span></span>

<span data-ttu-id="e53d9-179">Esta vista es una colección estática que se compila cuando se inicia visual UIA verify.</span><span class="sxs-lookup"><span data-stu-id="e53d9-179">This view is a static collection that is compiled when Visual UIA Verify starts.</span></span> <span data-ttu-id="e53d9-180">Para actualizar la vista en el nodo seleccionado, use el comando de menú **Actualizar elemento seleccionado** o el botón de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e53d9-180">To refresh the view at the selected node, use the **Refresh Selected Element** menu command or toolbar button.</span></span>

<span data-ttu-id="e53d9-181">En la captura de pantalla siguiente se muestra el panel del **árbol elementos de automatización** .</span><span class="sxs-lookup"><span data-stu-id="e53d9-181">The following screen shot shows the **Automation Elements Tree** pane.</span></span>

![panel del árbol de elementos de automatización de Visual UIA verify](images/automation-elements-tree-pane.png)

<span data-ttu-id="e53d9-183">Un nodo atenuado (no disponible) en el **árbol de elementos de automatización** indica que el elemento es miembro de la vista sin formato de automatización de la interfaz de usuario, pero no cumple las condiciones necesarias para que se considere un miembro de la vista de contenido o la vista de control.</span><span class="sxs-lookup"><span data-stu-id="e53d9-183">A dimmed (unavailable) node in the **Automation Elements Tree** indicates that the element is a member of the UI Automation raw view, but does not meet the conditions necessary to be considered a member of the content view or control view.</span></span> <span data-ttu-id="e53d9-184">Sin embargo, todavía se puede probar el elemento desde la comprobación de la automatización de la interfaz de usuario visual.</span><span class="sxs-lookup"><span data-stu-id="e53d9-184">However, the element can still be tested from Visual UI Automation Verify.</span></span> <span data-ttu-id="e53d9-185">Para obtener más información, vea [información general del árbol de automatización](uiauto-treeoverview.md)de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e53d9-185">For more information, see the [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="e53d9-186">Los comandos disponibles en la barra de herramientas del **árbol de elementos de automatización** incluyen:</span><span class="sxs-lookup"><span data-stu-id="e53d9-186">Commands available from the **Automation Elements Tree** toolbar include:</span></span>

-   <span data-ttu-id="e53d9-187">**Actualizar**: actualice el nodo seleccionado y sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e53d9-187">**Refresh**—Refresh the selected node and its children.</span></span> <span data-ttu-id="e53d9-188">Este comando no actualiza todo el árbol de elementos a menos que se seleccione el nodo raíz.</span><span class="sxs-lookup"><span data-stu-id="e53d9-188">This command does not refresh the entire element tree unless the root node is selected.</span></span>
-   <span data-ttu-id="e53d9-189">**Primario (Ctrl + Mayús + F6)**: ir al elemento primario del nodo actual.</span><span class="sxs-lookup"><span data-stu-id="e53d9-189">**Parent (Ctrl+Shift+F6)**—Go to parent of the current node.</span></span>
-   <span data-ttu-id="e53d9-190">**Primer elemento secundario (Ctrl + Mayús + F7)**: ir al primer elemento secundario del nodo actual..</span><span class="sxs-lookup"><span data-stu-id="e53d9-190">**First Child (Ctrl+Shift+F7)**—Go to first child of the current node..</span></span>
-   <span data-ttu-id="e53d9-191">**Siguiente relacionado (Ctrl + Mayús + F8)**: ir al siguiente elemento secundario del mismo nivel del nodo actual.</span><span class="sxs-lookup"><span data-stu-id="e53d9-191">**Next Sibling (Ctrl+Shift+F8)**—Go to next sibling child of the current node.</span></span>
-   <span data-ttu-id="e53d9-192">**Relacionado anterior (Ctrl + Mayús + F9)**: ir al elemento anterior del mismo nivel del nodo actual.</span><span class="sxs-lookup"><span data-stu-id="e53d9-192">**Previous Sibling (Ctrl+Shift+F9)**—Go to previous sibling of the current node.</span></span>
-   <span data-ttu-id="e53d9-193">**Último elemento secundario (Ctrl + Mayús + F10)**: va al último elemento secundario del nodo actual.</span><span class="sxs-lookup"><span data-stu-id="e53d9-193">**Last Child (Ctrl+Shift+F10)**—Go to last child of the current node.</span></span>
-   <span data-ttu-id="e53d9-194">**Seguimiento de foco**: alternar la selección de nodo activada o desactivada en función del seguimiento del foco.</span><span class="sxs-lookup"><span data-stu-id="e53d9-194">**Focus Tracking**—Toggle node selection on or off based on focus tracking.</span></span>

### <a name="tests-pane"></a><span data-ttu-id="e53d9-195">Panel pruebas</span><span class="sxs-lookup"><span data-stu-id="e53d9-195">Tests Pane</span></span>

<span data-ttu-id="e53d9-196">El **Panel pruebas** contiene una lista de pruebas de automatización de la interfaz de usuario organizadas por tipo de prueba (**elemento de automatización**, **control** y **patrón**) y prioridad (**comprobación de compilación**, **prioridad 0**, **prioridad 1**, **prioridad 2** y **prioridad 3**).</span><span class="sxs-lookup"><span data-stu-id="e53d9-196">The **Tests** pane contains a list of UI Automation tests organized by test type (**Automation Element**, **Control**, and **Pattern**) and priority (**Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, and **Priority 3**).</span></span> <span data-ttu-id="e53d9-197">Esta lista se genera basándose en el tipo de control del elemento seleccionado en el panel de **árbol de elementos de automatización** .</span><span class="sxs-lookup"><span data-stu-id="e53d9-197">This list is generated based on the control type of the selected element in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="e53d9-198">Para obtener más información, consulta [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e53d9-198">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="e53d9-199">En la captura de pantalla siguiente se muestra el panel **pruebas** .</span><span class="sxs-lookup"><span data-stu-id="e53d9-199">The following screen shot shows the **Tests** pane.</span></span>

![panel prueba](images/test-pane.png)

<span data-ttu-id="e53d9-201">Los comandos disponibles en la barra de herramientas **pruebas** incluyen:</span><span class="sxs-lookup"><span data-stu-id="e53d9-201">Commands available from the **Tests** toolbar include:</span></span>

-   <span data-ttu-id="e53d9-202">**Show**: especifica las pruebas de automatización de la interfaz de usuario que se van a mostrar. es decir, se muestran todas las pruebas o solo las pruebas adecuadas para el tipo de control del elemento seleccionado en el **árbol de elementos de automatización** (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="e53d9-202">**Show**—Specifies the UI Automation tests to display; that is, display all tests or only tests suited to the control type of the selected element in the **Automation Elements Tree** (default).</span></span>
-   <span data-ttu-id="e53d9-203">**Tipo**: especifica los tipos de prueba que se van a mostrar: **elemento de automatización**, **patrón** o **control**.</span><span class="sxs-lookup"><span data-stu-id="e53d9-203">**Type**—Specifies the test types to display: **Automation Element**, **Pattern**, or **Control**.</span></span>
-   <span data-ttu-id="e53d9-204">**Prioridades**: especifica las prioridades de prueba que se van a mostrar: **comprobación de compilación**, **prioridad 0**, **prioridad 1**, **prioridad 2** o **prioridad 3**.</span><span class="sxs-lookup"><span data-stu-id="e53d9-204">**Priorities**—Specifies the test priorities to display: **Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, or **Priority 3**.</span></span>
-   <span data-ttu-id="e53d9-205">**Ir** a la izquierda: vaya al elemento primario del nodo actual.</span><span class="sxs-lookup"><span data-stu-id="e53d9-205">**Go Left**—Go to the parent of the current node.</span></span>
-   <span data-ttu-id="e53d9-206">**Subir: ir** al elemento anterior del mismo nivel del nodo actual.</span><span class="sxs-lookup"><span data-stu-id="e53d9-206">**Go Up**—Go to the previous sibling of the current node.</span></span>
-   <span data-ttu-id="e53d9-207">**Bajar**: ir al siguiente elemento del mismo nivel del nodo actual.</span><span class="sxs-lookup"><span data-stu-id="e53d9-207">**Go Down**—Go to the next sibling of the current node.</span></span>
-   <span data-ttu-id="e53d9-208">**Ir** a la derecha: ir al primer elemento secundario del nodo actual.</span><span class="sxs-lookup"><span data-stu-id="e53d9-208">**Go Right**—Go to the first child of the current node.</span></span>
-   <span data-ttu-id="e53d9-209">**Ejecutar pruebas seleccionadas**: ejecuta las pruebas en el elemento seleccionado en el **árbol de elementos de automatización**.</span><span class="sxs-lookup"><span data-stu-id="e53d9-209">**Run Selected Test(s)**—Runs the tests on the element selected in the **Automation Elements Tree**.</span></span>

### <a name="test-results-pane"></a><span data-ttu-id="e53d9-210">Panel Resultados de prueba</span><span class="sxs-lookup"><span data-stu-id="e53d9-210">Test Results Pane</span></span>

<span data-ttu-id="e53d9-211">El panel de **resultados de pruebas** contiene la funcionalidad de comprobación de registro de Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="e53d9-211">The **Test Results** pane contains the Visual UIA Verify logging functionality.</span></span> <span data-ttu-id="e53d9-212">En la captura de pantalla siguiente se muestra el panel **resultados de pruebas** .</span><span class="sxs-lookup"><span data-stu-id="e53d9-212">The following screen shot shows the **Test Results** pane.</span></span>

![panel de resultados de pruebas](images/test-results-pane.png)

<span data-ttu-id="e53d9-214">Los comandos disponibles en la barra de herramientas de **resultados de pruebas** incluyen:</span><span class="sxs-lookup"><span data-stu-id="e53d9-214">Commands available from the **Tests Results** toolbar include:</span></span>

-   <span data-ttu-id="e53d9-215">**Atrás**: página hacia atrás en el historial de visualización del informe.</span><span class="sxs-lookup"><span data-stu-id="e53d9-215">**Back**—Page backward in report viewing history.</span></span>
-   <span data-ttu-id="e53d9-216">**Avanzar**: página hacia delante en el historial de visualización del informe.</span><span class="sxs-lookup"><span data-stu-id="e53d9-216">**Forward**—Page forward in report viewing history.</span></span>
-   <span data-ttu-id="e53d9-217">**General**: muestra un resumen de los resultados de la prueba (**superado**, **error** e **inesperado**).</span><span class="sxs-lookup"><span data-stu-id="e53d9-217">**Overall**—Displays a summary of the test results (**Passed**, **Failed**, and **Unexpected Error**).</span></span> <span data-ttu-id="e53d9-218">El resultado de la prueba se vincula a la vista **todos los resultados** .</span><span class="sxs-lookup"><span data-stu-id="e53d9-218">The test result is linked to the **All Results** view.</span></span> <span data-ttu-id="e53d9-219">El comando **General** muestra una tabla como la siguiente.</span><span class="sxs-lookup"><span data-stu-id="e53d9-219">The **Overall** command displays a table like the following one.</span></span>

    ![tabla de resultados de pruebas generales](images/overall-test-results.png)

-   <span data-ttu-id="e53d9-221">**Todos los resultados**: muestra un registro detallado de cada resultado de la prueba, como se muestra en las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="e53d9-221">**All Results**— Displays a detailed log for each test result, as shown in the following tables.</span></span>

    ![detalle del resultado del registro de ejemplo en la vista todos los resultados](images/all-results-log.png)

    <span data-ttu-id="e53d9-223">El nombre de la prueba de la tabla **todos los resultados** se vincula a una descripción del caso de prueba para el elemento, como en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e53d9-223">The test name in the **All Results** table is linked to a test case description for the element, as in the following table.</span></span>

    ![detalles del caso de prueba](images/test-case-detail.png)

-   <span data-ttu-id="e53d9-225">**Registro completo**: muestra una vista alternativa del registro detallado de cada resultado de la prueba, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e53d9-225">**Full Log**—Displays an alternate view of the detailed log for each test result, as shown in the following screen shot.</span></span>

    ![Vista alternativa de los detalles de un caso de prueba](images/alt-view-of-test-case-detail.png)

-   <span data-ttu-id="e53d9-227">**XML**: muestra el XML sin formato generado por el registrador XML.</span><span class="sxs-lookup"><span data-stu-id="e53d9-227">**XML**—Displays the raw XML generated by the XML logger.</span></span>
-   <span data-ttu-id="e53d9-228">Búsqueda **rápida**: búsqueda de texto simple de la vista actual en el panel de **resultados de pruebas** .</span><span class="sxs-lookup"><span data-stu-id="e53d9-228">**Quick Find**—Simple text search of the current view in the **Test Results** pane.</span></span>
-   <span data-ttu-id="e53d9-229">**Abrir en nueva ventana**: abre la vista actual en una nueva instancia de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e53d9-229">**Open in New Window**—Opens the current view in a new instance of Internet Explorer.</span></span>

### <a name="properties-pane"></a><span data-ttu-id="e53d9-230">Panel Propiedades</span><span class="sxs-lookup"><span data-stu-id="e53d9-230">Properties Pane</span></span>

<span data-ttu-id="e53d9-231">El panel **propiedades** contiene una lista de propiedades de automatización de la interfaz de usuario y valores de propiedad organizados por tipo de propiedad: **accesibilidad general**, **identificación**, **patrones** (patrones de control), **Estado** y **visibilidad**.</span><span class="sxs-lookup"><span data-stu-id="e53d9-231">The **Properties** pane contains a list of UI Automation properties and property values organized by property type: **General Accessibility**, **Identification**, **Patterns** (control patterns), **State**, and **Visibility**.</span></span> <span data-ttu-id="e53d9-232">Los valores de propiedad se rellenan dinámicamente basándose en el tipo de control del objeto seleccionado en el panel de **árbol elementos de automatización** .</span><span class="sxs-lookup"><span data-stu-id="e53d9-232">The property values are dynamically populated based on the control type of the object selected in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="e53d9-233">En la captura de pantalla siguiente se muestra el panel de **propiedades** .</span><span class="sxs-lookup"><span data-stu-id="e53d9-233">The following screen shot shows the **Properties** pane.</span></span>

![panel Propiedades](images/properties-pane.png)

<span data-ttu-id="e53d9-235">Si el control seleccionado admite un patrón de control concreto, visual UIA Verify proporciona la capacidad de llamar a los métodos admitidos por ese patrón de control.</span><span class="sxs-lookup"><span data-stu-id="e53d9-235">If the selected control supports a specific control pattern, Visual UIA Verify provides the ability to call methods that are supported by that control pattern.</span></span> <span data-ttu-id="e53d9-236">Por ejemplo, el [tipo de control window](uiauto-supportwindowcontroltype.md) es compatible con el [patrón de control window](uiauto-implementingwindow.md), que tiene un método [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) que se puede invocar desde el panel **propiedades** , como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e53d9-236">For example, the [Window control type](uiauto-supportwindowcontroltype.md) supports the [Window control pattern](uiauto-implementingwindow.md), which has a [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) method that can be invoked from the **Properties** pane, as shown in the following screen shot.</span></span> <span data-ttu-id="e53d9-237">Para obtener más información, consulta [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e53d9-237">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

![método Close del patrón de control window invocado desde el panel de propiedades](images/close-invoked-from-properties-pane.png)

<span data-ttu-id="e53d9-239">Los comandos disponibles en la barra de herramientas de **propiedades** incluyen:</span><span class="sxs-lookup"><span data-stu-id="e53d9-239">Commands available from the **Properties** toolbar include:</span></span>

-   <span data-ttu-id="e53d9-240">**Actualizar**: actualice el árbol de **propiedades** .</span><span class="sxs-lookup"><span data-stu-id="e53d9-240">**Refresh**—Refresh the **Properties** tree.</span></span>
-   <span data-ttu-id="e53d9-241">**Expandir todo**: expande todos los nodos del árbol de **propiedades** .</span><span class="sxs-lookup"><span data-stu-id="e53d9-241">**Expand All**—Expands all nodes in the **Properties** tree.</span></span>

 

 




