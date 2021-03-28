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
# <a name="ishelldispatch-object"></a>Objeto IShellDispatch

Representa un objeto en el shell. Se proporcionan métodos para controlar el Shell y ejecutar comandos dentro del shell. También hay métodos para obtener otros objetos relacionados con el shell.

> [!Note]  
> **IShellDispatch** se implementa y se obtiene acceso a él a través del objeto de [**Shell**](shell.md) .

 

## <a name="members"></a>Miembros

El objeto **IShellDispatch** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **IShellDispatch** tiene estos métodos.



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
<td style="text-align: left;"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">Crea un cuadro de diálogo que permite al usuario seleccionar una carpeta y, a continuación, devuelve el objeto de <a href="folder.md"><strong>carpeta</strong></a> de la carpeta seleccionada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">Organiza en cascada todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>ventanas en cascada</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Ejecuta la aplicación del panel de control especificada. Si la aplicación ya está abierta, se activará la instancia en ejecución. <br/>
<blockquote>
<p>[!Note]<br />
A partir de Windows Vista, la mayoría de las aplicaciones del panel de control son elementos de Shell y no se pueden abrir con esta función. Para abrir esas aplicaciones del panel de control, pase el nombre canónico a control.exe. Por ejemplo:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">Expulsa el equipo de la estación de acoplamiento. Esto es lo mismo que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>expulsar equipo</strong>si el equipo es compatible con este comando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-explore.md"><strong>Explorar</strong></a></td>
<td style="text-align: left;">Abre una carpeta especificada en una ventana del explorador de Windows.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">Muestra el cuadro de diálogo de <strong>ejecución</strong> al usuario.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Muestra el cuadro de diálogo resultados de la <strong>búsqueda: equipos</strong> . En el cuadro de diálogo se muestra el resultado de la búsqueda de un equipo especificado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Muestra el cuadro de diálogo <strong>Buscar: todos los archivos</strong> . Esto es lo mismo que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>Buscar</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-help.md"><strong>Ayuda</strong></a></td>
<td style="text-align: left;">Muestra la ventana de ayuda y soporte técnico de Windows. Este método tiene el mismo efecto que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>ayuda y soporte técnico</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">Minimiza todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>minimizar todas las ventanas</strong> en sistemas antiguos o hacer clic en el icono <strong>Mostrar escritorio</strong> en la barra de tareas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-namespace.md"><strong>System.IO</strong></a></td>
<td style="text-align: left;">Crea y devuelve un objeto de <a href="folder.md"><strong>carpeta</strong></a> para la carpeta especificada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-open.md"><strong>Ábra</strong></a></td>
<td style="text-align: left;">Abre la carpeta especificada.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Actualiza el contenido del menú <strong>Inicio</strong> . Solo se usa con sistemas anteriores a Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">Muestra el cuadro de diálogo <strong>fecha y hora</strong> . Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar <strong>Ajustar fecha y hora</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">Muestra el cuadro de diálogo <strong>cerrar Windows</strong> . Esto es lo mismo que hacer clic en el menú <strong>Inicio</strong> y seleccionar <strong>apagar</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-suspend.md"><strong>Suspender</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Organiza en mosaico todas las ventanas del escritorio de forma horizontal. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Mostrar ventanas apiladas</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Organiza en mosaico todas las ventanas del escritorio verticalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Mostrar ventanas en paralelo</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></td>
<td style="text-align: left;">Muestra el cuadro de diálogo Propiedades de la <strong>barra de tareas y del menú Inicio</strong> . Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>propiedades</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Restaura todas las ventanas de escritorio al estado en que se encontraban antes del último comando <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> . Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar <strong>Deshacer minimizar todas las ventanas</strong> (en sistemas anteriores) o hacer clic en el icono <strong>Mostrar escritorio</strong> en la barra de tareas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Crea y devuelve un objeto <a href="shellwindows.md"><strong>ShellWindows</strong></a> . Este objeto representa una colección de todas las ventanas abiertas que pertenecen al shell.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propiedades

El objeto **IShellDispatch** tiene estas propiedades.



| Propiedad                                                     | Tipo de acceso          | Descripción                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Application**](ishelldispatch-application.md)<br/> | Solo lectura<br/> | Contiene un objeto que representa una aplicación.<br/>                    |
| [**Parent**](ishelldispatch-parent.md)<br/>           | Solo lectura<br/> | Recupera un objeto que representa el elemento primario del objeto actual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto de Shell**](shell.md)
</dt> </dl>

 

 
