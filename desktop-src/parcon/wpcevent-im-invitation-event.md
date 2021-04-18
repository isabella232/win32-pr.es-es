---
description: Evento por usuario proporcionado para el inicio de sesión de las conversaciones por parte de clientes de mensajería instantánea.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: Evento WPCEVENT_IM_INVITATION (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c9d7e90eaa901b5e18a072e03e3112ee8c2934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716669"
---
# <a name="wpcevent_im_invitation-event"></a><span data-ttu-id="ce806-103">Evento de invitación de WPCEVENT \_ im \_</span><span class="sxs-lookup"><span data-stu-id="ce806-103">WPCEVENT\_IM\_INVITATION event</span></span>

<span data-ttu-id="ce806-104">Evento por usuario proporcionado para el inicio de sesión de las conversaciones por parte de clientes de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="ce806-104">Per-user event provided for logging initiation of conversations by Instant Messaging clients.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="ce806-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce806-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce806-106">*AppName*</span><span class="sxs-lookup"><span data-stu-id="ce806-106">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="ce806-107">El nombre de la aplicación que está generando el evento.</span><span class="sxs-lookup"><span data-stu-id="ce806-107">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="ce806-108">*Versiónaplicación*</span><span class="sxs-lookup"><span data-stu-id="ce806-108">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="ce806-109">La cadena de versión de la aplicación que está generando el evento.</span><span class="sxs-lookup"><span data-stu-id="ce806-109">The version string for the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="ce806-110">*AccountName*</span><span class="sxs-lookup"><span data-stu-id="ce806-110">*AccountName*</span></span> 
</dt> <dd>

<span data-ttu-id="ce806-111">Cadena de identidad de la cuenta de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="ce806-111">The instant messaging account identity string.</span></span>

</dd> <dt>

<span data-ttu-id="ce806-112">*ConvID*</span><span class="sxs-lookup"><span data-stu-id="ce806-112">*ConvID*</span></span> 
</dt> <dd>

<span data-ttu-id="ce806-113">Identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="ce806-113">The identifier for the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="ce806-114">*RequestingIP*</span><span class="sxs-lookup"><span data-stu-id="ce806-114">*RequestingIP*</span></span> 
</dt> <dd>

<span data-ttu-id="ce806-115">Cadena que contiene la dirección IP del equipo que envía la invitación.</span><span class="sxs-lookup"><span data-stu-id="ce806-115">A string that contains the IP address of the computer that is sending the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="ce806-116">*Sender*</span><span class="sxs-lookup"><span data-stu-id="ce806-116">*Sender*</span></span> 
</dt> <dd>

<span data-ttu-id="ce806-117">La cadena de identidad de la cuenta de mensajería instantánea para la cuenta que emite la invitación.</span><span class="sxs-lookup"><span data-stu-id="ce806-117">The instant messaging account identity string for the account that is issuing the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="ce806-118">*Motivo*</span><span class="sxs-lookup"><span data-stu-id="ce806-118">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="ce806-119">Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ce806-119">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="ce806-120">*RecipCount*</span><span class="sxs-lookup"><span data-stu-id="ce806-120">*RecipCount*</span></span> 
</dt> <dd>

<span data-ttu-id="ce806-121">El número de destinatarios que reciben la invitación y que tienen identidades definidas en el campo de destinatario.</span><span class="sxs-lookup"><span data-stu-id="ce806-121">The count of recipients who are receiving the invitation and who have identities defined in the recipient field.</span></span>

</dd> <dt>

<span data-ttu-id="ce806-122">*Recipient*</span><span class="sxs-lookup"><span data-stu-id="ce806-122">*Recipient*</span></span> 
</dt> <dd>

<span data-ttu-id="ce806-123">Una cadena delimitada que contiene cadenas de identidad de la cuenta de mensajería instantánea para los destinatarios de la invitación.</span><span class="sxs-lookup"><span data-stu-id="ce806-123">A delimited string that contains instant messaging account identity strings for the recipients of the invitation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce806-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce806-124">Requirements</span></span>



| <span data-ttu-id="ce806-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce806-125">Requirement</span></span> | <span data-ttu-id="ce806-126">Value</span><span class="sxs-lookup"><span data-stu-id="ce806-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce806-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce806-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ce806-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ce806-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce806-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce806-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ce806-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ce806-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="ce806-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce806-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce806-132"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce806-132"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce806-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce806-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce806-134">Uso de las API de registro para controles parentales</span><span class="sxs-lookup"><span data-stu-id="ce806-134">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="ce806-135">**WPC \_ args \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="ce806-135">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




