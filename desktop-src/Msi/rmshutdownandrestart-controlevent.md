---
description: Notifica a la Windows Installer que use el administrador de reinicio para cerrar todas las aplicaciones que tienen archivos en uso y reiniciarlas al final de la instalación.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: RmShutdownAndRestart ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc91d1de52f516c0728e8d6469fb8cddc2e50cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652520"
---
# <a name="rmshutdownandrestart-controlevent"></a>RmShutdownAndRestart ControlEvent,

Este evento notifica a la Windows Installer que use el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) para cerrar todas las aplicaciones que tienen archivos en uso y reiniciarlas al final de la instalación.

Este ControlEvent, no tiene ningún efecto si se cumple alguna de las siguientes condiciones.

-   El sistema operativo que ejecuta la instalación no es Windows Vista ni Windows Server 2008.
-   Las interacciones con el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) se han deshabilitado mediante la propiedad [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) o la directiva [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .
-   Actualmente no hay ninguna sesión de [Administrador de reinicio](../rstmgr/restart-manager-portal.md) abierta.
-   Cualquier llamada del Windows Installer al administrador de [reinicio](../rstmgr/restart-manager-portal.md) devuelve un error.

## <a name="typical-use"></a>Uso típico

El evento de control RMShutdownAndRestart solo se publica mediante un control [Pushbutton](pushbutton-control.md) en el cuadro de [diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) .

 

 
