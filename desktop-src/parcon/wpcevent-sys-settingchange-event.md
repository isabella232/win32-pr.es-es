---
description: Evento de nivel de sistema generado en un cambio de configuración de controles parentales.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: Evento WPCEVENT_SYS_SETTINGCHANGE (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716947"
---
# <a name="wpcevent_sys_settingchange-event"></a><span data-ttu-id="6fe1b-103">WPCEVENT \_ Sys \_ SETTINGCHANGE</span><span class="sxs-lookup"><span data-stu-id="6fe1b-103">WPCEVENT\_SYS\_SETTINGCHANGE event</span></span>

<span data-ttu-id="6fe1b-104">Evento de nivel de sistema generado en un cambio de configuración de controles parentales.</span><span class="sxs-lookup"><span data-stu-id="6fe1b-104">System-level event generated on a Parental Controls setting change.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a><span data-ttu-id="6fe1b-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6fe1b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe1b-106">*Clase*</span><span class="sxs-lookup"><span data-stu-id="6fe1b-106">*Class*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe1b-107">La clase que está generando el evento.</span><span class="sxs-lookup"><span data-stu-id="6fe1b-107">The class that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="6fe1b-108">*Configuración*</span><span class="sxs-lookup"><span data-stu-id="6fe1b-108">*Setting*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe1b-109">Un valor de la enumeración de **\_ configuración WPC** .</span><span class="sxs-lookup"><span data-stu-id="6fe1b-109">A value of the **WPC\_SETTINGS** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="6fe1b-110">*Propietario*</span><span class="sxs-lookup"><span data-stu-id="6fe1b-110">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe1b-111">El identificador de seguridad del usuario que está generando el evento.</span><span class="sxs-lookup"><span data-stu-id="6fe1b-111">The security identifier of the user who is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="6fe1b-112">*OldVal*</span><span class="sxs-lookup"><span data-stu-id="6fe1b-112">*OldVal*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe1b-113">Valor anterior de esta configuración, si se elimina o se cambia.</span><span class="sxs-lookup"><span data-stu-id="6fe1b-113">The previous value of this setting, if deleted or changed.</span></span>

</dd> <dt>

<span data-ttu-id="6fe1b-114">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="6fe1b-114">*NewVal*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe1b-115">Nuevo valor de esta configuración, si se ha agregado o cambiado.</span><span class="sxs-lookup"><span data-stu-id="6fe1b-115">The new value of this setting, if added or changed.</span></span>

</dd> <dt>

<span data-ttu-id="6fe1b-116">*Motivo*</span><span class="sxs-lookup"><span data-stu-id="6fe1b-116">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe1b-117">Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.</span><span class="sxs-lookup"><span data-stu-id="6fe1b-117">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="6fe1b-118">*Opcional*</span><span class="sxs-lookup"><span data-stu-id="6fe1b-118">*Optional*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe1b-119">Un campo opcional.</span><span class="sxs-lookup"><span data-stu-id="6fe1b-119">An optional field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fe1b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fe1b-120">Requirements</span></span>



| <span data-ttu-id="6fe1b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fe1b-121">Requirement</span></span> | <span data-ttu-id="6fe1b-122">Value</span><span class="sxs-lookup"><span data-stu-id="6fe1b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe1b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fe1b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6fe1b-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6fe1b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6fe1b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fe1b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6fe1b-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6fe1b-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="6fe1b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fe1b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fe1b-128"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fe1b-128"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fe1b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fe1b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe1b-130">Uso de las API de registro para controles parentales</span><span class="sxs-lookup"><span data-stu-id="6fe1b-130">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="6fe1b-131">**WPC \_ args \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="6fe1b-131">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




