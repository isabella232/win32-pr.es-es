---
description: Un control ControlEvent especifica una acción que debe realizar el instalador o un cambio en los atributos de uno o varios controles de un cuadro de diálogo. Para obtener más información sobre ControlEvents, vea Información general de ControlEvent.
ms.assetid: 8768acaa-884b-428f-a14e-3f39f8ea4ad5
title: Eventos de control (Windows instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd72e93da7ed84c845b5993b2a021119c861b682ab5eb4645c69c723b17a404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075095"
---
# <a name="control-events-windows-installer"></a>Eventos de control (Windows instalador)

Un control ControlEvent especifica una acción que debe realizar el instalador o un cambio en los atributos de uno o varios controles de un cuadro de diálogo. Para obtener más información sobre ControlEvents, vea [Información general de ControlEvent.](controlevent-overview.md)

En la tabla siguiente se proporcionan vínculos a más información sobre determinados ControlEvents.



| Evento de control                                                       | Breve descripción de ControlEvent                                                                                                                                                                             |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ActionData](actiondata-controlevent.md)                           | Publica los datos de la acción más reciente.                                                                                                                                                                          |
| [ActionText](actiontext-controlevent.md)                           | Publica el nombre de la acción actual.                                                                                                                                                                     |
| [AddLocal](addlocal-controlevent.md)                               | Notifica al instalador que ejecute las características localmente.                                                                                                                                                               |
| [AddSource](addsource-controlevent.md)                             | Notifica al instalador que ejecute características desde su origen.                                                                                                                                                     |
| [CheckExistingTargetPath](checkexistingtargetpath-controlevent.md) | Notifica al instalador que compruebe que se puede escribir la ruta de acceso.                                                                                                                                                |
| [CheckTargetPath](checktargetpath-controlevent.md)                 | Notifica al instalador que compruebe que la ruta de acceso es válida.                                                                                                                                                      |
| [DirectoryListNew](directorylistnew-controlevent.md)               | Notifica al control DirectoryList que cree una carpeta.                                                                                                                                                    |
| [DirectoryListOpen](directorylistopen-controlevent.md)             | Selecciona el directorio en el control DirectoryList.                                                                                                                                                           |
| [DirectoryListUp](directorylistup-controlevent.md)                 | Notifica al control DirectoryList que seleccione el elemento primario del directorio actual.                                                                                                                             |
| [DoAction](doaction-controlevent.md)                               | El cuadro de diálogo notifica al instalador que ejecute una acción personalizada.                                                                                                                                                 |
| [EnableRollback](enablerollback-controlevent.md)                   | Se usa para desactivar y activar las funcionalidades de reversión.                                                                                                                                                                |
| [EndDialog](enddialog-controlevent.md)                             | Notifica al instalador que quite un cuadro de diálogo modal.                                                                                                                                                          |
| [IgnoreChange](ignorechange-controlevent.md)                       | Publicado por el control DirectoryList cuando una carpeta está resaltada pero no abierta.                                                                                                                           |
| [MsiLaunchApp](msilaunchapp-controlevent.md)                       | Este evento de control ejecuta un archivo especificado. **[Windows Installer 4.5 y versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite.<br/>                                                       |
| [Msiprint](msiprint-controlevent.md)                               | Permite al usuario imprimir el contenido del control [ScrollableText](scrollabletext-control.md). **[Windows Installer 4.5 y versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite.<br/> |
| [NewDialog](newdialog-controlevent.md)                             | Notifica al instalador que cambie un cuadro de diálogo modal a otro cuadro de diálogo.                                                                                                                                  |
| [Reinstalación](reinstall-controlevent.md)                             | Inicia una reinstalación de características.                                                                                                                                                                       |
| [ReinstallMode](reinstallmode-controlevent.md)                     | Especifica el modo de validación durante una reinstalación.                                                                                                                                                        |
| [Remove](remove-controlevent.md)                                   | Notifica al instalador cuándo se seleccionan las características para su eliminación.                                                                                                                                                |
| [Reset](reset-controlevent.md)                                     | Restablece todos los valores de propiedad a los valores predeterminados usados cuando se creó el cuadro de diálogo.                                                                                                                    |
| [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)       | Use el [Administrador de reinicio](/windows/desktop/RstMgr/restart-manager-portal) para apagar todas las aplicaciones que tienen archivos en uso y reiniciarlas al final de la instalación.                                                              |
| [ScriptInProgress](scriptinprogress-controlevent.md)               | Muestra una cadena mientras se compila el script de ejecución.                                                                                                                                                     |
| [SelectionAction](selectionaction-controlevent.md)                 | Publicado por SelectionTree para describir un elemento.                                                                                                                                                               |
| [SelectionBrowse](selectionbrowse-controlevent.md)                 | Publicado por SelectionTree para generar un cuadro de diálogo.                                                                                                                                                             |
| [SelectionDescription](selectiondescription-controlevent.md)       | Publicado por SelectionTree para proporcionar una cadena en el campo Descripción de la tabla de características.                                                                                                                 |
| [SelectionNoItems](selectionnoitems-controlevent.md)               | Usado por SelectionTree para eliminar texto o deshabilitar botones.                                                                                                                                                      |
| [SelectionPath](selectionpath-controlevent.md)                     | Publicado por SelectionTree para proporcionar la ruta de acceso de un elemento.                                                                                                                                                    |
| [SelectionPathOn](selectionpathon-controlevent.md)                 | Publicado por SelectionTree para indicar si hay una ruta de acceso asociada a una característica.                                                                                                                     |
| [SelectionSize](selectionsize-controlevent.md)                     | Publicado por el control SelectionTree para proporcionar el tamaño de un elemento.                                                                                                                                            |
| [SetInstallLevel](setinstalllevel-controlevent.md)                 | El instalador cambia el nivel de instalación a un valor especificado.                                                                                                                                                |
| [SetProgress](setprogress-controlevent.md)                         | Publicado por el instalador para proporcionar el progreso de la instalación.                                                                                                                                                  |
| [SetProperty](setproperty-controlevent.md)                         | Establece una propiedad especificada.                                                                                                                                                                                    |
| [SetTargetPath](settargetpath-controlevent.md)                     | Notifica al instalador que compruebe y establezca una ruta de acceso.                                                                                                                                                               |
| [SpawnDialog](spawndialog-controlevent.md)                         | Notifica al instalador que cree un elemento secundario de un cuadro modal.                                                                                                                                                      |
| [SpawnWaitDialog](spawnwaitdialog-controlevent.md)                 | Desencadena un cuadro de diálogo especificado.                                                                                                                                                                              |
| [TimeRemaining](timeremaining-controlevent.md)                     | Publicado por el instalador para proporcionar el tiempo restante en la secuencia de progreso.                                                                                                                            |
| [ValidateProductID](validateproductid-controlevent.md)             | Establece ProductID en el identificador de producto completo.                                                                                                                                                                        |



 

 

