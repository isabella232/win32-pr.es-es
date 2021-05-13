---
description: Representa un objeto en el shell.
title: Objeto IShellDispatch (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.openlocfilehash: 02fbead4b2d40a91ec6dab70f536d1ea3241ee84
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840896"
---
# <a name="ishelldispatch-object"></a><span data-ttu-id="18152-103">Objeto IShellDispatch</span><span class="sxs-lookup"><span data-stu-id="18152-103">IShellDispatch object</span></span>

<span data-ttu-id="18152-104">Representa un objeto en el shell.</span><span class="sxs-lookup"><span data-stu-id="18152-104">Represents an object in the Shell.</span></span> <span data-ttu-id="18152-105">Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell.</span><span class="sxs-lookup"><span data-stu-id="18152-105">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="18152-106">También hay métodos para obtener otros objetos relacionados con Shell.</span><span class="sxs-lookup"><span data-stu-id="18152-106">There are also methods to obtain other Shell-related objects.</span></span>

> [!Note]  
> <span data-ttu-id="18152-107">**IShellDispatch** se implementa y se accede a través del [**objeto Shell.**](shell.md)</span><span class="sxs-lookup"><span data-stu-id="18152-107">**IShellDispatch** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="18152-108">Members</span><span class="sxs-lookup"><span data-stu-id="18152-108">Members</span></span>

<span data-ttu-id="18152-109">El **objeto IShellDispatch** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="18152-109">The **IShellDispatch** object has these types of members:</span></span>

-   [<span data-ttu-id="18152-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="18152-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="18152-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="18152-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18152-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="18152-112">Methods</span></span>

<span data-ttu-id="18152-113">El **objeto IShellDispatch** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="18152-113">The **IShellDispatch** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="18152-114">Método</span><span class="sxs-lookup"><span data-stu-id="18152-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="18152-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="18152-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="18152-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-117">Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto Folder de <a href="folder.md"><strong>la carpeta</strong></a> seleccionada.</span><span class="sxs-lookup"><span data-stu-id="18152-117">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="18152-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-119">En cascada todas las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="18152-119">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="18152-120">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Ventanas en cascada</strong>.</span><span class="sxs-lookup"><span data-stu-id="18152-120">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="18152-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-122">Ejecuta la aplicación Panel de control especificada.</span><span class="sxs-lookup"><span data-stu-id="18152-122">Runs the specified Control Panel application.</span></span> <span data-ttu-id="18152-123">Si la aplicación ya está abierta, activará la instancia en ejecución.</span><span class="sxs-lookup"><span data-stu-id="18152-123">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="18152-124">Desde Windows Vista, la mayoría Panel de control aplicaciones son elementos de Shell y no se pueden abrir con esta función.</span><span class="sxs-lookup"><span data-stu-id="18152-124">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="18152-125">Para abrir esas Panel de control, pase el nombre canónico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="18152-125">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="18152-126">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="18152-126">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="18152-127"><a href="ishelldispatch-ejectpc.md"><strong>DesalojónPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-128">Expulsa el equipo de su estación de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="18152-128">Ejects the computer from its docking station.</span></span> <span data-ttu-id="18152-129">Esto es lo mismo que hacer clic en el <strong>menú</strong> Inicio y seleccionar <strong>Expulsar PC</strong>, si el equipo admite este comando.</span><span class="sxs-lookup"><span data-stu-id="18152-129">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="18152-130"><a href="ishelldispatch-explore.md"><strong>Explorar</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-130"><a href="ishelldispatch-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-131">Abre una carpeta especificada en una Explorador de Windows especificada.</span><span class="sxs-lookup"><span data-stu-id="18152-131">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="18152-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-133">Muestra el <strong>cuadro de</strong> diálogo Ejecutar al usuario.</span><span class="sxs-lookup"><span data-stu-id="18152-133">Displays the <strong>Run</strong> dialog to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="18152-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-135">Muestra el cuadro <strong>de diálogo Resultados de la búsqueda:</strong> Equipos.</span><span class="sxs-lookup"><span data-stu-id="18152-135">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="18152-136">El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="18152-136">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="18152-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-138">Muestra el <strong>cuadro de diálogo Buscar: Todos los</strong> archivos .</span><span class="sxs-lookup"><span data-stu-id="18152-138">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="18152-139">Esto es lo mismo que hacer clic en el <strong>menú</strong> Inicio y, a continuación, seleccionar <strong>Buscar.</strong></span><span class="sxs-lookup"><span data-stu-id="18152-139">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="18152-140"><a href="ishelldispatch-help.md"><strong>Ayuda</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-141">Muestra la ventana Ayuda y soporte técnico de Windows.</span><span class="sxs-lookup"><span data-stu-id="18152-141">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="18152-142">Este método tiene el mismo efecto que hacer clic en el <strong>menú</strong> Inicio y seleccionar <strong>Ayuda y soporte técnico.</strong></span><span class="sxs-lookup"><span data-stu-id="18152-142">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="18152-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-144">Minimiza todas las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="18152-144">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="18152-145">Este método tiene el mismo efecto que hacer clic con el botón derecho <strong></strong> en la barra de tareas y seleccionar Minimizar todas las <strong>ventanas</strong> en sistemas anteriores o hacer clic en el icono Mostrar escritorio de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="18152-145">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon on the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="18152-146"><a href="ishelldispatch-namespace.md"><strong>Nombres</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-146"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-147">Crea y devuelve un <a href="folder.md"><strong>objeto Folder</strong></a> para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="18152-147">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="18152-148"><a href="ishelldispatch-open.md"><strong>Abierto</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-148"><a href="ishelldispatch-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-149">Abre la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="18152-149">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="18152-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-151">Actualiza el contenido del <strong>menú</strong> Inicio.</span><span class="sxs-lookup"><span data-stu-id="18152-151">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="18152-152">Se usa solo con sistemas anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18152-152">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="18152-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-154">Muestra el <strong>cuadro de diálogo Fecha</strong> y hora .</span><span class="sxs-lookup"><span data-stu-id="18152-154">Displays the <strong>Date and Time</strong> dialog box.</span></span> <span data-ttu-id="18152-155">Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar <strong>Ajustar fecha y hora.</strong></span><span class="sxs-lookup"><span data-stu-id="18152-155">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust date/time</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="18152-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-157">Muestra el <strong>cuadro de diálogo Apagar Windows.</strong></span><span class="sxs-lookup"><span data-stu-id="18152-157">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="18152-158">Esto es lo mismo que hacer clic en <strong>el menú</strong> Inicio y seleccionar <strong>Apagar.</strong></span><span class="sxs-lookup"><span data-stu-id="18152-158">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="18152-159"><a href="ishelldispatch-suspend.md"><strong>Suspender</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="18152-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-161">Iconos de todas las ventanas en el escritorio horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="18152-161">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="18152-162">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Mostrar ventanas apiladas.</strong></span><span class="sxs-lookup"><span data-stu-id="18152-162">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows stacked</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="18152-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-164">Iconos de todas las ventanas en el escritorio verticalmente.</span><span class="sxs-lookup"><span data-stu-id="18152-164">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="18152-165">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Mostrar ventanas en paralelo.</strong></span><span class="sxs-lookup"><span data-stu-id="18152-165">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows side by side</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="18152-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-167">Muestra el cuadro <strong>de diálogo Propiedades de la barra de tareas y del menú</strong> Inicio .</span><span class="sxs-lookup"><span data-stu-id="18152-167">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="18152-168">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Propiedades</strong>.</span><span class="sxs-lookup"><span data-stu-id="18152-168">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="18152-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-170">Restaura todas las ventanas de escritorio al estado en que estaban antes del último <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-170">Restores all desktop windows to the state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="18152-171">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra <strong></strong> de tareas y seleccionar Deshacer Minimizar todas las <strong>ventanas</strong> (en sistemas anteriores) o un segundo clic en el icono Mostrar escritorio de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="18152-171">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> (on older systems) or a second clicking of the <strong>Show Desktop</strong> icon in the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="18152-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="18152-173">Crea y devuelve un <a href="shellwindows.md"><strong>objeto ShellWindows.</strong></a></span><span class="sxs-lookup"><span data-stu-id="18152-173">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="18152-174">Este objeto representa una colección de todas las ventanas abiertas que pertenecen al Shell.</span><span class="sxs-lookup"><span data-stu-id="18152-174">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="18152-175">Propiedades</span><span class="sxs-lookup"><span data-stu-id="18152-175">Properties</span></span>

<span data-ttu-id="18152-176">El **objeto IShellDispatch** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="18152-176">The **IShellDispatch** object has these properties.</span></span>



| <span data-ttu-id="18152-177">Propiedad</span><span class="sxs-lookup"><span data-stu-id="18152-177">Property</span></span>                                                     | <span data-ttu-id="18152-178">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="18152-178">Access type</span></span>          | <span data-ttu-id="18152-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="18152-179">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="18152-180">**Application**</span><span class="sxs-lookup"><span data-stu-id="18152-180">**Application**</span></span>](ishelldispatch-application.md)<br/> | <span data-ttu-id="18152-181">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="18152-181">Read-only</span></span><br/> | <span data-ttu-id="18152-182">Contiene un objeto que representa una aplicación.</span><span class="sxs-lookup"><span data-stu-id="18152-182">Contains an object that represents an application.</span></span><br/>                    |
| [<span data-ttu-id="18152-183">**Parent**</span><span class="sxs-lookup"><span data-stu-id="18152-183">**Parent**</span></span>](ishelldispatch-parent.md)<br/>           | <span data-ttu-id="18152-184">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="18152-184">Read-only</span></span><br/> | <span data-ttu-id="18152-185">Recupera un objeto que representa el elemento primario del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="18152-185">Retrieves an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="18152-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18152-186">Requirements</span></span>



| <span data-ttu-id="18152-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="18152-187">Requirement</span></span> | <span data-ttu-id="18152-188">Value</span><span class="sxs-lookup"><span data-stu-id="18152-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18152-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18152-189">Minimum supported client</span></span><br/> | <span data-ttu-id="18152-190">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="18152-190">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="18152-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18152-191">Minimum supported server</span></span><br/> | <span data-ttu-id="18152-192">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="18152-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="18152-193">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18152-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="18152-194"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="18152-194"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="18152-195">Idl</span><span class="sxs-lookup"><span data-stu-id="18152-195">IDL</span></span><br/>                      | <dl> <span data-ttu-id="18152-196"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="18152-196"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="18152-197">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="18152-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18152-198"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="18152-198"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18152-199">Consulte también</span><span class="sxs-lookup"><span data-stu-id="18152-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18152-200">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="18152-200">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="18152-201">**Objeto shell**</span><span class="sxs-lookup"><span data-stu-id="18152-201">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 
