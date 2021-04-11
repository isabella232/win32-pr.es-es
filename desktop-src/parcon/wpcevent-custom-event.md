---
description: Evento por usuario que admite hasta tres campos.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: Evento WPCEVENT_CUSTOM (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276675"
---
# <a name="wpcevent_custom-event"></a><span data-ttu-id="1ad45-103">\_Evento personalizado WPCEVENT</span><span class="sxs-lookup"><span data-stu-id="1ad45-103">WPCEVENT\_CUSTOM event</span></span>

<span data-ttu-id="1ad45-104">Evento por usuario que admite hasta tres campos.</span><span class="sxs-lookup"><span data-stu-id="1ad45-104">Per-user event that supports up to three fields.</span></span>

<span data-ttu-id="1ad45-105">Los eventos se muestran en el **visor de actividades** de la **otra** sección con la siguiente jerarquía:</span><span class="sxs-lookup"><span data-stu-id="1ad45-105">Events are displayed in the **Activity Viewer** in the **Other** section with the following hierarchy:</span></span>

1.  <span data-ttu-id="1ad45-106">Publicador</span><span class="sxs-lookup"><span data-stu-id="1ad45-106">Publisher</span></span>

2.  <span data-ttu-id="1ad45-107">Application</span><span class="sxs-lookup"><span data-stu-id="1ad45-107">Application</span></span>

3.  <span data-ttu-id="1ad45-108">Evento</span><span class="sxs-lookup"><span data-stu-id="1ad45-108">Event</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="1ad45-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ad45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ad45-110">*Publicador*</span><span class="sxs-lookup"><span data-stu-id="1ad45-110">*Publisher*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad45-111">El publicador del evento (por ejemplo, un nombre de empresa).</span><span class="sxs-lookup"><span data-stu-id="1ad45-111">The publisher of the event (for example, a company name).</span></span>

</dd> <dt>

<span data-ttu-id="1ad45-112">*AppName*</span><span class="sxs-lookup"><span data-stu-id="1ad45-112">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad45-113">El nombre de la aplicación que está generando el evento.</span><span class="sxs-lookup"><span data-stu-id="1ad45-113">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="1ad45-114">*Versiónaplicación*</span><span class="sxs-lookup"><span data-stu-id="1ad45-114">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad45-115">Versión de la aplicación que está generando el evento.</span><span class="sxs-lookup"><span data-stu-id="1ad45-115">The version of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="1ad45-116">*Evento*</span><span class="sxs-lookup"><span data-stu-id="1ad45-116">*Event*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad45-117">Nombre del evento.</span><span class="sxs-lookup"><span data-stu-id="1ad45-117">The name for the event.</span></span>

</dd> <dt>

<span data-ttu-id="1ad45-118">*Value1*</span><span class="sxs-lookup"><span data-stu-id="1ad45-118">*Value1*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad45-119">Campo personalizado 1.</span><span class="sxs-lookup"><span data-stu-id="1ad45-119">Custom field 1.</span></span>

</dd> <dt>

<span data-ttu-id="1ad45-120">*Valor2*</span><span class="sxs-lookup"><span data-stu-id="1ad45-120">*Value2*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad45-121">Campo personalizado 2.</span><span class="sxs-lookup"><span data-stu-id="1ad45-121">Custom field 2.</span></span>

</dd> <dt>

<span data-ttu-id="1ad45-122">*Value3*</span><span class="sxs-lookup"><span data-stu-id="1ad45-122">*Value3*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad45-123">Campo personalizado 3.</span><span class="sxs-lookup"><span data-stu-id="1ad45-123">Custom field 3.</span></span>

</dd> <dt>

<span data-ttu-id="1ad45-124">*Bloqueado*</span><span class="sxs-lookup"><span data-stu-id="1ad45-124">*Blocked*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad45-125">Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1ad45-125">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="1ad45-126">*Motivo*</span><span class="sxs-lookup"><span data-stu-id="1ad45-126">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad45-127">Una cadena personalizada que proporciona información adicional sobre el motivo de bloqueo o no bloqueo.</span><span class="sxs-lookup"><span data-stu-id="1ad45-127">A custom string that provides extra information about the reason for blocking or not blocking.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ad45-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ad45-128">Requirements</span></span>



| <span data-ttu-id="1ad45-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ad45-129">Requirement</span></span> | <span data-ttu-id="1ad45-130">Value</span><span class="sxs-lookup"><span data-stu-id="1ad45-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad45-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ad45-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad45-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ad45-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ad45-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ad45-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad45-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1ad45-134">None supported</span></span><br/>                                                             |
| <span data-ttu-id="1ad45-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ad45-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ad45-136"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ad45-136"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ad45-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ad45-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad45-138">Uso de las API de registro para controles parentales</span><span class="sxs-lookup"><span data-stu-id="1ad45-138">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="1ad45-139">**WPC \_ args \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="1ad45-139">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




