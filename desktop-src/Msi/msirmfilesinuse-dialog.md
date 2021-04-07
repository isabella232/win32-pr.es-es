---
description: Se puede crear el cuadro de diálogo MsiRMFilesInUse para mostrar una lista de los procesos que están en ejecución en ese momento y que la instalación debe sobrescribir o eliminar.
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: Cuadro de diálogo MsiRMFilesInUse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bba73cab51f4b3d8321b15001dbb72c638176b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002975"
---
# <a name="msirmfilesinuse-dialog"></a>Cuadro de diálogo MsiRMFilesInUse

Se puede crear el cuadro de diálogo MsiRMFilesInUse para mostrar una lista de los procesos que están en ejecución en ese momento y que la instalación debe sobrescribir o eliminar. El usuario puede seleccionar entre las opciones para "cerrar automáticamente las aplicaciones y reiniciarlas" o "no cerrar las aplicaciones. (Se requerirá un reinicio). Si el usuario selecciona la opción "cerrar aplicaciones y reiniciarse automáticamente", se puede crear un control de botón de opción en este cuadro de diálogo para publicar el evento de control RMShutdownAndRestart y el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) puede cerrar las aplicaciones y reiniciarlas al final de la instalación. Esto puede eliminar o reducir la necesidad de reiniciar el equipo. Para obtener más información, consulte [reinicios del sistema](system-reboots.md).

El cuadro de diálogo **MsiRMFilesInUse** se muestra durante una instalación solo si se cumplen todas las condiciones siguientes. Cuando cualquiera de ellas es falsa, el Windows Installer omite el cuadro de diálogo **MsiRMFilesInUse** .

-   Una versión de Windows Installer que no sea anterior a la versión 4,0 y un sistema operativo que no sea anterior a Windows Vista o Windows Server 2008 está ejecutando la instalación.
-   Se utiliza el [nivel de interfaz de usuario](user-interface-levels.md) completo de la interfaz de usuario.
-   La propiedad [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) o la directiva [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) no han deshabilitado las interacciones con el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) .
-   El cuadro de diálogo **MsiRMFilesInUse** está presente en el paquete de instalación.
-   Todas las llamadas del Windows Installer al [Administrador de reinicio](../rstmgr/restart-manager-portal.md) son correctas.

Este cuadro de diálogo se creará según sea necesario para la [acción InstallValidate](installvalidate-action.md).

 

 
