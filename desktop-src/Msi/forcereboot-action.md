---
description: La acción ForceReboot solicita al usuario que se reinicie el sistema durante la instalación.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: Acción ForceReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807bab474f1faacfbc7684797b7a0b7b74f354d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667792"
---
# <a name="forcereboot-action"></a><span data-ttu-id="3ba69-103">Acción ForceReboot</span><span class="sxs-lookup"><span data-stu-id="3ba69-103">ForceReboot Action</span></span>

<span data-ttu-id="3ba69-104">La acción ForceReboot solicita al usuario que se reinicie el sistema durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="3ba69-104">The ForceReboot action prompts the user for a restart of the system during the installation.</span></span> <span data-ttu-id="3ba69-105">La acción ForceReboot es diferente de la [acción ScheduleReboot](schedulereboot-action.md) en que la acción ScheduleReboot se usa para programar una solicitud de reinicio al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="3ba69-105">The ForceReboot action is different from the [ScheduleReboot action](schedulereboot-action.md) in that the ScheduleReboot action is used to schedule a prompt to restart at the end of the installation.</span></span>

<span data-ttu-id="3ba69-106">Si la instalación tiene una interfaz de usuario, el instalador muestra un cuadro de diálogo en cada acción de ForceReboot que solicita al usuario que reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="3ba69-106">If the installation has a user interface, the installer displays a dialog box at each ForceReboot action which prompts the user to restart the system.</span></span> <span data-ttu-id="3ba69-107">El usuario debe responder a este mensaje antes de continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="3ba69-107">The user must respond to this prompt before continuing with the installation.</span></span> <span data-ttu-id="3ba69-108">Si la instalación no tiene ninguna interfaz de usuario, el sistema se reiniciará automáticamente en la acción ForceReboot.</span><span class="sxs-lookup"><span data-stu-id="3ba69-108">If the installation has no user interface, the system automatically restarts at the ForceReboot action.</span></span>

<span data-ttu-id="3ba69-109">Si el instalador determina que se necesita un reinicio, automáticamente solicita al usuario que reinicie al final de la instalación, independientemente de si hay alguna acción de ForceReboot o ScheduleReboot en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="3ba69-109">If the installer determines that a restart is necessary, it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="3ba69-110">Por ejemplo, el instalador solicita automáticamente un reinicio si es necesario reemplazar los archivos que se usan durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="3ba69-110">For example, the installer automatically prompts for a restart if it needs to replace any files used during the installation.</span></span>

<span data-ttu-id="3ba69-111">Para suprimir ciertas solicitudes de reinicio, establezca la propiedad [**reboot**](reboot.md) .</span><span class="sxs-lookup"><span data-stu-id="3ba69-111">Suppress certain restart prompts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="3ba69-112">Si el Windows Installer encuentra la acción ForceReboot o [ScheduleReboot](schedulereboot-action.md) durante una [instalación de varios paquetes](multiple-package-installations.md), el instalador se detendrá y revertirá la instalación.</span><span class="sxs-lookup"><span data-stu-id="3ba69-112">If the Windows Installer encounters the ForceReboot or [ScheduleReboot](schedulereboot-action.md) action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="3ba69-113">Se pueden instalar otros paquetes que pertenezcan a la instalación de varios paquetes que no contengan una acción ForceReboot o ScheduleReboot.</span><span class="sxs-lookup"><span data-stu-id="3ba69-113">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3ba69-114">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="3ba69-114">Sequence Restrictions</span></span>

<span data-ttu-id="3ba69-115">Las siguientes acciones suelen producirse juntas como un grupo en la secuencia de acciones.</span><span class="sxs-lookup"><span data-stu-id="3ba69-115">The following actions commonly occur together as a group in the action sequence.</span></span> <span data-ttu-id="3ba69-116">Se recomienda programar la acción ForceReboot para que aparezca después de este grupo.</span><span class="sxs-lookup"><span data-stu-id="3ba69-116">It is recommended that the ForceReboot action be scheduled to come after this group.</span></span> <span data-ttu-id="3ba69-117">Si la acción ForceReboot está programada antes de la [acción RegisterProduct](registerproduct-action.md), el instalador necesita de nuevo el origen del paquete de instalación después del reinicio.</span><span class="sxs-lookup"><span data-stu-id="3ba69-117">If the ForceReboot action is scheduled before the [RegisterProduct action](registerproduct-action.md), the installer again requires the source of the installation package after the restart.</span></span> <span data-ttu-id="3ba69-118">Por lo tanto, la secuencia preferida para ForceReboot está inmediatamente después de esta secuencia de acción.</span><span class="sxs-lookup"><span data-stu-id="3ba69-118">Therefore, the preferred sequence for ForceReboot is immediately following this action sequence.</span></span>

-   [<span data-ttu-id="3ba69-119">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="3ba69-119">RegisterProduct</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="3ba69-120">RegisterUser</span><span class="sxs-lookup"><span data-stu-id="3ba69-120">RegisterUser</span></span>](registeruser-action.md)
-   [<span data-ttu-id="3ba69-121">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="3ba69-121">PublishProduct</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="3ba69-122">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="3ba69-122">PublishFeatures</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="3ba69-123">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="3ba69-123">CreateShortcuts</span></span>](createshortcuts-action.md)
-   [<span data-ttu-id="3ba69-124">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="3ba69-124">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)
-   [<span data-ttu-id="3ba69-125">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="3ba69-125">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="3ba69-126">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="3ba69-126">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="3ba69-127">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="3ba69-127">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="3ba69-128">La acción ForceReboot debe estar entre [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md) en la secuencia de acción de la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="3ba69-128">The ForceReboot action must come between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the action sequence of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3ba69-129">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="3ba69-129">ActionData Messages</span></span>

<span data-ttu-id="3ba69-130">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="3ba69-130">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ba69-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ba69-131">Remarks</span></span>

<span data-ttu-id="3ba69-132">La acción ForceReboot siempre debe usarse con una instrucción condicional de modo que el instalador desencadene un reinicio solo cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="3ba69-132">The ForceReboot action must always be used with a conditional statement such that the installer triggers a restart only when necessary.</span></span> <span data-ttu-id="3ba69-133">Por ejemplo, un reinicio solo puede ser necesario si se reemplaza un archivo determinado o si se instala un componente determinado.</span><span class="sxs-lookup"><span data-stu-id="3ba69-133">For example, a restart may only be required if a particular file is replaced or a particular component is installed.</span></span> <span data-ttu-id="3ba69-134">Cada instalación de producto es única y es posible que sea necesaria una acción personalizada para determinar si es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="3ba69-134">Each product installation is unique and a custom action may be required to determine whether a restart is needed.</span></span> <span data-ttu-id="3ba69-135">Normalmente, la condición de la acción ForceReboot hace uso de la propiedad [**AFTERREBOOT**](afterreboot.md) .</span><span class="sxs-lookup"><span data-stu-id="3ba69-135">The condition on the ForceReboot action commonly makes use of the [**AFTERREBOOT**](afterreboot.md) property.</span></span>

<span data-ttu-id="3ba69-136">ForceReboot ejecuta operaciones del sistema generadas por acciones anteriores antes de solicitar un reinicio o un reinicio.</span><span class="sxs-lookup"><span data-stu-id="3ba69-136">ForceReboot runs system operations generated by any previous actions before prompting for a restart or restarting.</span></span> <span data-ttu-id="3ba69-137">Por ejemplo, las operaciones del sistema generadas por [InstallFiles](installfiles-action.md) y [WriteRegistryValues](writeregistryvalues-action.md) se ejecutan antes de un reinicio.</span><span class="sxs-lookup"><span data-stu-id="3ba69-137">For example, the system operations generated by [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) are run before a restart.</span></span>

<span data-ttu-id="3ba69-138">La acción ForceReboot escribe una clave del registro que hace que el instalador se inicie después de reiniciar.</span><span class="sxs-lookup"><span data-stu-id="3ba69-138">The ForceReboot action writes a registry key that causes the installer to start after restarting.</span></span> <span data-ttu-id="3ba69-139">La ubicación de esta clave es **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**.</span><span class="sxs-lookup"><span data-stu-id="3ba69-139">The location of this key is **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\RunOnce**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ba69-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3ba69-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ba69-141">Reinicios del sistema</span><span class="sxs-lookup"><span data-stu-id="3ba69-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 



