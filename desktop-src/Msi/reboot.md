---
description: La propiedad reboot suprime determinados mensajes para reiniciar el sistema.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Reboot (propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94b08a04f3e95d873f6fc233185ce623cafc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653733"
---
# <a name="reboot-property"></a><span data-ttu-id="11448-103">Reboot (propiedad)</span><span class="sxs-lookup"><span data-stu-id="11448-103">REBOOT property</span></span>

<span data-ttu-id="11448-104">La propiedad **REboot** suprime determinados mensajes para reiniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="11448-104">The **REBOOT** property suppresses certain prompts for a restart of the system.</span></span> <span data-ttu-id="11448-105">Normalmente, un administrador usa esta propiedad con una serie de instalaciones para instalar varios productos al mismo tiempo con un solo reinicio al final.</span><span class="sxs-lookup"><span data-stu-id="11448-105">An administrator typically uses this property with a series of installations to install several products at the same time with only one restart at the end.</span></span> <span data-ttu-id="11448-106">Para obtener más información, consulte [reinicios del sistema](system-reboots.md).</span><span class="sxs-lookup"><span data-stu-id="11448-106">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="11448-107">Las acciones [ForceReboot](forcereboot-action.md) y [ScheduleReboot](schedulereboot-action.md) informan al instalador de que pida al usuario que reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="11448-107">The [ForceReboot](forcereboot-action.md) and [ScheduleReboot](schedulereboot-action.md) actions inform the installer to prompt the user to restart the system.</span></span> <span data-ttu-id="11448-108">El instalador también puede determinar que es necesario reiniciar si hay alguna acción de ForceReboot o ScheduleReboot en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="11448-108">The installer can also determine that a restart is necessary whether there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="11448-109">Por ejemplo, el instalador solicita automáticamente un reinicio si es necesario reemplazar los archivos que se usan durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="11448-109">For example, the installer automatically prompts for a restart if it needs to replace any files in use during the installation.</span></span>

<span data-ttu-id="11448-110">Puede suprimir determinados mensajes para los reinicios si establece la propiedad **reboot** como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="11448-110">You can suppress certain prompts for restarts by setting the **REBOOT** property as follows.</span></span>



| <span data-ttu-id="11448-111">Valor de reinicio</span><span class="sxs-lookup"><span data-stu-id="11448-111">REBOOT value</span></span>   | <span data-ttu-id="11448-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="11448-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11448-113">Force</span><span class="sxs-lookup"><span data-stu-id="11448-113">Force</span></span>          | <span data-ttu-id="11448-114">Pida siempre un reinicio al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="11448-114">Always prompt for a restart at the end of the installation.</span></span> <span data-ttu-id="11448-115">La interfaz de usuario siempre solicita al usuario una opción para reiniciarla al final.</span><span class="sxs-lookup"><span data-stu-id="11448-115">The UI always prompts the user with an option to restart at the end.</span></span> <span data-ttu-id="11448-116">Si no hay ninguna interfaz de usuario y no se trata de una [instalación de varios paquetes](multiple-package-installations.md), el sistema se reiniciará automáticamente al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="11448-116">If there is no user interface, and this is not a [multiple-package installation](multiple-package-installations.md), the system automatically restarts at the end of the installation.</span></span> <span data-ttu-id="11448-117">Si se trata de una instalación de varios paquetes, no se reinicia automáticamente el sistema y el instalador devuelve el ERROR \_ se \_ requiere un reinicio correcto \_ .</span><span class="sxs-lookup"><span data-stu-id="11448-117">If this is a multiple-package installation, there is no automatic restart of the system and the installer returns ERROR\_SUCCESS\_REBOOT\_REQUIRED.</span></span> |
| <span data-ttu-id="11448-118">Suprimir</span><span class="sxs-lookup"><span data-stu-id="11448-118">Suppress</span></span>       | <span data-ttu-id="11448-119">Suprima los mensajes para un reinicio al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="11448-119">Suppress prompts for a restart at the end of the installation.</span></span> <span data-ttu-id="11448-120">El instalador sigue solicitando al usuario que se reinicie durante la instalación cada vez que encuentra la [acción ForceReboot](forcereboot-action.md).</span><span class="sxs-lookup"><span data-stu-id="11448-120">The installer still prompts the user with an option to restart during the installation whenever it encounters the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="11448-121">Si no hay ninguna interfaz de usuario, el sistema se reinicia automáticamente en cada ForceReboot.</span><span class="sxs-lookup"><span data-stu-id="11448-121">If there is no user interface, the system automatically restarts at each ForceReboot.</span></span> <span data-ttu-id="11448-122">Los reinicios al final de la instalación (por ejemplo, debido a un intento de instalar un archivo en uso) se suprimen.</span><span class="sxs-lookup"><span data-stu-id="11448-122">Restarts at the end of the installation (for example, caused by an attempt to install a file in use) are suppressed.</span></span>                                    |
| <span data-ttu-id="11448-123">ReallySuppress</span><span class="sxs-lookup"><span data-stu-id="11448-123">ReallySuppress</span></span> | <span data-ttu-id="11448-124">Suprimir todos los reinicios y reiniciar los mensajes iniciados por ForceReboot durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="11448-124">Suppress all restarts and restart prompts initiated by ForceReboot during the installation.</span></span> <span data-ttu-id="11448-125">Suprima todos los reinicios y los mensajes de reinicio al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="11448-125">Suppress all restarts and restart prompts at the end of the installation.</span></span> <span data-ttu-id="11448-126">Se suprimen el mensaje de reinicio y el reinicio.</span><span class="sxs-lookup"><span data-stu-id="11448-126">Both the restart prompt and the restart itself are suppressed.</span></span> <span data-ttu-id="11448-127">Por ejemplo, los reinicios al final de la instalación, causados por un intento de instalar un archivo en uso, se suprimen.</span><span class="sxs-lookup"><span data-stu-id="11448-127">For example, restarts at the end of the installation, caused by an attempt to install a file in use, are suppressed.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="11448-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11448-128">Remarks</span></span>

<span data-ttu-id="11448-129">El instalador solo evalúa el primer carácter de la propiedad de **reinicio** .</span><span class="sxs-lookup"><span data-stu-id="11448-129">The installer only evaluates the first character of the **REBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="11448-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11448-130">Requirements</span></span>



| <span data-ttu-id="11448-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="11448-131">Requirement</span></span> | <span data-ttu-id="11448-132">Value</span><span class="sxs-lookup"><span data-stu-id="11448-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11448-133">Versión</span><span class="sxs-lookup"><span data-stu-id="11448-133">Version</span></span><br/> | <span data-ttu-id="11448-134">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="11448-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="11448-135">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11448-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="11448-136">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="11448-136">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="11448-137">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="11448-137">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11448-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="11448-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11448-139">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11448-139">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="11448-140">**Propiedad REBOOTPROMPT**</span><span class="sxs-lookup"><span data-stu-id="11448-140">**REBOOTPROMPT Property**</span></span>](rebootprompt.md)
</dt> <dt>

[<span data-ttu-id="11448-141">Reinicios del sistema</span><span class="sxs-lookup"><span data-stu-id="11448-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




