---
description: Representa los objetos del shell. Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell. También hay métodos para obtener otros objetos relacionados con el shell.
title: 'Objeto de Shell (Shldisp.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 75fc151e-5b9e-476b-b4e5-b848917357a8
ms.openlocfilehash: 3e891278d98ca2eb51fca11054cba01947e03c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912362"
---
# <a name="shell-object"></a><span data-ttu-id="cac8b-105">Objeto de Shell</span><span class="sxs-lookup"><span data-stu-id="cac8b-105">Shell object</span></span>

<span data-ttu-id="cac8b-106">Representa los objetos del shell.</span><span class="sxs-lookup"><span data-stu-id="cac8b-106">Represents the objects in the Shell.</span></span> <span data-ttu-id="cac8b-107">Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell.</span><span class="sxs-lookup"><span data-stu-id="cac8b-107">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="cac8b-108">También hay métodos para obtener otros objetos relacionados con el shell.</span><span class="sxs-lookup"><span data-stu-id="cac8b-108">There are also methods to obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="cac8b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cac8b-109">Members</span></span>

<span data-ttu-id="cac8b-110">El objeto de **Shell** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cac8b-110">The **Shell** object has these types of members:</span></span>

-   [<span data-ttu-id="cac8b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="cac8b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="cac8b-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cac8b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cac8b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="cac8b-113">Methods</span></span>

<span data-ttu-id="cac8b-114">El objeto de **Shell** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cac8b-114">The **Shell** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="cac8b-115">Método</span><span class="sxs-lookup"><span data-stu-id="cac8b-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="cac8b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="cac8b-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-118">Agrega un archivo a la lista de elementos usados más recientemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="cac8b-118">Adds a file to the most recently used (MRU) list.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-120">Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto de <a href="folder.md"><strong>carpeta</strong></a> de la carpeta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="cac8b-120">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-122">Determina si el usuario actual puede iniciar y detener el servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="cac8b-122">Determines if the current user can start and stop the named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-124">Organiza en cascada todas las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="cac8b-124">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="cac8b-125">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>ventanas en cascada</strong>.</span><span class="sxs-lookup"><span data-stu-id="cac8b-125">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade Windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-127">Ejecuta la aplicación del panel de control (\*. cpl) especificada.</span><span class="sxs-lookup"><span data-stu-id="cac8b-127">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="cac8b-128">Si la aplicación ya está abierta, se activará la instancia en ejecución.</span><span class="sxs-lookup"><span data-stu-id="cac8b-128">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="cac8b-129">A partir de Windows Vista, la mayoría de las aplicaciones del panel de control son elementos de Shell y no se pueden abrir con esta función.</span><span class="sxs-lookup"><span data-stu-id="cac8b-129">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="cac8b-130">Para abrir esas aplicaciones del panel de control, pase el nombre canónico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="cac8b-130">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="cac8b-131">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cac8b-131">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-133">Expulsa el equipo de la estación de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="cac8b-133">Ejects the computer from its docking station.</span></span> <span data-ttu-id="cac8b-134">Esto es lo mismo que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>expulsar equipo</strong>si el equipo es compatible con este comando.</span><span class="sxs-lookup"><span data-stu-id="cac8b-134">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-135"><a href="shell-explore.md"><strong>Explorar</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-135"><a href="shell-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-136">Abre una carpeta especificada en una ventana del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="cac8b-136">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-138">Obtiene el valor de una directiva especificada de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="cac8b-138">Gets the value for a specified Internet Explorer policy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-140">Muestra el cuadro de diálogo de <strong>ejecución</strong> al usuario.</span><span class="sxs-lookup"><span data-stu-id="cac8b-140">Displays the <strong>Run</strong> dialog to the user.</span></span> <span data-ttu-id="cac8b-141">Este método tiene el mismo efecto que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>Ejecutar</strong>.</span><span class="sxs-lookup"><span data-stu-id="cac8b-141">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Run</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-143">Muestra el cuadro de diálogo resultados de la <strong>búsqueda: equipos</strong> .</span><span class="sxs-lookup"><span data-stu-id="cac8b-143">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="cac8b-144">En el cuadro de diálogo se muestra el resultado de la búsqueda de un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="cac8b-144">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-146">Muestra el cuadro de diálogo <strong>Buscar: todos los archivos</strong> .</span><span class="sxs-lookup"><span data-stu-id="cac8b-146">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="cac8b-147">Esto es lo mismo que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>Buscar</strong> (o su equivalente en sistemas anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cac8b-147">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong> (or its equivalent under systems earlier than Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-149">Muestra el cuadro de diálogo <strong>Buscar impresora</strong> .</span><span class="sxs-lookup"><span data-stu-id="cac8b-149">Displays the <strong>Find Printer</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-151">Recupera una configuración de Shell global.</span><span class="sxs-lookup"><span data-stu-id="cac8b-151">Retrieves a global Shell setting.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-153">Recupera información del sistema.</span><span class="sxs-lookup"><span data-stu-id="cac8b-153">Retrieves system information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-154"><a href="shell-help.md"><strong>Ayuda</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-154"><a href="shell-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-155">Muestra el centro de ayuda y soporte técnico de Windows.</span><span class="sxs-lookup"><span data-stu-id="cac8b-155">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="cac8b-156">Este método tiene el mismo efecto que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>ayuda y soporte técnico</strong>.</span><span class="sxs-lookup"><span data-stu-id="cac8b-156">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-158">Recupera el valor de restricción de un grupo del registro.</span><span class="sxs-lookup"><span data-stu-id="cac8b-158">Retrieves a group's restriction setting from the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-160">Devuelve un valor que indica si se está ejecutando un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="cac8b-160">Returns a value that indicates whether a particular service is running.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-162">Minimiza todas las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="cac8b-162">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="cac8b-163">Este método tiene el mismo efecto que hacer clic con el botón secundario en la barra de tareas y seleccionar <strong>minimizar todas las ventanas</strong> en sistemas antiguos o hacer clic en el icono <strong>Mostrar escritorio</strong> del área Inicio rápido de la barra de tareas de Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cac8b-163">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-164"><a href="shell-namespace.md"><strong>System.IO</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-164"><a href="shell-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-165">Crea y devuelve un objeto de <a href="folder.md"><strong>carpeta</strong></a> para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="cac8b-165">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-166"><a href="shell-open.md"><strong>Ábra</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-166"><a href="shell-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-167">Abre la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="cac8b-167">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-169">Actualiza el contenido del menú <strong>Inicio</strong> .</span><span class="sxs-lookup"><span data-stu-id="cac8b-169">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="cac8b-170">Solo se usa con sistemas anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cac8b-170">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-172">Muestra el panel de búsqueda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="cac8b-172">Displays the Apps Search pane.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-174">Inicia un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="cac8b-174">Starts a named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-176">Detiene un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="cac8b-176">Stops a named service.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-178">Muestra el cuadro de diálogo <strong>propiedades de fecha y hora</strong> .</span><span class="sxs-lookup"><span data-stu-id="cac8b-178">Displays the <strong>Date and Time Properties</strong> dialog box.</span></span> <span data-ttu-id="cac8b-179">Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar <strong>Ajustar fecha y hora</strong>.</span><span class="sxs-lookup"><span data-stu-id="cac8b-179">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust Date/Time</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-181">Realiza una operación especificada en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="cac8b-181">Performs a specified operation on a specified file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-183">Muestra una barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="cac8b-183">Displays a browser bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-185">Muestra el cuadro de diálogo <strong>cerrar Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="cac8b-185">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="cac8b-186">Esto es lo mismo que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>apagar</strong>.</span><span class="sxs-lookup"><span data-stu-id="cac8b-186">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-187"><a href="shell-suspend.md"><strong>Suspender</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-187"><a href="shell-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-189">Organiza en mosaico todas las ventanas del escritorio de forma horizontal.</span><span class="sxs-lookup"><span data-stu-id="cac8b-189">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="cac8b-190">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>mosaico de ventanas horizontalmente</strong>.</span><span class="sxs-lookup"><span data-stu-id="cac8b-190">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Horizontally</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-192">Organiza en mosaico todas las ventanas del escritorio verticalmente.</span><span class="sxs-lookup"><span data-stu-id="cac8b-192">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="cac8b-193">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>ventanas de mosaico verticalmente</strong>.</span><span class="sxs-lookup"><span data-stu-id="cac8b-193">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Vertically</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-195">Muestra u oculta el escritorio.</span><span class="sxs-lookup"><span data-stu-id="cac8b-195">Displays or hides the desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-197">Muestra el cuadro de diálogo Propiedades de la <strong>barra de tareas y del menú Inicio</strong> .</span><span class="sxs-lookup"><span data-stu-id="cac8b-197">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="cac8b-198">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>propiedades</strong>.</span><span class="sxs-lookup"><span data-stu-id="cac8b-198">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-200">Restaura todas las ventanas de escritorio al mismo estado en que se encontraban antes del último comando <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cac8b-200">Restores all desktop windows to the same state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="cac8b-201">Este método tiene el mismo efecto que hacer clic con el botón secundario en la barra de tareas y seleccionar <strong>Deshacer minimizar todas las ventanas</strong> en sistemas antiguos o hacer clic en el icono <strong>Mostrar escritorio</strong> del área Inicio rápido de la barra de tareas de Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cac8b-201">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> on older systems or a second clicking of the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-202"><a href="shell-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-202"><a href="shell-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-203">Crea y devuelve un objeto <a href="shellwindows.md"><strong>ShellWindows</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cac8b-203">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="cac8b-204">Este objeto representa una colección de todas las ventanas abiertas que pertenecen al shell.</span><span class="sxs-lookup"><span data-stu-id="cac8b-204">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cac8b-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-206">Muestra el cuadro de diálogo <strong>seguridad de Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="cac8b-206">Displays the <strong>Windows Security</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cac8b-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span><span class="sxs-lookup"><span data-stu-id="cac8b-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="cac8b-208">Muestra las ventanas abiertas en una pila 3D que se puede desplazar.</span><span class="sxs-lookup"><span data-stu-id="cac8b-208">Displays your open windows in a 3D stack that you can flip through.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="cac8b-209">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cac8b-209">Properties</span></span>

<span data-ttu-id="cac8b-210">El objeto de **Shell** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cac8b-210">The **Shell** object has these properties.</span></span>



| <span data-ttu-id="cac8b-211">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cac8b-211">Property</span></span>                                            | <span data-ttu-id="cac8b-212">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="cac8b-212">Access type</span></span>          | <span data-ttu-id="cac8b-213">Descripción</span><span class="sxs-lookup"><span data-stu-id="cac8b-213">Description</span></span>                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="cac8b-214">**Application**</span><span class="sxs-lookup"><span data-stu-id="cac8b-214">**Application**</span></span>](shell-application.md)<br/> | <span data-ttu-id="cac8b-215">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="cac8b-215">Read-only</span></span><br/> | <span data-ttu-id="cac8b-216">Contiene el objeto de aplicación del objeto.</span><span class="sxs-lookup"><span data-stu-id="cac8b-216">Contains the object's Application object.</span></span><br/>                        |
| [<span data-ttu-id="cac8b-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="cac8b-217">**Parent**</span></span>](shell-parent.md)<br/>           | <span data-ttu-id="cac8b-218">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="cac8b-218">Read-only</span></span><br/> | <span data-ttu-id="cac8b-219">Obtiene un objeto que representa el elemento primario del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="cac8b-219">Gets an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cac8b-220">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cac8b-220">Requirements</span></span>



| <span data-ttu-id="cac8b-221">Requisito</span><span class="sxs-lookup"><span data-stu-id="cac8b-221">Requirement</span></span> | <span data-ttu-id="cac8b-222">Value</span><span class="sxs-lookup"><span data-stu-id="cac8b-222">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac8b-223">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cac8b-223">Minimum supported client</span></span><br/> | <span data-ttu-id="cac8b-224">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="cac8b-224">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cac8b-225">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cac8b-225">Minimum supported server</span></span><br/> | <span data-ttu-id="cac8b-226">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cac8b-226">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cac8b-227">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cac8b-227">Header</span></span><br/>                   | <dl> <span data-ttu-id="cac8b-228"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cac8b-228"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cac8b-229">IDL</span><span class="sxs-lookup"><span data-stu-id="cac8b-229">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cac8b-230"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cac8b-230"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cac8b-231">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cac8b-231">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cac8b-232"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="cac8b-232"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
