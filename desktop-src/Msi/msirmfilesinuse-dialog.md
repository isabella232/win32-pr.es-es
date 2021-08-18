---
description: Se puede crear el cuadro de diálogo MsiRMFilesInUse para mostrar una lista de procesos que actualmente ejecutan archivos que la instalación debe sobrescribir o eliminar.
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: Cuadro de diálogo MsiRMFilesInUse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04aa3167609693135e2d3196fef0495d5244fe44f1a6e7d95d11f999efe51a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012894"
---
# <a name="msirmfilesinuse-dialog"></a>Cuadro de diálogo MsiRMFilesInUse

Se puede crear el cuadro de diálogo MsiRMFilesInUse para mostrar una lista de procesos que actualmente ejecutan archivos que la instalación debe sobrescribir o eliminar. El usuario puede seleccionar entre opciones para "Cerrar automáticamente las aplicaciones y reiniciarlas" o "No cerrar aplicaciones. (Se requiere un reinicio)." Si el usuario selecciona la opción "Cerrar automáticamente las aplicaciones y reiniciarlas", se puede crear un control de botón de [](../rstmgr/restart-manager-portal.md) inserción en este cuadro de diálogo para publicar el evento de control RMShutdownAndRestart y el Administrador de reinicio puede cerrar las aplicaciones y reiniciarlas al final de la instalación. Esto puede eliminar o reducir la necesidad de reiniciar el equipo. Para obtener más información, vea [Reinicios del sistema.](system-reboots.md)

El **cuadro de diálogo MsiRMFilesInUse** se muestra durante una instalación solo si se cumplen todas las condiciones siguientes. Cuando cualquiera de ellos es false, el Windows omite el **cuadro de diálogo MsiRMFilesInUse.**

-   Una versión del instalador de Windows que no sea anterior a la versión 4.0 y un sistema operativo que no sea anterior a Windows Vista o Windows Server 2008 está ejecutando la instalación.
-   Se usa el nivel de [interfaz de usuario De](user-interface-levels.md) interfaz de usuario completa.
-   Las interacciones con [el Administrador de](../rstmgr/restart-manager-portal.md) reinicio no se han deshabilitado mediante la propiedad [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) o la directiva [DisableAutomaticApplicationShutdown.](disableautomaticapplicationshutdown.md)
-   El **cuadro de diálogo MsiRMFilesInUse** está presente en el paquete de instalación.
-   Todas las llamadas del instalador Windows al [Administrador de reinicio](../rstmgr/restart-manager-portal.md) se han realizado correctamente.

Este cuadro de diálogo se creará según sea necesario en la [acción InstallValidate](installvalidate-action.md).

 

 
