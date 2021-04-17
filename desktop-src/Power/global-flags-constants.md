---
description: Las constantes de las marcas globales se utilizan para habilitar o deshabilitar las opciones de directiva de energía de usuario.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Constantes de marcas globales (PowrProf. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd31340e3e7daf4f9dd034c3fa2db333680a626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667214"
---
# <a name="global-flags-constants"></a><span data-ttu-id="c102d-103">Constantes de marcas globales</span><span class="sxs-lookup"><span data-stu-id="c102d-103">Global Flags Constants</span></span>

<span data-ttu-id="c102d-104">Las constantes de las marcas globales se utilizan para habilitar o deshabilitar las opciones de directiva de energía de usuario.</span><span class="sxs-lookup"><span data-stu-id="c102d-104">The global flags constants are used to enable or disable user power policy options.</span></span>



| <span data-ttu-id="c102d-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="c102d-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="c102d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c102d-106">Description</span></span>                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <span data-ttu-id="c102d-107"><dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="c102d-107"><dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="c102d-108">Habilita o deshabilita la visualización de varias baterías en el medidor de energía del sistema.</span><span class="sxs-lookup"><span data-stu-id="c102d-108">Enables or disables multiple battery display in the system Power Meter.</span></span><br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <span data-ttu-id="c102d-109"><dt>**EnablePasswordLogon**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="c102d-109"><dt>**EnablePasswordLogon**</dt> <dt>0x04</dt></span></span> </dl>                         | <span data-ttu-id="c102d-110">Habilita o deshabilita la necesidad de inicio de sesión de contraseña cuando el sistema se reanuda desde el modo de espera o hibernación.</span><span class="sxs-lookup"><span data-stu-id="c102d-110">Enables or disables requiring password logon when the system resumes from standby or hibernate.</span></span><br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <span data-ttu-id="c102d-111"><dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="c102d-111"><dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="c102d-112">Habilita o deshabilita el icono del medidor de la batería en la bandeja del sistema.</span><span class="sxs-lookup"><span data-stu-id="c102d-112">Enables or disables the battery meter icon in the system tray.</span></span> <span data-ttu-id="c102d-113">Cuando esta marca está desactivada, no se muestra el icono del medidor de la batería.</span><span class="sxs-lookup"><span data-stu-id="c102d-113">When this flag is cleared, the battery meter icon is not displayed.</span></span><br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <span data-ttu-id="c102d-114"><dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="c102d-114"><dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt></span></span> </dl>                 | <span data-ttu-id="c102d-115">Habilita o deshabilita la compatibilidad para atenuar el vídeo que se muestra cuando el sistema cambia de funcionar con corriente alterna a la energía de la batería.</span><span class="sxs-lookup"><span data-stu-id="c102d-115">Enables or disables support for dimming the video display when the system changes from running on AC power to running on battery power.</span></span><br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <span data-ttu-id="c102d-116"><dt>**EnableWakeOnRing**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="c102d-116"><dt>**EnableWakeOnRing**</dt> <dt>0x08</dt></span></span> </dl>                                     | <span data-ttu-id="c102d-117">Habilita o deshabilita la compatibilidad con Wake on Ring.</span><span class="sxs-lookup"><span data-stu-id="c102d-117">Enables or disables wake on ring support.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="c102d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c102d-118">Requirements</span></span>



| <span data-ttu-id="c102d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c102d-119">Requirement</span></span> | <span data-ttu-id="c102d-120">Value</span><span class="sxs-lookup"><span data-stu-id="c102d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c102d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c102d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c102d-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c102d-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c102d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c102d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c102d-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c102d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c102d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c102d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c102d-126"><dt>PowrProf. h</dt></span><span class="sxs-lookup"><span data-stu-id="c102d-126"><dt>PowrProf.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c102d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c102d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c102d-128">**\_Directiva de \_ energía de usuario global \_**</span><span class="sxs-lookup"><span data-stu-id="c102d-128">**GLOBAL\_USER\_POWER\_POLICY**</span></span>](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




