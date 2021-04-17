---
description: El Windows Installer puede determinar cuándo es necesario reiniciar el sistema y solicitar automáticamente al usuario que reinicie al final de la instalación.
ms.assetid: 10117d2c-c2c8-456f-9fce-a89c2d69d3c1
title: Reinicios del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b32149bbcd43e284f45d7cabcba94a080be5262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652489"
---
# <a name="system-reboots"></a>Reinicios del sistema

El Windows Installer puede determinar cuándo es necesario reiniciar el sistema y solicitar automáticamente al usuario que reinicie al final de la instalación. Por ejemplo, el instalador solicita automáticamente que se reinicie si es necesario reemplazar los archivos que se están usando durante la instalación.

Las aplicaciones que usan [Windows Installer](windows-installer-portal.md) versión 4,0 o posterior para la instalación y el mantenimiento usan automáticamente el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) para reducir los reinicios del sistema. Windows Installer versión 4,0 o posterior tiene propiedades y directivas que permiten al autor del paquete y a los administradores controlar la interacción de Windows Installer con el administrador de reinicio. Para obtener más información, consulte [uso de Windows Installer con el administrador de reinicio](using-windows-installer-with-restart-manager.md).

Los autores de paquetes de instalación pueden programar y suprimir los reinicios mediante acciones estándar en las tablas de secuencia y estableciendo las propiedades. Las siguientes acciones y propiedades se usan para controlar los reinicios del sistema.



| Acción, cuadro de diálogo o propiedad                                                | Breve descripción                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acción ForceReboot](forcereboot-action.md)                                   | Solicita al usuario que se reinicie durante la instalación.                                                                                                        |
| [Acción ScheduleReboot](schedulereboot-action.md)                             | Solicita al usuario un reinicio al final de la instalación.                                                                                                 |
| [**Reboot (propiedad)**](reboot.md)                                              | Fuerza o suprime ciertos mensajes automáticos de un reinicio del sistema.                                                                                           |
| [**Propiedad REBOOTPROMPT**](rebootprompt.md)                                  | Suprime la presentación de mensajes para que los reinicie el usuario. Los reinicios necesarios se producen automáticamente.                                                           |
| [**Propiedad AFTERREBOOT**](afterreboot.md)                                    | Se utiliza normalmente en una condición impuesta en la acción ForceReboot.                                                                                               |
| [Acción InstallValidate](installvalidate-action.md)                           | Muestra el cuadro de diálogo FilesInUse, si es necesario, ofreciendo a los usuarios la oportunidad de cerrar procesos y evitar algunos reinicios del sistema.                              |
| [Cuadro de diálogo FilesInUse](filesinuse-dialog.md)                                     | Ofrece a los usuarios la oportunidad de cerrar los procesos para evitar que se reinicie el sistema.                                                                              |
| [Cuadro de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md)                           | Ofrece a los usuarios la opción de usar el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) para cerrar y reiniciar las aplicaciones. Disponible a partir de Windows Installer versión 4,0. |
| [**Propiedad ReplacedInUseFiles**](replacedinusefiles.md)                      | Se establece si el instalador se instala en un archivo en uso. Esta propiedad la usan las acciones personalizadas para detectar que es necesario reiniciar.                                |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)                   | Propiedad para deshabilitar la interacción de Windows Installer con el [Administrador de reinicio](../rstmgr/restart-manager-portal.md). Disponible a partir de Windows Installer versión 4,0.          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)                             | Especifica cómo se cierra el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) y reinicia las aplicaciones. Disponible a partir de Windows Installer versión 4,0.                  |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)                                         | Especifica cómo se cierra el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) y reinicia las aplicaciones. Disponible a partir de Windows Installer versión 4,0.                  |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)                       | El instalador establece esta propiedad si está pendiente un reinicio del sistema operativo. Disponible a partir de Windows Installer versión 4,0.                         |
| [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) | Directiva para deshabilitar la interacción de Windows Installer con el [Administrador de reinicio](../rstmgr/restart-manager-portal.md). Disponible a partir de Windows Installer versión 4,0.                |



 

ERROR \_ en \_ la instalación de la suspensión significa que la instalación no se completó o revierte. La instalación se debe reanudar antes de completarse. Es posible que sea necesario reiniciar el sistema antes de que se pueda reanudar la instalación.

El Windows Installer devuelve el código de error ERROR al \_ instalar \_ suspender cuando se ejecuta la [acción ForceReboot](forcereboot-action.md) . Devuelve un ERROR \_ \_ de reinicio correcto \_ necesario si se requiere un reinicio antes de ejecutar la aplicación y devuelve un error de \_ \_ reinicio correcto \_ iniciado si el instalador ha iniciado realmente un reinicio. Tenga en cuenta que, dado que los reinicios son asíncronos, es posible que se produzca el reinicio antes de que se devuelva el código de error. Para obtener más información, consulte [códigos de error](error-codes.md).

Las acciones personalizadas pueden forzar un aviso para que se reinicie al final de una instalación mediante una llamada a [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode). Las acciones personalizadas también pueden comprobar si hay un mensaje de reinicio pendiente llamando a [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode).

## <a name="filesinuse-dialog"></a>Cuadro de diálogo FilesInUse

El instalador puede determinar cuándo es necesario reiniciar el sistema y preguntar al usuario con una solicitud de reinicio. Normalmente, es necesario reiniciar el sistema porque el instalador está intentando instalar un archivo que se está usando actualmente. Si la [acción InstallValidate](installvalidate-action.md) detecta la instalación de un archivo en uso, muestra el [cuadro de diálogo FilesInUse](filesinuse-dialog.md).

Si espera que el instalador muestre un FilesInUseDialog, pero no lo hace, puede deberse a uno de los siguientes motivos:

-   Los archivos en uso no son ejecutables.
-   El instalador no está intentando realmente instalar esos archivos.
-   El proceso que contiene esos archivos es el proceso que invoca la instalación.
-   El proceso que contiene esos archivos es aquél que no tiene una ventana con un título asociado.

Para obtener más información, consulte [registro de solicitudes de reinicio](logging-of-reboot-requests.md).

 

 
