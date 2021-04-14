---
title: La interfaz gráfica de usuario de AccChecker
description: En este tema se describen los elementos que componen la GUI de AccChecker.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26d847d1bc198958ca28dd77d67b0e99b9d7745
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104555404"
---
# <a name="the-accchecker-graphical-user-interface"></a><span data-ttu-id="8baff-103">La interfaz gráfica de usuario de AccChecker</span><span class="sxs-lookup"><span data-stu-id="8baff-103">The AccChecker Graphical User Interface</span></span>

<span data-ttu-id="8baff-104">En este tema se describen los elementos que componen la GUI de AccChecker.</span><span class="sxs-lookup"><span data-stu-id="8baff-104">This topic describes the elements that make up the AccChecker GUI.</span></span>

-   [<span data-ttu-id="8baff-105">Pestaña comprobaciones</span><span class="sxs-lookup"><span data-stu-id="8baff-105">Verifications Tab</span></span>](#verifications-tab)
-   [<span data-ttu-id="8baff-106">Pestaña resultados</span><span class="sxs-lookup"><span data-stu-id="8baff-106">Results Tab</span></span>](#results-tab)
-   [<span data-ttu-id="8baff-107">Pestañas de lector de pantalla de MSAA y UIA</span><span class="sxs-lookup"><span data-stu-id="8baff-107">MSAA and UIA Screen Reader Tabs</span></span>](#msaa-and-uia-screen-reader-tabs)
-   [<span data-ttu-id="8baff-108">Pestañas de los árboles MSAA y UIA</span><span class="sxs-lookup"><span data-stu-id="8baff-108">MSAA and UIA Tree Tabs</span></span>](#msaa-and-uia-tree-tabs)
-   [<span data-ttu-id="8baff-109">Menú Archivo</span><span class="sxs-lookup"><span data-stu-id="8baff-109">File Menu</span></span>](#file-menu)
-   [<span data-ttu-id="8baff-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8baff-110">Related topics</span></span>](#related-topics)

## <a name="verifications-tab"></a><span data-ttu-id="8baff-111">Pestaña comprobaciones</span><span class="sxs-lookup"><span data-stu-id="8baff-111">Verifications Tab</span></span>

<span data-ttu-id="8baff-112">AccChecker se inicia con la vista predeterminada de la pestaña **comprobaciones** :</span><span class="sxs-lookup"><span data-stu-id="8baff-112">AccChecker starts with the default view of the **Verifications** tab:</span></span>

![Captura de pantalla que muestra la pestaña ' comprobaciones ' en el comprobador de accesibilidad U I.](images/accchecker-verifications-tab.png)

<span data-ttu-id="8baff-114">La pestaña **comprobaciones** contiene los siguientes componentes.</span><span class="sxs-lookup"><span data-stu-id="8baff-114">The **Verifications** tab contains the following components.</span></span>

-   <span data-ttu-id="8baff-115">**Selector de destino de comprobación** Ofrece las siguientes opciones para seleccionar un control o una aplicación de destino.</span><span class="sxs-lookup"><span data-stu-id="8baff-115">**Verification target selector** Offers the following options for selecting a target application or control.</span></span>
    -   <span data-ttu-id="8baff-116">Elija un destino en la lista desplegable rellenada previamente.</span><span class="sxs-lookup"><span data-stu-id="8baff-116">Choose a target from the pre-populated drop-down list.</span></span> <span data-ttu-id="8baff-117">Esta lista contiene todos los HWND de nivel superior identificados en el inicio.</span><span class="sxs-lookup"><span data-stu-id="8baff-117">This list contains all top-level HWNDs identified at start-up.</span></span>
    -   <span data-ttu-id="8baff-118">Elija un HWND en función de la ubicación del cursor del mouse (los controles seleccionables se resaltan con un rectángulo rojo).</span><span class="sxs-lookup"><span data-stu-id="8baff-118">Choose an HWND based on the location of the mouse cursor (selectable controls are highlighted with a red rectangle).</span></span> <span data-ttu-id="8baff-119">Esta opción permite seleccionar cualquier objeto visible que tenga un HWND.</span><span class="sxs-lookup"><span data-stu-id="8baff-119">This option lets you select any visible object that has an HWND.</span></span>
    -   <span data-ttu-id="8baff-120">Escriba un HWND determinado.</span><span class="sxs-lookup"><span data-stu-id="8baff-120">Enter a particular HWND.</span></span>
-   <span data-ttu-id="8baff-121">**Lista de comprobación de rutinas de comprobación** Proporciona la capacidad de seleccionar la rutina de comprobación deseada que se va a realizar en una aplicación o un control.</span><span class="sxs-lookup"><span data-stu-id="8baff-121">**Verification routines checklist** Provides the ability to select the desired verification routine to be performed against an application or control.</span></span> <span data-ttu-id="8baff-122">Vea rutinas de comprobación para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8baff-122">See Verification Routines for more information.</span></span>
-   <span data-ttu-id="8baff-123">**Selector de archivos de supresión de errores y advertencias** Los archivos de supresión se generan en la pestaña **resultados** de la comprobación. Al hacer clic con el botón secundario en un mensaje de error o advertencia y seleccionar **suprimir** en el menú contextual, se establece una marca para ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="8baff-123">**Error and warning suppression file selector** Suppression files are generated from the verification **Results** tab. By right-clicking an error or warning message and selecting **Suppress** from the context menu, a flag is set for that message.</span></span> <span data-ttu-id="8baff-124">Si la casilla de **supresión** está activada, las entradas suprimidas aparecen en la lista.</span><span class="sxs-lookup"><span data-stu-id="8baff-124">If the **Suppressions** check box is checked, suppressed entries appear in the list.</span></span> <span data-ttu-id="8baff-125">Una entrada suprimida se puede eliminar mediante el mismo menú contextual que se usa para suprimirla.</span><span class="sxs-lookup"><span data-stu-id="8baff-125">A suppressed entry can be unsuppressed by using the same context menu used to suppress it.</span></span>

    <span data-ttu-id="8baff-126">Un archivo de supresión se guarda en formato XML seleccionando **Guardar supresión** en el menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="8baff-126">A suppression file is saved in XML format by selecting **Save Suppression** from the **File** menu.</span></span> <span data-ttu-id="8baff-127">Este archivo se usa en ejecuciones de comprobación posteriores en las que se ocultan los mensajes.</span><span class="sxs-lookup"><span data-stu-id="8baff-127">This file is consumed on subsequent verification runs where the messages will be hidden.</span></span> <span data-ttu-id="8baff-128">Para quitar el archivo de supresión, haga clic en **Borrar**.</span><span class="sxs-lookup"><span data-stu-id="8baff-128">To remove the suppression file, click **Clear**.</span></span> <span data-ttu-id="8baff-129">Para obtener información sobre mensajes específicos, vea mensajes de registro de comprobación.</span><span class="sxs-lookup"><span data-stu-id="8baff-129">For information on specific messages, see Verification Log Messages.</span></span> <span data-ttu-id="8baff-130">Use **Guardar registro** en el menú **archivo** para guardar la lista completa como un archivo de registro en XML o como un archivo de texto con formato.</span><span class="sxs-lookup"><span data-stu-id="8baff-130">Use **Save Log** from the **File** menu to save the entire list as a log file in XML or as a formatted text file.</span></span>

    ![accchecker pestaña resultados con el elemento de contexto suprimir resaltado](images/accchecker-results-tab-with-suppress.png)

    <span data-ttu-id="8baff-132">En el ejemplo siguiente se muestra el contenido de un archivo de supresión generado al ejecutar las comprobaciones de **propiedades** en la aplicación del panel de control de Firewall de Windows.</span><span class="sxs-lookup"><span data-stu-id="8baff-132">The following example shows the content of a suppression file generated by running the **Properties** verifications on the Windows Firewall control panel application.</span></span> <span data-ttu-id="8baff-133">El error con el identificador "ElementHasNoName" se eligió para su supresión en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8baff-133">The error with an ID of "ElementHasNoName" was chosen for suppression in this example.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?><ArrayOfLogEvent xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema">
      <LogEvent>
        <EventID>ElementHasNoName</EventID>
        <Text>Element has no name</Text>
        <ParentChain>Windows Firewall.Windows Firewall</ParentChain>
        <VerificationRoutine>VerificationRoutines.CheckName</VerificationRoutine>
        <Classname>ATL:BUTTON</Classname>
        <AccName />
        <AccRole>PushButton</AccRole>
      </LogEvent>
    </ArrayOfLogEvent>
    ```

    

-   <span data-ttu-id="8baff-134">**Mostrar resultados con prioridad** Ofrece las siguientes opciones para filtrar los resultados de la comprobación por prioridad.</span><span class="sxs-lookup"><span data-stu-id="8baff-134">**Show prioritized results** Offers the following options for filtering the verification results by priority.</span></span>
    -   <span data-ttu-id="8baff-135">**Todo** Incluye todos los resultados independientemente de la prioridad.</span><span class="sxs-lookup"><span data-stu-id="8baff-135">**All** Include all all results regardless of priority.</span></span>
    -   <span data-ttu-id="8baff-136">**Solo P1** Incluya solo los resultados de prioridad 0 y prioridad 1.</span><span class="sxs-lookup"><span data-stu-id="8baff-136">**P1 only** Include only priority 0 and priority 1 results.</span></span>
    -   <span data-ttu-id="8baff-137">**Solo P1 P2** Incluya los resultados de la prioridad 0 a la prioridad 2.</span><span class="sxs-lookup"><span data-stu-id="8baff-137">**P1   P2 only** Include priority 0 through priority 2 results.</span></span>
-   <span data-ttu-id="8baff-138">**Ejecutar comprobaciones seleccionadas** Proporciona el botón **ejecutar comprobaciones** para iniciar el proceso de comprobación.</span><span class="sxs-lookup"><span data-stu-id="8baff-138">**Run selected verifications** Provides the **Run Verifications** button for starting the verification process.</span></span> <span data-ttu-id="8baff-139">Mientras se ejecutan las comprobaciones, el botón cambia a **Cancelar comprobaciones** y se puede usar para detener las comprobaciones después de que se complete la actual.</span><span class="sxs-lookup"><span data-stu-id="8baff-139">While verifications are running, the button changes to **Cancel Verifications** and can be used to stop the verifications after the current one completes.</span></span>

## <a name="results-tab"></a><span data-ttu-id="8baff-140">Pestaña Resultados</span><span class="sxs-lookup"><span data-stu-id="8baff-140">Results Tab</span></span>

<span data-ttu-id="8baff-141">La pestaña **resultados** se rellena después de que se hayan completado las tareas de comprobación seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="8baff-141">The **Results** tab is populated after the selected verification tasks are complete.</span></span> <span data-ttu-id="8baff-142">Consta de los siguientes componentes.</span><span class="sxs-lookup"><span data-stu-id="8baff-142">It consists of the following components.</span></span>

-   <span data-ttu-id="8baff-143">La lista de mensajes, que muestra los mensajes de error, de advertencia e informativos generados por las tareas de comprobación seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="8baff-143">The message list, which displays the error, warning, and informational messages generated by the selected verification tasks.</span></span> <span data-ttu-id="8baff-144">Los mensajes mostrados se pueden filtrar por tipo mediante las casillas situadas encima de la lista de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8baff-144">The messages displayed can be filtered by type using the checkboxes above the message list.</span></span>
-   <span data-ttu-id="8baff-145">Los detalles del mensaje y una captura de pantalla del destino de la comprobación.</span><span class="sxs-lookup"><span data-stu-id="8baff-145">The message details and a screen capture of the verification target.</span></span> <span data-ttu-id="8baff-146">Al seleccionar un mensaje en la lista de mensajes se muestran más detalles y se resalta el elemento correspondiente en el panel Captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="8baff-146">Selecting a message from the message list displays further details and highlights the corresponding element in the screen capture pane.</span></span> <span data-ttu-id="8baff-147">El botón **visualizar** , cambia AccChecker a la pestaña de **árbol de MSAA** . Si se resalta un error en la pestaña **resultados** , el elemento correspondiente se resalta en la pestaña **árbol de MSAA** .</span><span class="sxs-lookup"><span data-stu-id="8baff-147">The **Visualize** button, switches AccChecker to the **MSAA Tree** tab. If an error is highlighted on the **Results** tab, the corresponding element is highlighted on the **MSAA Tree** tab.</span></span>

<span data-ttu-id="8baff-148">Al hacer clic con el botón secundario en un mensaje, se expone un menú contextual con los elementos siguientes.</span><span class="sxs-lookup"><span data-stu-id="8baff-148">Right-clicking on a message exposes a context menu with the following items.</span></span>

-   <span data-ttu-id="8baff-149">**Suprimir** Agrega el mensaje a la lista de supresión.</span><span class="sxs-lookup"><span data-stu-id="8baff-149">**Suppress** Adds the message to the suppression list.</span></span>
-   <span data-ttu-id="8baff-150">**Copiar al portapapeles** Copia los detalles del mensaje en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="8baff-150">**Copy to clipboard** Copies the message details to the clipboard.</span></span>
-   <span data-ttu-id="8baff-151">**Visualizar** Cambia AccChecker a la pestaña de **árbol de MSAA** . Se resalta el elemento que se corresponde con el error seleccionado.</span><span class="sxs-lookup"><span data-stu-id="8baff-151">**Visualize** Switches AccChecker to the **MSAA Tree** tab. The element that corresponds to the selected error is highlighted.</span></span>
-   <span data-ttu-id="8baff-152">**Ayuda** de Muestra información adicional sobre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8baff-152">**Help** Displays additional information about the message.</span></span>

## <a name="msaa-and-uia-screen-reader-tabs"></a><span data-ttu-id="8baff-153">Pestañas de lector de pantalla de MSAA y UIA</span><span class="sxs-lookup"><span data-stu-id="8baff-153">MSAA and UIA Screen Reader Tabs</span></span>

<span data-ttu-id="8baff-154">Las pestañas lector de pantalla de MSAA y lector de pantalla de UIA son similares.</span><span class="sxs-lookup"><span data-stu-id="8baff-154">The MSAA Screen reader and the UIA Screen reader tabs are similar.</span></span> <span data-ttu-id="8baff-155">Ambos muestran una transcripción de los elementos encontrados en un recorrido simulado del destino de la comprobación por un lector de pantalla, excepto en que se muestra la implementación de MSAA y el otro muestra la implementación de UIA.</span><span class="sxs-lookup"><span data-stu-id="8baff-155">Both display a transcript of elements encountered in a simulated traversal of the verification target by a screen reader, except that one shows the MSAA implementation, and the other shows the UIA implemention.</span></span>

<span data-ttu-id="8baff-156">Los elementos se desplazan y se registran de la misma forma que un lector de pantalla los leería.</span><span class="sxs-lookup"><span data-stu-id="8baff-156">Elements are navigated and logged just as a screen reader would read them.</span></span> <span data-ttu-id="8baff-157">La información que se presenta en esta pestaña es esencial para confirmar que solo se anuncia información útil y relevante.</span><span class="sxs-lookup"><span data-stu-id="8baff-157">The information presented on this tab is essential to confirm that only useful and relevant information is being announced.</span></span> <span data-ttu-id="8baff-158">Por ejemplo, es aceptable un nombre de control de sonido normal como "MenuItem Edit" o "PushButton Close". sin embargo, el nombre de un control que no tiene sentido, como "CPNavPanel22" o "DefaultValue1", no es aceptable.</span><span class="sxs-lookup"><span data-stu-id="8baff-158">For example, a normal-sounding control name such as "MenuItem Edit" or "PushButton Close" is acceptable; however, a control name that doesn't make sense, such as "CPNavPanel22" or "DefaultValue1", is not acceptable.</span></span> <span data-ttu-id="8baff-159">El botón **visualizar** , hace que AccChecker cambie al árbol de **MSAA** o a la pestaña de **árbol de UIA** . Si un elemento está resaltado en la pestaña **lector de pantalla** , el elemento correspondiente se resalta en la pestaña árbol de **MSAA** o en el **árbol de UIA** .</span><span class="sxs-lookup"><span data-stu-id="8baff-159">The **Visualize** button, causes AccChecker to switch to the **MSAA Tree** or **UIA Tree** tab. If an element is highlighted on the **Screen Reader** tab, the corresponding element is highlighted on the **MSAA Tree** or **UIA Tree** tab.</span></span>

<span data-ttu-id="8baff-160">La rutina de comprobación de **ScreenReader** en la que **se debe realizar** la comprobación debe estar seleccionada en la pestaña **comprobaciones** para que se muestre la **pestaña lector de pantalla de MSAA** .</span><span class="sxs-lookup"><span data-stu-id="8baff-160">The **ScreenReader** verification routine under **Consistence** must be selected in the **Verifications** tab for the **MSAA Screen reader tab** to be displayed.</span></span> <span data-ttu-id="8baff-161">Del mismo modo, se debe seleccionar la rutina de comprobación **UiaScreenReader** para que se muestre la pestaña **lector de pantalla de UIA** .</span><span class="sxs-lookup"><span data-stu-id="8baff-161">Similarly, the **UiaScreenReader** verification routine must be selected for the **UIA Screen reader** tab to be displayed.</span></span>

<span data-ttu-id="8baff-162">En la captura de pantalla siguiente se muestra la pestaña lector de pantalla de UIA con una comprobación de ejemplo del Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="8baff-162">The following screen shot shows the UIA Screen reader tab with a sample verification of Notepad.</span></span>

![accchecker pestaña lector de pantalla que muestra los resultados de comprobación de ejemplo](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a><span data-ttu-id="8baff-164">Pestañas de los árboles MSAA y UIA</span><span class="sxs-lookup"><span data-stu-id="8baff-164">MSAA and UIA Tree Tabs</span></span>

<span data-ttu-id="8baff-165">Al ejecutar cualquier rutina de comprobación, AccChecker se compilan todos los elementos visibles en el destino de comprobación y se muestran jerárquicamente en la pestaña de **árbol de MSAA** y en la pestaña de **árbol de UIA** . En la captura de pantalla siguiente se muestra la pestaña árbol de MSAA con la jerarquía de elementos del Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="8baff-165">Running any verification routine causes AccChecker to compile all visible elements in the verification target and display them hierarchically on the **MSAA Tree** tab and the **UIA Tree** tab. The following screen shot shows the MSAA Tree tab with the hierarchy of elements for Notepad.</span></span>

![accchecker pestaña de árbol de MSAA](images/accchecker-tree-tab.png)

## <a name="file-menu"></a><span data-ttu-id="8baff-167">Menú Archivo</span><span class="sxs-lookup"><span data-stu-id="8baff-167">File Menu</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8baff-168">Menú</span><span class="sxs-lookup"><span data-stu-id="8baff-168">Menu</span></span></th>
<th><span data-ttu-id="8baff-169">Get-Help</span><span class="sxs-lookup"><span data-stu-id="8baff-169">Command</span></span></th>
<th><span data-ttu-id="8baff-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="8baff-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="8baff-171"><strong>Archivo</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8baff-171"><strong>File</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8baff-172"><strong>Abrir</strong></span><span class="sxs-lookup"><span data-stu-id="8baff-172"><strong>Open</strong></span></span></td>
<td><span data-ttu-id="8baff-173">Proporciona las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="8baff-173">Provides the following options.</span></span><br/>
<ul>
<li><span data-ttu-id="8baff-174"><strong>Comprobaciones dll</strong> Abre un archivo DLL de comprobación.</span><span class="sxs-lookup"><span data-stu-id="8baff-174"><strong>Verifications DLL</strong> Opens a verification DLL.</span></span> <span data-ttu-id="8baff-175">Las comprobaciones de AccChecker nativas se encapsulan en un archivo DLL independiente (VerificationRoutines.dll).</span><span class="sxs-lookup"><span data-stu-id="8baff-175">Native AccChecker verifications are encapsulated in a standalone DLL (VerificationRoutines.dll).</span></span> <span data-ttu-id="8baff-176">Este diseño permite a los equipos de pruebas crear su propio conjunto de comprobaciones basadas en la plataforma de interfaz de usuario que se está probando.</span><span class="sxs-lookup"><span data-stu-id="8baff-176">This design allows test teams to create their own set of verifications based on the UI platform being tested.</span></span></li>
<li><span data-ttu-id="8baff-177"><strong>Archivo de registro</strong> Permite elegir un archivo de registro de comprobación para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="8baff-177"><strong>Log file</strong> Lets you choose a verification log file to open.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8baff-178"><strong>Cargar automáticamente comprobaciones disponibles</strong></span><span class="sxs-lookup"><span data-stu-id="8baff-178"><strong>Automatically load available verifications</strong></span></span></td>
<td><span data-ttu-id="8baff-179">Carga automáticamente todas las comprobaciones de AccChecker disponibles.</span><span class="sxs-lookup"><span data-stu-id="8baff-179">Automatically loads all available AccChecker verifications.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8baff-180"><strong>Guardar registro</strong></span><span class="sxs-lookup"><span data-stu-id="8baff-180"><strong>Save Log</strong></span></span></td>
<td><span data-ttu-id="8baff-181">Guarde el registro de comprobación como XML o como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="8baff-181">Save the verification log as XML or as plain text.</span></span> <span data-ttu-id="8baff-182">El texto sin formato es más legible.</span><span class="sxs-lookup"><span data-stu-id="8baff-182">Plain text is more readable.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8baff-183"><strong>Guardar supresión</strong></span><span class="sxs-lookup"><span data-stu-id="8baff-183"><strong>Save Suppression</strong></span></span></td>
<td><span data-ttu-id="8baff-184">Guarde el registro de supresión como XML.</span><span class="sxs-lookup"><span data-stu-id="8baff-184">Save the suppression log as XML.</span></span> <span data-ttu-id="8baff-185">Este archivo especifica los mensajes de comprobación que se van a omitir en las pruebas de regresión.</span><span class="sxs-lookup"><span data-stu-id="8baff-185">This file specifies the verification messages to ignore in regression testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8baff-186"><strong>Salir</strong></span><span class="sxs-lookup"><span data-stu-id="8baff-186"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="8baff-187">Cierra la herramienta AccChecker.</span><span class="sxs-lookup"><span data-stu-id="8baff-187">Closes the AccChecker tool.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="8baff-188"><strong>Comprobaciones</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8baff-188"><strong>Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8baff-189"><strong>Ejecutar ahora</strong></span><span class="sxs-lookup"><span data-stu-id="8baff-189"><strong>Run Now</strong></span></span></td>
<td><span data-ttu-id="8baff-190">Ejecute las rutinas de comprobación tal y como se especifica para el destino de comprobación elegido.</span><span class="sxs-lookup"><span data-stu-id="8baff-190">Run the verification routines as specified for the chosen verification target.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8baff-191"><strong>Habilitar todo</strong></span><span class="sxs-lookup"><span data-stu-id="8baff-191"><strong>Enable All</strong></span></span></td>
<td><span data-ttu-id="8baff-192">Active todas las casillas de rutina de comprobación.</span><span class="sxs-lookup"><span data-stu-id="8baff-192">Check all verification routine check boxes.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8baff-193"><strong>Deshabilitar todo</strong></span><span class="sxs-lookup"><span data-stu-id="8baff-193"><strong>Disable All</strong></span></span></td>
<td><span data-ttu-id="8baff-194">Desactive las casillas de todas las rutinas de comprobación.</span><span class="sxs-lookup"><span data-stu-id="8baff-194">Uncheck all verification routine check boxes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8baff-195"><strong>Opciones</strong></span><span class="sxs-lookup"><span data-stu-id="8baff-195"><strong>Options</strong></span></span></td>
<td><span data-ttu-id="8baff-196"><strong>Always On superior</strong></span><span class="sxs-lookup"><span data-stu-id="8baff-196"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="8baff-197">AccChecker la ventana superior en el orden z.</span><span class="sxs-lookup"><span data-stu-id="8baff-197">Make AccChecker the topmost window in the z-order.</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="8baff-198"><strong>Ayuda</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8baff-198"><strong>Help</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8baff-199"><strong>Ayuda</strong></span><span class="sxs-lookup"><span data-stu-id="8baff-199"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="8baff-200">Mostrar información de la ayuda.</span><span class="sxs-lookup"><span data-stu-id="8baff-200">Display help information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8baff-201"><strong>Acerca de</strong></span><span class="sxs-lookup"><span data-stu-id="8baff-201"><strong>About</strong></span></span></td>
<td><span data-ttu-id="8baff-202">Muestra la versión de AccChecker y una dirección de correo electrónico para ponerse en contacto con Microsoft sobre AccChecker.</span><span class="sxs-lookup"><span data-stu-id="8baff-202">Display the AccChecker version and an email address for contacting Microsoft about AccChecker.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8baff-203">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8baff-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8baff-204">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="8baff-204">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





