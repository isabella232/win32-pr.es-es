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
# <a name="shell-object"></a>Objeto de Shell

Representa los objetos del shell. Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell. También hay métodos para obtener otros objetos relacionados con el shell.

## <a name="members"></a>Members

El objeto de **Shell** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **Shell** tiene estos métodos.



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
<td style="text-align: left;">Agrega un archivo a la lista de elementos usados más recientemente (MRU).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto de <a href="folder.md"><strong>carpeta</strong></a> de la carpeta seleccionada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></td>
<td style="text-align: left;">Determina si el usuario actual puede iniciar y detener el servicio con nombre.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">Organiza en cascada todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>ventanas en cascada</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Ejecuta la aplicación del panel de control (*. cpl) especificada. Si la aplicación ya está abierta, se activará la instancia en ejecución. <br/>
<blockquote>
<p>[!Note]<br />
A partir de Windows Vista, la mayoría de las aplicaciones del panel de control son elementos de Shell y no se pueden abrir con esta función. Para abrir esas aplicaciones del panel de control, pase el nombre canónico a control.exe. Por ejemplo:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">Expulsa el equipo de la estación de acoplamiento. Esto es lo mismo que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>expulsar equipo</strong>si el equipo es compatible con este comando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-explore.md"><strong>Explorar</strong></a></td>
<td style="text-align: left;">Abre una carpeta especificada en una ventana del explorador de Windows.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></td>
<td style="text-align: left;">Obtiene el valor de una directiva especificada de Internet Explorer.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">Muestra el cuadro de diálogo de <strong>ejecución</strong> al usuario. Este método tiene el mismo efecto que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>Ejecutar</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Muestra el cuadro de diálogo resultados de la <strong>búsqueda: equipos</strong> . En el cuadro de diálogo se muestra el resultado de la búsqueda de un equipo especificado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Muestra el cuadro de diálogo <strong>Buscar: todos los archivos</strong> . Esto es lo mismo que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>Buscar</strong> (o su equivalente en sistemas anteriores a Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></td>
<td style="text-align: left;">Muestra el cuadro de diálogo <strong>Buscar impresora</strong> .<br/></td>
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
<td style="text-align: left;">Muestra el centro de ayuda y soporte técnico de Windows. Este método tiene el mismo efecto que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>ayuda y soporte técnico</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></td>
<td style="text-align: left;">Recupera el valor de restricción de un grupo del registro.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></td>
<td style="text-align: left;">Devuelve un valor que indica si se está ejecutando un servicio determinado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">Minimiza todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón secundario en la barra de tareas y seleccionar <strong>minimizar todas las ventanas</strong> en sistemas antiguos o hacer clic en el icono <strong>Mostrar escritorio</strong> del área Inicio rápido de la barra de tareas de Windows 2000 o Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-namespace.md"><strong>System.IO</strong></a></td>
<td style="text-align: left;">Crea y devuelve un objeto de <a href="folder.md"><strong>carpeta</strong></a> para la carpeta especificada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-open.md"><strong>Abrir</strong></a></td>
<td style="text-align: left;">Abre la carpeta especificada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Actualiza el contenido del menú <strong>Inicio</strong> . Solo se usa con sistemas anteriores a Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></td>
<td style="text-align: left;">Muestra el panel de búsqueda de aplicaciones.<br/></td>
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
<td style="text-align: left;">Muestra el cuadro de diálogo <strong>propiedades de fecha y hora</strong> . Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar <strong>Ajustar fecha y hora</strong>.<br/></td>
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
<td style="text-align: left;">Muestra el cuadro de diálogo <strong>cerrar Windows</strong> . Esto es lo mismo que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>apagar</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-suspend.md"><strong>Suspender</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Organiza en mosaico todas las ventanas del escritorio de forma horizontal. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>mosaico de ventanas horizontalmente</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Organiza en mosaico todas las ventanas del escritorio verticalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>ventanas de mosaico verticalmente</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></td>
<td style="text-align: left;">Muestra u oculta el escritorio.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></td>
<td style="text-align: left;">Muestra el cuadro de diálogo Propiedades de la <strong>barra de tareas y del menú Inicio</strong> . Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>propiedades</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Restaura todas las ventanas de escritorio al mismo estado en que se encontraban antes del último comando <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> . Este método tiene el mismo efecto que hacer clic con el botón secundario en la barra de tareas y seleccionar <strong>Deshacer minimizar todas las ventanas</strong> en sistemas antiguos o hacer clic en el icono <strong>Mostrar escritorio</strong> del área Inicio rápido de la barra de tareas de Windows 2000 o Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Crea y devuelve un objeto <a href="shellwindows.md"><strong>ShellWindows</strong></a> . Este objeto representa una colección de todas las ventanas abiertas que pertenecen al shell.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></td>
<td style="text-align: left;">Muestra el cuadro de diálogo <strong>seguridad de Windows</strong> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></td>
<td style="text-align: left;">Muestra las ventanas abiertas en una pila 3D que se puede desplazar.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propiedades

El objeto de **Shell** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso          | Descripción                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Application**](shell-application.md)<br/> | Solo lectura<br/> | Contiene el objeto de aplicación del objeto.<br/>                        |
| [**Parent**](shell-parent.md)<br/>           | Solo lectura<br/> | Obtiene un objeto que representa el elemento primario del objeto actual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 
