---
description: Esta clase es la clase primaria para los eventos de llamada a procedimiento local avanzados. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: ALPC (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2a4b09a8bab9280de8fb4c91368f5d6d93f7944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984523"
---
# <a name="alpc-class"></a><span data-ttu-id="d7a07-104">ALPC (clase)</span><span class="sxs-lookup"><span data-stu-id="d7a07-104">ALPC class</span></span>

<span data-ttu-id="d7a07-105">Esta clase es la clase primaria para los eventos de llamada a procedimiento local avanzados.</span><span class="sxs-lookup"><span data-stu-id="d7a07-105">This class is the parent class for advanced local procedure call events.</span></span>

<span data-ttu-id="d7a07-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="d7a07-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7a07-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7a07-107">Syntax</span></span>

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="d7a07-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7a07-108">Members</span></span>

<span data-ttu-id="d7a07-109">La clase **ALPC** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="d7a07-109">The **ALPC** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7a07-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7a07-110">Remarks</span></span>

<span data-ttu-id="d7a07-111">Para habilitar los eventos de llamada a procedimiento local avanzado en una sesión de registro del kernel de NT, especifique la marca de **seguimiento de eventos \_ \_ \_ ALPC** en el miembro **EnableFlags** de una estructura de propiedades de [**\_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="d7a07-111">To enable advanced local procedure call events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_ALPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="d7a07-112">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos ALPC llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**ALPCGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="d7a07-112">Event trace consumers can implement special processing for ALPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ALPCGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="d7a07-113">Use los siguientes tipos de eventos para identificar el evento ALPC real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="d7a07-113">Use the following event types to identify the actual ALPC event when consuming events.</span></span>



| <span data-ttu-id="d7a07-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="d7a07-114">Event type</span></span>           | <span data-ttu-id="d7a07-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7a07-115">Description</span></span>                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a07-116">Valor del tipo de evento, 33</span><span class="sxs-lookup"><span data-stu-id="d7a07-116">Event type value, 33</span></span> | <span data-ttu-id="d7a07-117">Enviar evento de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7a07-117">Send message event.</span></span> <span data-ttu-id="d7a07-118">La clase MOF de [**\_ envío de \_ mensaje ALPC**](alpc-send-message.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d7a07-118">The [**ALPC\_Send\_Message**](alpc-send-message.md) MOF class defines the event data for this event.</span></span>                           |
| <span data-ttu-id="d7a07-119">Valor del tipo de evento, 34</span><span class="sxs-lookup"><span data-stu-id="d7a07-119">Event type value, 34</span></span> | <span data-ttu-id="d7a07-120">Evento Receive Message.</span><span class="sxs-lookup"><span data-stu-id="d7a07-120">Receive message event.</span></span> <span data-ttu-id="d7a07-121">La clase MOF de [**\_ recepción de \_ mensajes ALPC**](alpc-receive-message.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d7a07-121">The [**ALPC\_Receive\_Message**](alpc-receive-message.md) MOF class defines the event data for this event.</span></span>                  |
| <span data-ttu-id="d7a07-122">Valor del tipo de evento, 35</span><span class="sxs-lookup"><span data-stu-id="d7a07-122">Event type value, 35</span></span> | <span data-ttu-id="d7a07-123">Evento wait for reply.</span><span class="sxs-lookup"><span data-stu-id="d7a07-123">Wait for reply event.</span></span> <span data-ttu-id="d7a07-124">La clase del MOF [**\_ Wait \_ for \_ reply de ALPC**](alpc-wait-for-reply.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d7a07-124">The [**ALPC\_Wait\_For\_Reply**](alpc-wait-for-reply.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="d7a07-125">Valor del tipo de evento, 36</span><span class="sxs-lookup"><span data-stu-id="d7a07-125">Event type value, 36</span></span> | <span data-ttu-id="d7a07-126">Esperar un nuevo evento de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7a07-126">Wait for new message event.</span></span> <span data-ttu-id="d7a07-127">La clase MOF [**\_ Wait \_ for \_ New \_ Message**](alpc-wait-for-new-message.md) mof define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d7a07-127">The [**ALPC\_Wait\_For\_New\_Message**](alpc-wait-for-new-message.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="d7a07-128">Valor del tipo de evento, 37</span><span class="sxs-lookup"><span data-stu-id="d7a07-128">Event type value, 37</span></span> | <span data-ttu-id="d7a07-129">Detener evento en espera.</span><span class="sxs-lookup"><span data-stu-id="d7a07-129">Stop waiting event.</span></span> <span data-ttu-id="d7a07-130">La clase de MOF [**\_ unwait de ALPC**](alpc-unwait.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="d7a07-130">The [**ALPC\_Unwait**](alpc-unwait.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="d7a07-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7a07-131">Requirements</span></span>



| <span data-ttu-id="d7a07-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7a07-132">Requirement</span></span> | <span data-ttu-id="d7a07-133">Value</span><span class="sxs-lookup"><span data-stu-id="d7a07-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d7a07-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7a07-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a07-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d7a07-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d7a07-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7a07-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a07-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7a07-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

