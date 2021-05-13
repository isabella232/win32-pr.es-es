---
description: Representa los objetos del Shell. Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell. También hay métodos para obtener otros objetos relacionados con Shell.
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
ms.openlocfilehash: 55f8062b71e553ec5ceefa413b45f439874744b8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841766"
---
# <a name="shell-object"></a><span data-ttu-id="4a280-105">Objeto shell</span><span class="sxs-lookup"><span data-stu-id="4a280-105">Shell object</span></span>

<span data-ttu-id="4a280-106">Representa los objetos del Shell.</span><span class="sxs-lookup"><span data-stu-id="4a280-106">Represents the objects in the Shell.</span></span> <span data-ttu-id="4a280-107">Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell.</span><span class="sxs-lookup"><span data-stu-id="4a280-107">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="4a280-108">También hay métodos para obtener otros objetos relacionados con Shell.</span><span class="sxs-lookup"><span data-stu-id="4a280-108">There are also methods to obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="4a280-109">Members</span><span class="sxs-lookup"><span data-stu-id="4a280-109">Members</span></span>

<span data-ttu-id="4a280-110">El **objeto Shell** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4a280-110">The **Shell** object has these types of members:</span></span>

-   [<span data-ttu-id="4a280-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a280-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4a280-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a280-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4a280-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a280-113">Methods</span></span>

<span data-ttu-id="4a280-114">El **objeto Shell** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4a280-114">The **Shell** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4a280-115">Método</span><span class="sxs-lookup"><span data-stu-id="4a280-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4a280-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a280-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-118">Agrega un archivo a la lista de mru usada más recientemente.</span><span class="sxs-lookup"><span data-stu-id="4a280-118">Adds a file to the most recently used (MRU) list.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-120">Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto Folder de <a href="folder.md"><strong>la carpeta</strong></a> seleccionada.</span><span class="sxs-lookup"><span data-stu-id="4a280-120">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-122">Determina si el usuario actual puede iniciar y detener el servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="4a280-122">Determines if the current user can start and stop the named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-124">En cascada todas las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="4a280-124">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="4a280-125">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Ventanas en cascada</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a280-125">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade Windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-127">Ejecuta la aplicación Panel de control especificada (\*.cpl).</span><span class="sxs-lookup"><span data-stu-id="4a280-127">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="4a280-128">Si la aplicación ya está abierta, activará la instancia en ejecución.</span><span class="sxs-lookup"><span data-stu-id="4a280-128">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="4a280-129">Desde Windows Vista, la mayoría de Panel de control son elementos de Shell y no se pueden abrir con esta función.</span><span class="sxs-lookup"><span data-stu-id="4a280-129">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="4a280-130">Para abrir esas Panel de control, pase el nombre canónico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="4a280-130">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="4a280-131">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4a280-131">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-132"><a href="shell-ejectpc.md"><strong>DesalojónPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-133">Expulsa el equipo de su estación de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="4a280-133">Ejects the computer from its docking station.</span></span> <span data-ttu-id="4a280-134">Esto es lo mismo que hacer clic en el <strong>menú</strong> Inicio y seleccionar <strong>Expulsar PC</strong>, si el equipo admite este comando.</span><span class="sxs-lookup"><span data-stu-id="4a280-134">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-135"><a href="shell-explore.md"><strong>Explorar</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-135"><a href="shell-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-136">Abre una carpeta especificada en una Explorador de Windows especificada.</span><span class="sxs-lookup"><span data-stu-id="4a280-136">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-138">Obtiene el valor de una directiva Internet Explorer especificada.</span><span class="sxs-lookup"><span data-stu-id="4a280-138">Gets the value for a specified Internet Explorer policy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-140">Muestra el <strong>cuadro de</strong> diálogo Ejecutar al usuario.</span><span class="sxs-lookup"><span data-stu-id="4a280-140">Displays the <strong>Run</strong> dialog to the user.</span></span> <span data-ttu-id="4a280-141">Este método tiene el mismo efecto que hacer clic en <strong>el menú</strong> Inicio y seleccionar <strong>Ejecutar</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a280-141">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Run</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-143">Muestra el cuadro <strong>de diálogo Resultados de la búsqueda:</strong> Equipos.</span><span class="sxs-lookup"><span data-stu-id="4a280-143">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="4a280-144">El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="4a280-144">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-146">Muestra el <strong>cuadro de diálogo Buscar: Todos los</strong> archivos .</span><span class="sxs-lookup"><span data-stu-id="4a280-146">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="4a280-147">Esto es lo mismo que hacer clic en el <strong>menú</strong> Inicio y, a continuación, seleccionar <strong>Buscar</strong> (o su equivalente en sistemas anteriores a Windows XP).</span><span class="sxs-lookup"><span data-stu-id="4a280-147">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong> (or its equivalent under systems earlier than Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-149">Muestra el <strong>cuadro de diálogo Buscar</strong> impresora.</span><span class="sxs-lookup"><span data-stu-id="4a280-149">Displays the <strong>Find Printer</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-151">Recupera una configuración de Shell global.</span><span class="sxs-lookup"><span data-stu-id="4a280-151">Retrieves a global Shell setting.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-153">Recupera información del sistema.</span><span class="sxs-lookup"><span data-stu-id="4a280-153">Retrieves system information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-154"><a href="shell-help.md"><strong>Ayuda</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-154"><a href="shell-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-155">Muestra la ventana de Windows Centro de ayuda y soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="4a280-155">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="4a280-156">Este método tiene el mismo efecto que hacer clic en <strong>el menú</strong> Inicio y seleccionar Ayuda y <strong>soporte técnico.</strong></span><span class="sxs-lookup"><span data-stu-id="4a280-156">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-158">Recupera la configuración de restricción de un grupo del Registro.</span><span class="sxs-lookup"><span data-stu-id="4a280-158">Retrieves a group's restriction setting from the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-160">Devuelve un valor que indica si se está ejecutando un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="4a280-160">Returns a value that indicates whether a particular service is running.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-162">Minimiza todas las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="4a280-162">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="4a280-163">Este método tiene el mismo efecto que hacer clic con el botón derecho <strong></strong> en la barra de tareas y seleccionar Minimizar todas las <strong>ventanas</strong> en sistemas anteriores o hacer clic en el icono Mostrar escritorio en el área inicio rápido de la barra de tareas en Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a280-163">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-164"><a href="shell-namespace.md"><strong>Nombres</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-164"><a href="shell-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-165">Crea y devuelve un <a href="folder.md"><strong>objeto Folder</strong></a> para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="4a280-165">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-166"><a href="shell-open.md"><strong>Abierto</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-166"><a href="shell-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-167">Abre la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="4a280-167">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-169">Actualiza el contenido del <strong>menú</strong> Inicio.</span><span class="sxs-lookup"><span data-stu-id="4a280-169">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="4a280-170">Se usa solo con sistemas anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a280-170">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-172">Muestra el panel Búsqueda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4a280-172">Displays the Apps Search pane.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-174">Inicia un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="4a280-174">Starts a named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-176">Detiene un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="4a280-176">Stops a named service.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-178">Muestra el cuadro <strong>de diálogo Propiedades de fecha</strong> y hora .</span><span class="sxs-lookup"><span data-stu-id="4a280-178">Displays the <strong>Date and Time Properties</strong> dialog box.</span></span> <span data-ttu-id="4a280-179">Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar <strong>Ajustar fecha y hora.</strong></span><span class="sxs-lookup"><span data-stu-id="4a280-179">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust Date/Time</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-181">Realiza una operación especificada en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="4a280-181">Performs a specified operation on a specified file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-183">Muestra una barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="4a280-183">Displays a browser bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-185">Muestra el <strong>cuadro de diálogo Apagar Windows.</strong></span><span class="sxs-lookup"><span data-stu-id="4a280-185">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="4a280-186">Esto es lo mismo que hacer clic en <strong>el menú</strong> Inicio y seleccionar <strong>Apagar.</strong></span><span class="sxs-lookup"><span data-stu-id="4a280-186">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-187"><a href="shell-suspend.md"><strong>Suspender</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-187"><a href="shell-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-189">Iconos de todas las ventanas del escritorio horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="4a280-189">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="4a280-190">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Mosaico de Windows horizontalmente.</strong></span><span class="sxs-lookup"><span data-stu-id="4a280-190">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Horizontally</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-192">Iconos de todas las ventanas en el escritorio verticalmente.</span><span class="sxs-lookup"><span data-stu-id="4a280-192">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="4a280-193">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Icono de Windows verticalmente.</strong></span><span class="sxs-lookup"><span data-stu-id="4a280-193">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Vertically</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-195">Muestra u oculta el escritorio.</span><span class="sxs-lookup"><span data-stu-id="4a280-195">Displays or hides the desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-197">Muestra el cuadro <strong>de diálogo Propiedades de la barra de tareas y del menú</strong> Inicio .</span><span class="sxs-lookup"><span data-stu-id="4a280-197">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="4a280-198">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Propiedades</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a280-198">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-200">Restaura todas las ventanas de escritorio al mismo estado en que estaban antes del último <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-200">Restores all desktop windows to the same state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="4a280-201">Este método tiene el mismo efecto que hacer clic con el botón derecho en la <strong></strong> barra de tareas y seleccionar Deshacer Minimizar todas las <strong>ventanas</strong> en sistemas anteriores o un segundo clic en el icono Mostrar escritorio en el área inicio rápido de la barra de tareas en Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a280-201">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> on older systems or a second clicking of the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-202"><a href="shell-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-202"><a href="shell-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-203">Crea y devuelve un <a href="shellwindows.md"><strong>objeto ShellWindows.</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-203">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="4a280-204">Este objeto representa una colección de todas las ventanas abiertas que pertenecen al Shell.</span><span class="sxs-lookup"><span data-stu-id="4a280-204">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a280-205"><a href="shell-windowssecurity.md"><strong>WindowsSeguridad</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-206">Muestra el <strong>cuadro Seguridad de Windows</strong> de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4a280-206">Displays the <strong>Windows Security</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a280-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a280-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a280-208">Muestra las ventanas abiertas en una pila 3D por la que puede pasar.</span><span class="sxs-lookup"><span data-stu-id="4a280-208">Displays your open windows in a 3D stack that you can flip through.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="4a280-209">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a280-209">Properties</span></span>

<span data-ttu-id="4a280-210">El **objeto Shell** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4a280-210">The **Shell** object has these properties.</span></span>



| <span data-ttu-id="4a280-211">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a280-211">Property</span></span>                                            | <span data-ttu-id="4a280-212">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="4a280-212">Access type</span></span>          | <span data-ttu-id="4a280-213">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a280-213">Description</span></span>                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="4a280-214">**Application**</span><span class="sxs-lookup"><span data-stu-id="4a280-214">**Application**</span></span>](shell-application.md)<br/> | <span data-ttu-id="4a280-215">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a280-215">Read-only</span></span><br/> | <span data-ttu-id="4a280-216">Contiene el objeto Application del objeto .</span><span class="sxs-lookup"><span data-stu-id="4a280-216">Contains the object's Application object.</span></span><br/>                        |
| [<span data-ttu-id="4a280-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="4a280-217">**Parent**</span></span>](shell-parent.md)<br/>           | <span data-ttu-id="4a280-218">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a280-218">Read-only</span></span><br/> | <span data-ttu-id="4a280-219">Obtiene un objeto que representa el elemento primario del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="4a280-219">Gets an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4a280-220">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a280-220">Requirements</span></span>



| <span data-ttu-id="4a280-221">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a280-221">Requirement</span></span> | <span data-ttu-id="4a280-222">Value</span><span class="sxs-lookup"><span data-stu-id="4a280-222">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a280-223">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a280-223">Minimum supported client</span></span><br/> | <span data-ttu-id="4a280-224">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="4a280-224">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4a280-225">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a280-225">Minimum supported server</span></span><br/> | <span data-ttu-id="4a280-226">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4a280-226">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4a280-227">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a280-227">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a280-228"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="4a280-228"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4a280-229">Idl</span><span class="sxs-lookup"><span data-stu-id="4a280-229">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a280-230"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a280-230"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4a280-231">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a280-231">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a280-232"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4a280-232"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
