---
description: Inserte la acción ScheduleReboot en la secuencia de acciones para solicitar al usuario que se reinicie el sistema al final de la instalación. Use la acción ForceReboot para solicitar un reinicio durante la instalación.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Acción ScheduleReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909814"
---
# <a name="schedulereboot-action"></a><span data-ttu-id="b28c1-104">Acción ScheduleReboot</span><span class="sxs-lookup"><span data-stu-id="b28c1-104">ScheduleReboot Action</span></span>

<span data-ttu-id="b28c1-105">Inserte la acción ScheduleReboot en la secuencia de acciones para solicitar al usuario que se reinicie el sistema al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="b28c1-105">Insert the ScheduleReboot action into the action sequence to prompt the user for a restart of the system at the end of the installation.</span></span> <span data-ttu-id="b28c1-106">Use la [acción ForceReboot](forcereboot-action.md) para solicitar un reinicio durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="b28c1-106">Use the [ForceReboot action](forcereboot-action.md) to prompt for a restart during installation.</span></span>

<span data-ttu-id="b28c1-107">Si la instalación tiene una interfaz de usuario, el instalador muestra un cuadro de mensaje y un botón al final de la instalación preguntándole si el usuario desea reiniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="b28c1-107">If the installation has a user interface, the installer displays a message box and button at the end of installation asking whether the user wants to restart the system.</span></span> <span data-ttu-id="b28c1-108">El usuario debe responder a este mensaje antes de completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="b28c1-108">The user must respond to this prompt before completing installation.</span></span> <span data-ttu-id="b28c1-109">Si la instalación no tiene ninguna interfaz de usuario, el sistema se reiniciará automáticamente al final.</span><span class="sxs-lookup"><span data-stu-id="b28c1-109">If the installation has no user interface, the system automatically restarts at the end.</span></span>

<span data-ttu-id="b28c1-110">Si el instalador determina que es necesario reiniciar, solicita automáticamente al usuario que reinicie al final de la instalación, si hay alguna acción ForceReboot o ScheduleReboot en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b28c1-110">If the installer determines that a restart is necessary it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="b28c1-111">Por ejemplo, el instalador solicita automáticamente un reinicio si es necesario reemplazar los archivos que se están usando durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="b28c1-111">For example, the installer automatically prompts for a restart if it needs to replace any files that are in use during installation.</span></span>

<span data-ttu-id="b28c1-112">Puede suprimir determinados mensajes para los reinicios estableciendo la propiedad [**reboot**](reboot.md) .</span><span class="sxs-lookup"><span data-stu-id="b28c1-112">You can suppress certain prompts for restarts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="b28c1-113">Si el Windows Installer encuentra la acción [ForceReboot](forcereboot-action.md) o ScheduleReboot durante una [instalación de varios paquetes](multiple-package-installations.md), el instalador se detendrá y revertirá la instalación.</span><span class="sxs-lookup"><span data-stu-id="b28c1-113">If the Windows Installer encounters the [ForceReboot](forcereboot-action.md) or ScheduleReboot action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="b28c1-114">Se pueden instalar otros paquetes que pertenezcan a la instalación de varios paquetes que no contengan una acción ForceReboot o ScheduleReboot.</span><span class="sxs-lookup"><span data-stu-id="b28c1-114">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b28c1-115">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="b28c1-115">Sequence Restrictions</span></span>

<span data-ttu-id="b28c1-116">No hay restricciones de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b28c1-116">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b28c1-117">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="b28c1-117">ActionData Messages</span></span>

<span data-ttu-id="b28c1-118">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="b28c1-118">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="b28c1-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b28c1-119">Remarks</span></span>

<span data-ttu-id="b28c1-120">Por ejemplo, esta acción se puede usar para obligar al instalador a solicitar un reinicio después de instalar los controladores que requieren un reinicio.</span><span class="sxs-lookup"><span data-stu-id="b28c1-120">For example, this action can be used to force the installer to prompt for a restart after installing drivers that require a restart.</span></span> <span data-ttu-id="b28c1-121">Si el instalador intenta reemplazar archivos que están en uso, automáticamente solicita al usuario que se reinicie aunque no se haya utilizado ScheduleReboot.</span><span class="sxs-lookup"><span data-stu-id="b28c1-121">If the installer attempts to replace files that are in use, it automatically prompts the user to restart even if ScheduleReboot has not been used.</span></span>

<span data-ttu-id="b28c1-122">La acción ScheduleReboot normalmente se coloca al final de la secuencia, pero se puede insertar en cualquier punto de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b28c1-122">The ScheduleReboot action is typically placed at the end of the sequence, but it can be inserted at any point in the sequence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b28c1-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b28c1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b28c1-124">Reinicios del sistema</span><span class="sxs-lookup"><span data-stu-id="b28c1-124">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 



