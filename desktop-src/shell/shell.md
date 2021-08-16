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
ms.openlocfilehash: fe2fbaa1bad61ac9c22d36919e49cf493a26a778a8e97d69d1b200c0c62205e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857724"
---
# <a name="shell-object"></a>Objeto shell

Representa los objetos del Shell. Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell. También hay métodos para obtener otros objetos relacionados con Shell.

## <a name="members"></a>Miembros

El **objeto** Shell tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Shell** tiene estos métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></td>
<td style="text-align: left;">Agrega un archivo a la lista de uso más reciente (MRU).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto Folder de <a href="folder.md"><strong>la carpeta</strong></a> seleccionada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></td>
<td style="text-align: left;">Determina si el usuario actual puede iniciar y detener el servicio con nombre.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">En cascada todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Cascada Windows</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Ejecuta la aplicación Panel de control especificada (*.cpl). Si la aplicación ya está abierta, activará la instancia en ejecución. <br/>
<blockquote>
<p>[!Note]<br />
A Windows Vista, la mayoría Panel de control aplicaciones son elementos de Shell y no se pueden abrir con esta función. Para abrir esas Panel de control, pase el nombre canónico a control.exe. Por ejemplo:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-ejectpc.md"><strong>DesalojónPC</strong></a></td>
<td style="text-align: left;">Expulsa el equipo de su estación de acoplamiento. Esto es lo mismo que hacer clic en el <strong>menú</strong> Inicio y seleccionar <strong>Expulsar PC</strong>, si el equipo admite este comando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-explore.md"><strong>Explorar</strong></a></td>
<td style="text-align: left;">Abre una carpeta especificada en una Windows Explorer.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></td>
<td style="text-align: left;">Obtiene el valor de una directiva Internet Explorer especificada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">Muestra el <strong>cuadro de</strong> diálogo Ejecutar al usuario. Este método tiene el mismo efecto que hacer clic en <strong>el menú</strong> Inicio y seleccionar <strong>Ejecutar</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Muestra el cuadro <strong>de diálogo Resultados de la búsqueda:</strong> Equipos . El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Muestra el <strong>cuadro de diálogo Buscar: Todos los</strong> archivos . Esto es lo mismo <strong></strong> que hacer clic en el menú Inicio y, a continuación, seleccionar <strong>Buscar</strong> (o su equivalente en sistemas anteriores a Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></td>
<td style="text-align: left;">Muestra el <strong>cuadro de diálogo Buscar</strong> impresora.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></td>
<td style="text-align: left;">Recupera una configuración de Shell global.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></td>
<td style="text-align: left;">Recupera información del sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-help.md"><strong>Ayuda</strong></a></td>
<td style="text-align: left;">Muestra el Windows Centro de ayuda y soporte técnico. Este método tiene el mismo efecto que hacer clic en <strong>el menú</strong> Inicio y seleccionar Ayuda y <strong>soporte técnico.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></td>
<td style="text-align: left;">Recupera la configuración de restricción de un grupo del Registro.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></td>
<td style="text-align: left;">Devuelve un valor que indica si se está ejecutando un servicio determinado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">Minimiza todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en <strong></strong> la barra de tareas y seleccionar Minimizar todos <strong>los Windows</strong> en sistemas anteriores o hacer clic en el icono Mostrar escritorio en el área inicio rápido de la barra de tareas en Windows 2000 o Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-namespace.md"><strong>Nombres</strong></a></td>
<td style="text-align: left;">Crea y devuelve un <a href="folder.md"><strong>objeto Folder</strong></a> para la carpeta especificada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-open.md"><strong>Abierto</strong></a></td>
<td style="text-align: left;">Abre la carpeta especificada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Actualiza el contenido del <strong>menú</strong> Inicio. Se usa solo con sistemas anteriores a Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></td>
<td style="text-align: left;">Muestra el panel Búsqueda de aplicaciones.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></td>
<td style="text-align: left;">Inicia un servicio con nombre.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></td>
<td style="text-align: left;">Detiene un servicio con nombre.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">Muestra el cuadro <strong>de diálogo Propiedades de fecha</strong> y hora . Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar <strong>Ajustar fecha y hora.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></td>
<td style="text-align: left;">Realiza una operación especificada en un archivo especificado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></td>
<td style="text-align: left;">Muestra una barra del explorador.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">Muestra el <strong>cuadro de diálogo Windows</strong> cierre. Esto es lo mismo que hacer clic en <strong>el menú</strong> Inicio y seleccionar <strong>Apagar.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-suspend.md"><strong>Suspender</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Iconos de todas las ventanas del escritorio horizontalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Icono Windows horizontalmente.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Iconos de todas las ventanas en el escritorio verticalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Icono Windows verticalmente.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></td>
<td style="text-align: left;">Muestra u oculta el escritorio.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></td>
<td style="text-align: left;">Muestra el cuadro <strong>de diálogo Propiedades de la barra de</strong> tareas y del menú Inicio . Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Propiedades</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Restaura todas las ventanas de escritorio al mismo estado que tenían antes del último <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a> Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de <strong></strong> tareas y seleccionar Deshacer minimizar todos <strong>los Windows</strong> en sistemas anteriores o hacer un segundo clic en el icono Mostrar escritorio en el área inicio rápido de la barra de tareas en Windows 2000 o Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Crea y devuelve un <a href="shellwindows.md"><strong>objeto ShellWindows.</strong></a> Este objeto representa una colección de todas las ventanas abiertas que pertenecen al Shell.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-windowssecurity.md"><strong>WindowsSeguridad</strong></a></td>
<td style="text-align: left;">Muestra el <strong>cuadro Seguridad de Windows</strong> de diálogo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></td>
<td style="text-align: left;">Muestra las ventanas abiertas en una pila 3D por la que puede pasar.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propiedades

El **objeto Shell** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso          | Descripción                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Application**](shell-application.md)<br/> | Solo lectura<br/> | Contiene el objeto Application del objeto .<br/>                        |
| [**Parent**](shell-parent.md)<br/>           | Solo lectura<br/> | Obtiene un objeto que representa el elemento primario del objeto actual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
