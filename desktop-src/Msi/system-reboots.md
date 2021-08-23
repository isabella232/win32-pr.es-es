---
description: El Windows puede determinar cuándo es necesario reiniciar el sistema y solicitar automáticamente al usuario que se reinicie al final de la instalación.
ms.assetid: 10117d2c-c2c8-456f-9fce-a89c2d69d3c1
title: Reinicios del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e5ff72b91b50a3da03fbfb0c52ff351af907c7f89b400120c463dab233f288
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626835"
---
# <a name="system-reboots"></a>Reinicios del sistema

El Windows puede determinar cuándo es necesario reiniciar el sistema y solicitar automáticamente al usuario que se reinicie al final de la instalación. Por ejemplo, el instalador solicita automáticamente un reinicio si necesita reemplazar los archivos que están en uso durante la instalación.

Las aplicaciones que [usan Windows Installer](windows-installer-portal.md) versión 4.0 o posterior para [](../rstmgr/restart-manager-portal.md) la instalación y el mantenimiento usan automáticamente el Administrador de reinicio para reducir los reinicios del sistema. Windows La versión del instalador 4.0 o posterior tiene propiedades y directivas que permiten al autor del paquete y a los administradores controlar la interacción de Windows Installer con el Administrador de reinicio. Para obtener más información, vea [Using Windows Installer with Restart Manager](using-windows-installer-with-restart-manager.md).

Los autores de paquetes de instalación pueden programar y suprimir reinicios mediante acciones estándar en las tablas de secuencia y estableciendo propiedades. Las siguientes acciones y propiedades se usan para controlar los reinicios del sistema.



| Acción, cuadro de diálogo o propiedad                                                | Breve descripción                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acción ForceReboot](forcereboot-action.md)                                   | Solicita al usuario un reinicio durante la instalación.                                                                                                        |
| [Acción ScheduleReboot](schedulereboot-action.md)                             | Solicita al usuario un reinicio al final de la instalación.                                                                                                 |
| [**Reboot (propiedad)**](reboot.md)                                              | Fuerza o suprime ciertos avisos automáticos para un reinicio del sistema.                                                                                           |
| [**Propiedad REBOOTPROMPT**](rebootprompt.md)                                  | Suprime la presentación de mensajes de reinicio al usuario. Los reinicios necesarios se suceden automáticamente.                                                           |
| [**Propiedad AFTERREBOOT**](afterreboot.md)                                    | Se usa normalmente en una condición impuesta en la acción ForceReboot.                                                                                               |
| [Acción InstallValidate](installvalidate-action.md)                           | Muestra el cuadro de diálogo FilesInUse , si es necesario, que ofrece a los usuarios la oportunidad de apagar los procesos y evitar algunos reinicios del sistema.                              |
| [Cuadro de diálogo FilesInUse](filesinuse-dialog.md)                                     | Ofrece a los usuarios la oportunidad de apagar los procesos para evitar algunos reinicios del sistema.                                                                              |
| [Cuadro de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md)                           | Ofrece a los usuarios la opción de usar [el Administrador de reinicio](../rstmgr/restart-manager-portal.md) para cerrar y reiniciar aplicaciones. Disponible a partir de Windows Installer versión 4.0. |
| [**Propiedad ReplacedInUseFiles**](replacedinusefiles.md)                      | Establezca si el instalador se instala a través de un archivo en uso. Esta propiedad se usa mediante acciones personalizadas para detectar que se requiere un reinicio.                                |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)                   | Propiedad para deshabilitar la Windows instalador con [el Administrador de reinicio.](../rstmgr/restart-manager-portal.md) Disponible a partir de Windows Installer versión 4.0.          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)                             | Especifica cómo el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) cierra y reinicia las aplicaciones. Disponible a partir de Windows Installer versión 4.0.                  |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)                                         | Especifica cómo el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) cierra y reinicia las aplicaciones. Disponible a partir de Windows Installer versión 4.0.                  |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)                       | El instalador establece esta propiedad si hay un reinicio del sistema operativo pendiente. Disponible a partir de Windows Installer versión 4.0.                         |
| [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) | Directiva para deshabilitar la Windows instalador con [el Administrador de reinicio.](../rstmgr/restart-manager-portal.md) Disponible a partir de Windows Installer versión 4.0.                |



 

ERROR \_ INSTALL SUSPEND significa que la instalación no se ha completado ni se ha \_ reversión. La instalación debe reanudarse antes de que se complete. Es posible que sea necesario reiniciar el sistema para poder reanudar la instalación.

El Windows de instalación devuelve el código de error ERROR \_ INSTALL SUSPEND cuando se ejecuta la acción \_ [ForceReboot.](forcereboot-action.md) Devuelve ERROR SUCCESS REBOOT REQUIRED si se requiere un reinicio antes de ejecutar la aplicación y devuelve ERROR SUCCESS REBOOT INITIATED si el instalador ha iniciado realmente \_ \_ un \_ \_ \_ \_ reinicio. Tenga en cuenta que, dado que los reinicios son asincrónicos, el reinicio puede producirse antes de que se devuelva el código de error. Para obtener más información, vea [Códigos de error](error-codes.md).

Las acciones personalizadas pueden forzar un aviso de reinicio al final de una instalación mediante una [**llamada a MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode). Las acciones personalizadas también pueden comprobar si hay un mensaje de reinicio pendiente llamando a [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode).

## <a name="filesinuse-dialog"></a>Cuadro de diálogo FilesInUse

El instalador puede determinar cuándo es necesario reiniciar el sistema y solicitar al usuario que reinicie. Normalmente, se requiere un reinicio del sistema porque el instalador está intentando instalar un archivo que se está utilizando actualmente. Si la [acción InstallValidate](installvalidate-action.md) detecta la instalación de un archivo en uso, se muestra el [cuadro de diálogo FilesInUse](filesinuse-dialog.md).

Si espera que el instalador muestre un elemento FilesInUseDialog, pero no lo hace, puede deberse a uno de los siguientes motivos:

-   Los archivos en uso no son ejecutables.
-   El instalador no está intentando instalar esos archivos.
-   El proceso que mantiene esos archivos es el proceso que invoca la instalación.
-   El proceso que contiene esos archivos es aquel que no tiene una ventana con un título asociado.

Para obtener más información, vea [Registro de solicitudes de reinicio.](logging-of-reboot-requests.md)

 

 
