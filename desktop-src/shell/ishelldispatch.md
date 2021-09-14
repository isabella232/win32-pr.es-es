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
ms.openlocfilehash: 322b912ad7332b0862309b0ecc1510adb3aa1a10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248073"
---
# <a name="ishelldispatch-object"></a>Objeto IShellDispatch

Representa un objeto en el shell. Se proporcionan métodos para controlar el shell y ejecutar comandos dentro del shell. También hay métodos para obtener otros objetos relacionados con Shell.

> [!Note]  
> **IShellDispatch** se implementa y se accede a través del [**objeto Shell.**](shell.md)

 

## <a name="members"></a>Members

El **objeto IShellDispatch** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto IShellDispatch** tiene estos métodos.




| Método | Descripción | 
|--------|-------------|
| <a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a> | Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto Folder de <a href="folder.md"><strong>la carpeta</strong></a> seleccionada.<br /> | 
| <a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a> | En cascada todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Ventanas en cascada</strong>.<br /> | 
| <a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a> | Ejecuta la aplicación Panel de control especificada. Si la aplicación ya está abierta, activará la instancia en ejecución. <br /><blockquote><p>[!Note]<br />A Windows Vista, la mayoría Panel de control aplicaciones son elementos de Shell y no se pueden abrir con esta función. Para abrir esas Panel de control, pase el nombre canónico a control.exe. Por ejemplo:</p><pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre></blockquote><br /> | 
| <a href="ishelldispatch-ejectpc.md"><strong>DesalojónPC</strong></a> | Expulsa el equipo de su estación de acoplamiento. Esto es lo mismo que hacer clic en el <strong>menú</strong> Inicio y seleccionar <strong>Expulsar PC</strong>si el equipo admite este comando.<br /> | 
| <a href="ishelldispatch-explore.md"><strong>Explorar</strong></a> | Abre una carpeta especificada en una ventana Windows Explorer.<br /> | 
| <a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a> | Muestra el <strong>cuadro de</strong> diálogo Ejecutar al usuario.<br /> | 
| <a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a> | Muestra el cuadro <strong>de diálogo Resultados de la búsqueda:</strong> Equipos . El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado.<br /> | 
| <a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a> | Muestra el <strong>cuadro de diálogo Buscar: Todos los</strong> archivos . Esto es lo mismo que hacer clic en el <strong>menú</strong> Inicio y, a continuación, seleccionar <strong>Buscar.</strong><br /> | 
| <a href="ishelldispatch-help.md"><strong>Ayuda</strong></a> | Muestra la Windows ayuda y soporte técnico. Este método tiene el mismo efecto que hacer clic en <strong>el menú</strong> Inicio y seleccionar Ayuda y <strong>soporte técnico.</strong><br /> | 
| <a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a> | Minimiza todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en <strong></strong> la barra de tareas y seleccionar Minimizar todos <strong>los Windows</strong> en sistemas anteriores o hacer clic en el icono Mostrar escritorio de la barra de tareas.<br /> | 
| <a href="ishelldispatch-namespace.md"><strong>Nombres</strong></a> | Crea y devuelve un <a href="folder.md"><strong>objeto Folder</strong></a> para la carpeta especificada.<br /> | 
| <a href="ishelldispatch-open.md"><strong>Abrir</strong></a> | Abre la carpeta especificada.<br /> | 
| <a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a> | Actualiza el contenido del <strong>menú</strong> Inicio. Se usa solo con sistemas anteriores a Windows XP.<br /> | 
| <a href="ishelldispatch-settime.md"><strong>SetTime</strong></a> | Muestra el <strong>cuadro de diálogo Fecha</strong> y hora . Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar <strong>Ajustar fecha y hora.</strong><br /> | 
| <a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a> | Muestra el <strong>cuadro de diálogo Windows</strong> apagado. Esto es lo mismo que hacer clic en <strong>el menú</strong> Inicio y seleccionar <strong>Apagar.</strong><br /> | 
| <a href="ishelldispatch-suspend.md"><strong>Suspender</strong></a> | Td | 
| <a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a> | Iconos de todas las ventanas en el escritorio horizontalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Mostrar ventanas apiladas.</strong><br /> | 
| <a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a> | Iconos de todas las ventanas en el escritorio verticalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Mostrar ventanas en paralelo.</strong><br /> | 
| <a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a> | Muestra el cuadro <strong>de diálogo Propiedades de la barra de tareas y del menú</strong> Inicio . Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Propiedades</strong>.<br /> | 
| <a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a> | Restaura todas las ventanas de escritorio al estado en el que estaban antes del último <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a> Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de <strong></strong> tareas y seleccionar Deshacer minimizar todo <strong>Windows</strong> (en sistemas anteriores) o un segundo clic en el icono Mostrar escritorio de la barra de tareas.<br /> | 
| <a href="ishelldispatch-windows.md"><strong>Windows</strong></a> | Crea y devuelve un <a href="shellwindows.md"><strong>objeto ShellWindows.</strong></a> Este objeto representa una colección de todas las ventanas abiertas que pertenecen al Shell.<br /> | 




 

### <a name="properties"></a>Propiedades

El **objeto IShellDispatch** tiene estas propiedades.



| Propiedad                                                     | Tipo de acceso          | Descripción                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Application**](ishelldispatch-application.md)<br/> | Solo lectura<br/> | Contiene un objeto que representa una aplicación.<br/>                    |
| [**Parent**](ishelldispatch-parent.md)<br/>           | Solo lectura<br/> | Recupera un objeto que representa el elemento primario del objeto actual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto shell**](shell.md)
</dt> </dl>

 

 
