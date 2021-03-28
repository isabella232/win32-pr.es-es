---
description: Representa un objeto en el shell.
title: Objeto IShellDispatch (Shldisp. h)
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
ms.openlocfilehash: 20c6cc9f0b3a2e2fde8f56311564d63bc1cc9c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984698"
---
# <a name="ishelldispatch-object"></a><span data-ttu-id="f8a61-103">Objeto IShellDispatch</span><span class="sxs-lookup"><span data-stu-id="f8a61-103">IShellDispatch object</span></span>

<span data-ttu-id="f8a61-104">Representa un objeto en el shell.</span><span class="sxs-lookup"><span data-stu-id="f8a61-104">Represents an object in the Shell.</span></span> <span data-ttu-id="f8a61-105">Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell.</span><span class="sxs-lookup"><span data-stu-id="f8a61-105">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="f8a61-106">También hay métodos para obtener otros objetos relacionados con el shell.</span><span class="sxs-lookup"><span data-stu-id="f8a61-106">There are also methods to obtain other Shell-related objects.</span></span>

> [!Note]  
> <span data-ttu-id="f8a61-107">**IShellDispatch** se implementa y se obtiene acceso a él a través del objeto de [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="f8a61-107">**IShellDispatch** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="f8a61-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f8a61-108">Members</span></span>

<span data-ttu-id="f8a61-109">El objeto **IShellDispatch** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f8a61-109">The **IShellDispatch** object has these types of members:</span></span>

-   [<span data-ttu-id="f8a61-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="f8a61-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f8a61-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f8a61-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f8a61-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f8a61-112">Methods</span></span>

<span data-ttu-id="f8a61-113">El objeto **IShellDispatch** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f8a61-113">The **IShellDispatch** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f8a61-114">Método</span><span class="sxs-lookup"><span data-stu-id="f8a61-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f8a61-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8a61-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f8a61-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-117">Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto de <a href="folder.md"><strong>carpeta</strong></a> de la carpeta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="f8a61-117">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f8a61-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-119">Organiza en cascada todas las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="f8a61-119">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="f8a61-120">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>ventanas en cascada</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8a61-120">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f8a61-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-122">Ejecuta la aplicación del panel de control especificada.</span><span class="sxs-lookup"><span data-stu-id="f8a61-122">Runs the specified Control Panel application.</span></span> <span data-ttu-id="f8a61-123">Si la aplicación ya está abierta, se activará la instancia en ejecución.</span><span class="sxs-lookup"><span data-stu-id="f8a61-123">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="f8a61-124">A partir de Windows Vista, la mayoría de las aplicaciones del panel de control son elementos de Shell y no se pueden abrir con esta función.</span><span class="sxs-lookup"><span data-stu-id="f8a61-124">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="f8a61-125">Para abrir esas aplicaciones del panel de control, pase el nombre canónico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="f8a61-125">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="f8a61-126">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f8a61-126">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f8a61-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-128">Expulsa el equipo de la estación de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="f8a61-128">Ejects the computer from its docking station.</span></span> <span data-ttu-id="f8a61-129">Esto es lo mismo que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>expulsar equipo</strong>si el equipo es compatible con este comando.</span><span class="sxs-lookup"><span data-stu-id="f8a61-129">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f8a61-130"><a href="ishelldispatch-explore.md"><strong>Explorar</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-130"><a href="ishelldispatch-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-131">Abre una carpeta especificada en una ventana del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="f8a61-131">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f8a61-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-133">Muestra el cuadro de diálogo de <strong>ejecución</strong> al usuario.</span><span class="sxs-lookup"><span data-stu-id="f8a61-133">Displays the <strong>Run</strong> dialog to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f8a61-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-135">Muestra el cuadro de diálogo resultados de la <strong>búsqueda: equipos</strong> .</span><span class="sxs-lookup"><span data-stu-id="f8a61-135">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="f8a61-136">En el cuadro de diálogo se muestra el resultado de la búsqueda de un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="f8a61-136">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f8a61-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-138">Muestra el cuadro de diálogo <strong>Buscar: todos los archivos</strong> .</span><span class="sxs-lookup"><span data-stu-id="f8a61-138">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="f8a61-139">Esto es lo mismo que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>Buscar</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8a61-139">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f8a61-140"><a href="ishelldispatch-help.md"><strong>Ayuda</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-141">Muestra la ventana de ayuda y soporte técnico de Windows.</span><span class="sxs-lookup"><span data-stu-id="f8a61-141">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="f8a61-142">Este método tiene el mismo efecto que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>ayuda y soporte técnico</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8a61-142">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f8a61-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-144">Minimiza todas las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="f8a61-144">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="f8a61-145">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>minimizar todas las ventanas</strong> en sistemas antiguos o hacer clic en el icono <strong>Mostrar escritorio</strong> en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="f8a61-145">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon on the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f8a61-146"><a href="ishelldispatch-namespace.md"><strong>System.IO</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-146"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-147">Crea y devuelve un objeto de <a href="folder.md"><strong>carpeta</strong></a> para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="f8a61-147">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f8a61-148"><a href="ishelldispatch-open.md"><strong>Ábra</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-148"><a href="ishelldispatch-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-149">Abre la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="f8a61-149">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f8a61-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-151">Actualiza el contenido del menú <strong>Inicio</strong> .</span><span class="sxs-lookup"><span data-stu-id="f8a61-151">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="f8a61-152">Solo se usa con sistemas anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f8a61-152">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f8a61-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-154">Muestra el cuadro de diálogo <strong>fecha y hora</strong> .</span><span class="sxs-lookup"><span data-stu-id="f8a61-154">Displays the <strong>Date and Time</strong> dialog box.</span></span> <span data-ttu-id="f8a61-155">Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar <strong>Ajustar fecha y hora</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8a61-155">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust date/time</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f8a61-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-157">Muestra el cuadro de diálogo <strong>cerrar Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="f8a61-157">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="f8a61-158">Esto es lo mismo que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>apagar</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8a61-158">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f8a61-159"><a href="ishelldispatch-suspend.md"><strong>Suspender</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f8a61-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-161">Organiza en mosaico todas las ventanas del escritorio de forma horizontal.</span><span class="sxs-lookup"><span data-stu-id="f8a61-161">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="f8a61-162">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Mostrar ventanas apiladas</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8a61-162">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows stacked</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f8a61-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-164">Organiza en mosaico todas las ventanas del escritorio verticalmente.</span><span class="sxs-lookup"><span data-stu-id="f8a61-164">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="f8a61-165">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Mostrar ventanas en paralelo</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8a61-165">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows side by side</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f8a61-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-167">Muestra el cuadro de diálogo Propiedades de la <strong>barra de tareas y del menú Inicio</strong> .</span><span class="sxs-lookup"><span data-stu-id="f8a61-167">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="f8a61-168">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>propiedades</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8a61-168">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="f8a61-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-170">Restaura todas las ventanas de escritorio al estado en que se encontraban antes del último comando <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f8a61-170">Restores all desktop windows to the state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="f8a61-171">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Deshacer minimizar todas las ventanas</strong> (en sistemas anteriores) o hacer clic en el icono <strong>Mostrar escritorio</strong> en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="f8a61-171">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> (on older systems) or a second clicking of the <strong>Show Desktop</strong> icon in the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="f8a61-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="f8a61-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="f8a61-173">Crea y devuelve un objeto <a href="shellwindows.md"><strong>ShellWindows</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f8a61-173">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="f8a61-174">Este objeto representa una colección de todas las ventanas abiertas que pertenecen al shell.</span><span class="sxs-lookup"><span data-stu-id="f8a61-174">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="f8a61-175">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f8a61-175">Properties</span></span>

<span data-ttu-id="f8a61-176">El objeto **IShellDispatch** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f8a61-176">The **IShellDispatch** object has these properties.</span></span>



| <span data-ttu-id="f8a61-177">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f8a61-177">Property</span></span>                                                     | <span data-ttu-id="f8a61-178">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="f8a61-178">Access type</span></span>          | <span data-ttu-id="f8a61-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8a61-179">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="f8a61-180">**Application**</span><span class="sxs-lookup"><span data-stu-id="f8a61-180">**Application**</span></span>](ishelldispatch-application.md)<br/> | <span data-ttu-id="f8a61-181">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f8a61-181">Read-only</span></span><br/> | <span data-ttu-id="f8a61-182">Contiene un objeto que representa una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8a61-182">Contains an object that represents an application.</span></span><br/>                    |
| [<span data-ttu-id="f8a61-183">**Parent**</span><span class="sxs-lookup"><span data-stu-id="f8a61-183">**Parent**</span></span>](ishelldispatch-parent.md)<br/>           | <span data-ttu-id="f8a61-184">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f8a61-184">Read-only</span></span><br/> | <span data-ttu-id="f8a61-185">Recupera un objeto que representa el elemento primario del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="f8a61-185">Retrieves an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f8a61-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8a61-186">Requirements</span></span>



| <span data-ttu-id="f8a61-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8a61-187">Requirement</span></span> | <span data-ttu-id="f8a61-188">Value</span><span class="sxs-lookup"><span data-stu-id="f8a61-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a61-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8a61-189">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a61-190">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f8a61-190">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f8a61-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8a61-191">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a61-192">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f8a61-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f8a61-193">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8a61-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8a61-194"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8a61-194"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f8a61-195">IDL</span><span class="sxs-lookup"><span data-stu-id="f8a61-195">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f8a61-196"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f8a61-196"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f8a61-197">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8a61-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8a61-198"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f8a61-198"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8a61-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8a61-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a61-200">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="f8a61-200">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="f8a61-201">**Objeto de Shell**</span><span class="sxs-lookup"><span data-stu-id="f8a61-201">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 
