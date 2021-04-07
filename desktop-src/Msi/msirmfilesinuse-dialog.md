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
# <a name="msirmfilesinuse-dialog"></a><span data-ttu-id="ec4c3-103">Cuadro de diálogo MsiRMFilesInUse</span><span class="sxs-lookup"><span data-stu-id="ec4c3-103">MsiRMFilesInUse Dialog</span></span>

<span data-ttu-id="ec4c3-104">Se puede crear el cuadro de diálogo MsiRMFilesInUse para mostrar una lista de los procesos que están en ejecución en ese momento y que la instalación debe sobrescribir o eliminar.</span><span class="sxs-lookup"><span data-stu-id="ec4c3-104">The MsiRMFilesInUse Dialog box can be authored to display a list of processes that are currently running files that need to be overwritten or deleted by the installation.</span></span> <span data-ttu-id="ec4c3-105">El usuario puede seleccionar entre las opciones para "cerrar automáticamente las aplicaciones y reiniciarlas" o "no cerrar las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ec4c3-105">The user can select between options to "Automatically close applications and restart them" or "Do not close applications.</span></span> <span data-ttu-id="ec4c3-106">(Se requerirá un reinicio). Si el usuario selecciona la opción "cerrar aplicaciones y reiniciarse automáticamente", se puede crear un control de botón de opción en este cuadro de diálogo para publicar el evento de control RMShutdownAndRestart y el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) puede cerrar las aplicaciones y reiniciarlas al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="ec4c3-106">(A reboot will be required.)" If the user selects the "Automatically close applications and restart them" option, a push button control on this dialog box can be authored to publish the RMShutdownAndRestart control event and the [Restart Manager](../rstmgr/restart-manager-portal.md) can close the applications and restart them at the end of the installation.</span></span> <span data-ttu-id="ec4c3-107">Esto puede eliminar o reducir la necesidad de reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="ec4c3-107">This can eliminate or reduce the need to restart the computer.</span></span> <span data-ttu-id="ec4c3-108">Para obtener más información, consulte [reinicios del sistema](system-reboots.md).</span><span class="sxs-lookup"><span data-stu-id="ec4c3-108">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="ec4c3-109">El cuadro de diálogo **MsiRMFilesInUse** se muestra durante una instalación solo si se cumplen todas las condiciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="ec4c3-109">The **MsiRMFilesInUse** dialog box is displayed during an installation only if all the following are true.</span></span> <span data-ttu-id="ec4c3-110">Cuando cualquiera de ellas es falsa, el Windows Installer omite el cuadro de diálogo **MsiRMFilesInUse** .</span><span class="sxs-lookup"><span data-stu-id="ec4c3-110">When any of these are false, the Windows Installer ignores the **MsiRMFilesInUse** dialog box.</span></span>

-   <span data-ttu-id="ec4c3-111">Una versión de Windows Installer que no sea anterior a la versión 4,0 y un sistema operativo que no sea anterior a Windows Vista o Windows Server 2008 está ejecutando la instalación.</span><span class="sxs-lookup"><span data-stu-id="ec4c3-111">A Windows Installer version that is not earlier than version 4.0 and an operating system that is not earlier than Windows Vista or Windows Server 2008 is running the installation.</span></span>
-   <span data-ttu-id="ec4c3-112">Se utiliza el [nivel de interfaz de usuario](user-interface-levels.md) completo de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ec4c3-112">The Full UI [user interface level](user-interface-levels.md) is used.</span></span>
-   <span data-ttu-id="ec4c3-113">La propiedad [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) o la directiva [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) no han deshabilitado las interacciones con el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ec4c3-113">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have not been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="ec4c3-114">El cuadro de diálogo **MsiRMFilesInUse** está presente en el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="ec4c3-114">The **MsiRMFilesInUse** dialog box is present in the installation package.</span></span>
-   <span data-ttu-id="ec4c3-115">Todas las llamadas del Windows Installer al [Administrador de reinicio](../rstmgr/restart-manager-portal.md) son correctas.</span><span class="sxs-lookup"><span data-stu-id="ec4c3-115">All calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) are successful.</span></span>

<span data-ttu-id="ec4c3-116">Este cuadro de diálogo se creará según sea necesario para la [acción InstallValidate](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="ec4c3-116">This dialog box will be created as required by the [InstallValidate action](installvalidate-action.md).</span></span>

 

 
