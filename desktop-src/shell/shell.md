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
ms.openlocfilehash: d31adcbf5a12d699750029c15a308ef73f4d8c03
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467232"
---
# <a name="shell-object"></a>Objeto shell

Representa los objetos del Shell. Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell. También hay métodos para obtener otros objetos relacionados con Shell.

## <a name="members"></a>Miembros

El **objeto Shell** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Shell** tiene estos métodos.




| Método | Descripción | 
|--------|-------------|
| <a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a> | Agrega un archivo a la lista de mru usada más recientemente.<br /> | 
| <a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a> | Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto Folder de <a href="folder.md"><strong>la carpeta</strong></a> seleccionada.<br /> | 
| <a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a> | Determina si el usuario actual puede iniciar y detener el servicio con nombre.<br /> | 
| <a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a> | En cascada todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Cascade Windows</strong>.<br /> | 
| <a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a> | Ejecuta la aplicación Panel de control especificada (*.cpl). Si la aplicación ya está abierta, activará la instancia en ejecución. <br /><blockquote><p>[!Note]<br />A Windows Vista, la mayoría Panel de control aplicaciones son elementos de Shell y no se pueden abrir con esta función. Para abrir esas Panel de control, pase el nombre canónico a control.exe. Por ejemplo:</p><pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre></blockquote><br /> | 
| <a href="shell-ejectpc.md"><strong>DesalojónPC</strong></a> | Expulsa el equipo de su estación de acoplamiento. Esto es lo mismo que hacer clic en el <strong>menú</strong> Inicio y seleccionar <strong>Expulsar PC</strong>si el equipo admite este comando.<br /> | 
| <a href="shell-explore.md"><strong>Explorar</strong></a> | Abre una carpeta especificada en una ventana Windows Explorador.<br /> | 
| <a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a> | Obtiene el valor de una directiva Internet Explorer especificada.<br /> | 
| <a href="shell-filerun.md"><strong>FileRun</strong></a> | Muestra el <strong>cuadro de</strong> diálogo Ejecutar al usuario. Este método tiene el mismo efecto que hacer clic en <strong>el menú</strong> Inicio y seleccionar <strong>Ejecutar</strong>.<br /> | 
| <a href="shell-findcomputer.md"><strong>FindComputer</strong></a> | Muestra el cuadro <strong>de diálogo Resultados de la búsqueda:</strong> Equipos . El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado.<br /> | 
| <a href="shell-findfiles.md"><strong>FindFiles</strong></a> | Muestra el <strong>cuadro de diálogo Buscar: Todos los</strong> archivos . Esto es lo mismo <strong></strong> que hacer clic en el menú Inicio y, a continuación, seleccionar <strong>Buscar</strong> (o su equivalente en sistemas anteriores a Windows XP.<br /> | 
| <a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a> | Muestra el <strong>cuadro de diálogo Buscar</strong> impresora.<br /> | 
| <a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a> | Recupera una configuración de Shell global.<br /> | 
| <a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a> | Recupera información del sistema.<br /> | 
| <a href="shell-help.md"><strong>Ayuda</strong></a> | Muestra el Windows Centro de ayuda y soporte técnico. Este método tiene el mismo efecto que hacer clic en <strong>el menú</strong> Inicio y seleccionar Ayuda y <strong>soporte técnico.</strong><br /> | 
| <a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a> | Recupera la configuración de restricción de un grupo del Registro.<br /> | 
| <a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a> | Devuelve un valor que indica si se está ejecutando un servicio determinado.<br /> | 
| <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> | Minimiza todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en <strong></strong> la barra de tareas y seleccionar Minimizar todos <strong>los Windows</strong> en sistemas anteriores o hacer clic en el icono Mostrar escritorio en el área inicio rápido de la barra de tareas en Windows 2000 o Windows XP.<br /> | 
| <a href="shell-namespace.md"><strong>Nombres</strong></a> | Crea y devuelve un <a href="folder.md"><strong>objeto Folder</strong></a> para la carpeta especificada.<br /> | 
| <a href="shell-open.md"><strong>Abierto</strong></a> | Abre la carpeta especificada.<br /> | 
| <a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a> | Actualiza el contenido del <strong>menú</strong> Inicio. Se usa solo con sistemas anteriores a Windows XP.<br /> | 
| <a href="shell-searchcommand.md"><strong>SearchCommand</strong></a> | Muestra el panel Búsqueda de aplicaciones.<br /> | 
| <a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a> | Inicia un servicio con nombre.<br /> | 
| <a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a> | Detiene un servicio con nombre.<br /> | 
| <a href="shell-settime.md"><strong>SetTime</strong></a> | Muestra el cuadro <strong>de diálogo Propiedades de fecha</strong> y hora . Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar <strong>Ajustar fecha y hora.</strong><br /> | 
| <a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a> | Realiza una operación especificada en un archivo especificado.<br /> | 
| <a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a> | Muestra una barra del explorador.<br /> | 
| <a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a> | Muestra el <strong>cuadro de diálogo Cerrar Windows</strong> cierre. Esto es lo mismo que hacer clic en <strong>el menú</strong> Inicio y seleccionar <strong>Apagar.</strong><br /> | 
| <a href="shell-suspend.md"><strong>Suspender</strong></a> | Td | 
| <a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a> | Iconos de todas las ventanas en el escritorio horizontalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Icono Windows horizontalmente.</strong><br /> | 
| <a href="shell-tilevertically.md"><strong>TileVertically</strong></a> | Iconos de todas las ventanas en el escritorio verticalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Icono Windows verticalmente.</strong><br /> | 
| <a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a> | Muestra u oculta el escritorio.<br /> | 
| <a href="shell-trayproperties.md"><strong>TrayProperties</strong></a> | Muestra el cuadro <strong>de diálogo Propiedades de la barra de tareas y del menú</strong> Inicio . Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Propiedades</strong>.<br /> | 
| <a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a> | Restaura todas las ventanas de escritorio al mismo estado que tenían antes del último <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a> Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de <strong></strong> tareas y seleccionar Deshacer Minimizar todos <strong>los Windows</strong> en sistemas anteriores o un segundo clic en el icono Mostrar escritorio en el área inicio rápido de la barra de tareas en Windows 2000 o Windows XP.<br /> | 
| <a href="shell-windows.md"><strong>Windows</strong></a> | Crea y devuelve un <a href="shellwindows.md"><strong>objeto ShellWindows.</strong></a> Este objeto representa una colección de todas las ventanas abiertas que pertenecen al Shell.<br /> | 
| <a href="shell-windowssecurity.md"><strong>WindowsSeguridad</strong></a> | Muestra el <strong>Seguridad de Windows</strong> de diálogo.<br /> | 
| <a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a> | Muestra las ventanas abiertas en una pila 3D por la que puede cambiar.<br /> | 




 

### <a name="properties"></a>Propiedades

El **objeto Shell** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso          | Descripción                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Application**](shell-application.md)<br/> | Solo lectura<br/> | Contiene el objeto Application del objeto .<br/>                        |
| [**Parent**](shell-parent.md)<br/>           | Solo lectura<br/> | Obtiene un objeto que representa el elemento primario del objeto actual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones de \[ escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
