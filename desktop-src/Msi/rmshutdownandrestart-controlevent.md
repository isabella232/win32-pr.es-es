---
description: Notifica al instalador Windows que use el Administrador de reinicio para apagar todas las aplicaciones que tienen archivos en uso y reiniciarlas al final de la instalación.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: RmShutdownAndRestart ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f483e485eeefc2d3a761a3d9c9ff95989a3150dcfd8fff6a36bfb6211504e95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625901"
---
# <a name="rmshutdownandrestart-controlevent"></a>RmShutdownAndRestart ControlEvent

Este evento notifica al instalador de Windows [](../rstmgr/restart-manager-portal.md) que use el Administrador de reinicio para apagar todas las aplicaciones que tienen archivos en uso y reiniciarlos al final de la instalación.

Este control ControlEvent no tiene ningún efecto si se cumple alguna de las siguientes condiciones.

-   El sistema operativo que ejecuta la instalación no Windows Vista ni Windows Server 2008.
-   Las interacciones con [el Administrador de reinicio](../rstmgr/restart-manager-portal.md) se han deshabilitado mediante la propiedad [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) o la [directiva DisableAutomaticApplicationShutdown.](disableautomaticapplicationshutdown.md)
-   Actualmente no hay ninguna sesión [de Restart Manager](../rstmgr/restart-manager-portal.md) abierta.
-   Las llamadas del instalador Windows al [Administrador de reinicio](../rstmgr/restart-manager-portal.md) devuelven un error.

## <a name="typical-use"></a>Uso típico

El evento de control RMShutdownAndRestart solo lo publica un control [PushButton](pushbutton-control.md) en el cuadro de [diálogo MsiRMFilesInUse.](msirmfilesinuse-dialog.md)

 

 
