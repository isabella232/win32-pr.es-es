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
# <a name="rmshutdownandrestart-controlevent"></a><span data-ttu-id="e5a31-103">RmShutdownAndRestart ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="e5a31-103">RmShutdownAndRestart ControlEvent</span></span>

<span data-ttu-id="e5a31-104">Este evento notifica a la Windows Installer que use el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) para cerrar todas las aplicaciones que tienen archivos en uso y reiniciarlas al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="e5a31-104">This event notifies the Windows Installer to use the [Restart Manager](../rstmgr/restart-manager-portal.md) to shutdown all applications that have files in use and to restart them at the end of the installation.</span></span>

<span data-ttu-id="e5a31-105">Este ControlEvent, no tiene ningún efecto si se cumple alguna de las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="e5a31-105">This ControlEvent has no effect if any of the following are true.</span></span>

-   <span data-ttu-id="e5a31-106">El sistema operativo que ejecuta la instalación no es Windows Vista ni Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e5a31-106">The operating system running the installation is not Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="e5a31-107">Las interacciones con el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) se han deshabilitado mediante la propiedad [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) o la directiva [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a31-107">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="e5a31-108">Actualmente no hay ninguna sesión de [Administrador de reinicio](../rstmgr/restart-manager-portal.md) abierta.</span><span class="sxs-lookup"><span data-stu-id="e5a31-108">There is currently no open [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>
-   <span data-ttu-id="e5a31-109">Cualquier llamada del Windows Installer al administrador de [reinicio](../rstmgr/restart-manager-portal.md) devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="e5a31-109">Any calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) returns a failure.</span></span>

## <a name="typical-use"></a><span data-ttu-id="e5a31-110">Uso típico</span><span class="sxs-lookup"><span data-stu-id="e5a31-110">Typical Use</span></span>

<span data-ttu-id="e5a31-111">El evento de control RMShutdownAndRestart solo se publica mediante un control [Pushbutton](pushbutton-control.md) en el cuadro de [diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a31-111">The RMShutdownAndRestart control event is published only by a [PushButton](pushbutton-control.md) control on the [MsiRMFilesInUse Dialog](msirmfilesinuse-dialog.md) box.</span></span>

 

 
