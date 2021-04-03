---
description: Evento de seguimiento de red Winsock para la operación de cierre del socket.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: Evento AFD_EVENT_CLOSE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: fbc6c63a3084db6a9be0a4b4ea7672d84881a29a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809764"
---
# <a name="afd_event_close-event"></a><span data-ttu-id="152dd-103">Evento de cierre de \_ evento de AFD \_</span><span class="sxs-lookup"><span data-stu-id="152dd-103">AFD\_EVENT\_CLOSE event</span></span>

<span data-ttu-id="152dd-104">El evento de **\_ \_ cierre de evento de AFD** es un evento de seguimiento de la red Winsock para la operación de cierre del socket.</span><span class="sxs-lookup"><span data-stu-id="152dd-104">The **AFD\_EVENT\_CLOSE** event is a Winsock network tracing event for socket close operation.</span></span>


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a><span data-ttu-id="152dd-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="152dd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="152dd-106">*EnterExit*</span><span class="sxs-lookup"><span data-stu-id="152dd-106">*EnterExit*</span></span> 
</dt> <dd>

<span data-ttu-id="152dd-107">Información sobre este evento.</span><span class="sxs-lookup"><span data-stu-id="152dd-107">Information on this event.</span></span>

<span data-ttu-id="152dd-108">En la tabla siguiente se enumeran los posibles valores para el parámetro *EnterExit* :</span><span class="sxs-lookup"><span data-stu-id="152dd-108">The following table lists the possible values for the *EnterExit* parameter:</span></span>



| <span data-ttu-id="152dd-109">Value</span><span class="sxs-lookup"><span data-stu-id="152dd-109">Value</span></span>                                                                        | <span data-ttu-id="152dd-110">Significado</span><span class="sxs-lookup"><span data-stu-id="152dd-110">Meaning</span></span>                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="152dd-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="152dd-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="152dd-112">Inicio de una solicitud Winsock.</span><span class="sxs-lookup"><span data-stu-id="152dd-112">The start of a Winsock request.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="152dd-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="152dd-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="152dd-114">Se completó la solicitud Winsock.</span><span class="sxs-lookup"><span data-stu-id="152dd-114">The Winsock request completed.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="152dd-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="152dd-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="152dd-116">El controlador Winsock AFD llevó a cabo una acción interna (anulando una conexión, por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="152dd-116">The Winsock AFD driver took an internal action (aborting a connection, for example).</span></span><br/>      |
| <dl> <span data-ttu-id="152dd-117"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="152dd-117"><dt>3</dt></span></span> </dl> | <span data-ttu-id="152dd-118">El controlador TCP/IP hizo que se produjera este evento.</span><span class="sxs-lookup"><span data-stu-id="152dd-118">The TCP/IP driver caused this event to occur.</span></span> <span data-ttu-id="152dd-119">Normalmente, esto indica una notificación de datos.</span><span class="sxs-lookup"><span data-stu-id="152dd-119">This usually indicates a data notification.</span></span><br/> |
| <dl> <span data-ttu-id="152dd-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="152dd-120"><dt>4</dt></span></span> </dl> | <span data-ttu-id="152dd-121">El controlador Winsock AFD hizo que se produjera este evento (por ejemplo, si se establece una opción de socket).</span><span class="sxs-lookup"><span data-stu-id="152dd-121">The Winsock AFD driver caused this event to occur (setting a socket option, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="152dd-122">*Ubicación*</span><span class="sxs-lookup"><span data-stu-id="152dd-122">*Location*</span></span> 
</dt> <dd>

<span data-ttu-id="152dd-123">Campo privado que se usa internamente.</span><span class="sxs-lookup"><span data-stu-id="152dd-123">A private field used internally.</span></span>

</dd> <dt>

<span data-ttu-id="152dd-124">*Proceso*</span><span class="sxs-lookup"><span data-stu-id="152dd-124">*Process*</span></span> 
</dt> <dd>

<span data-ttu-id="152dd-125">La dirección [EPROCESS](/windows-hardware/drivers/kernel/eprocess) del proceso que posee el socket relacionado.</span><span class="sxs-lookup"><span data-stu-id="152dd-125">The [EPROCESS](/windows-hardware/drivers/kernel/eprocess) address of the process that owns the related socket.</span></span> <span data-ttu-id="152dd-126">Se trata de una estructura opaca que actúa como el objeto de proceso de un proceso.</span><span class="sxs-lookup"><span data-stu-id="152dd-126">This is an opaque structure that serves as the process object for a process.</span></span> <span data-ttu-id="152dd-127">Para obtener más información, consulte la documentación del kit de controladores de Windows para la estructura [EPROCESS](/windows-hardware/drivers/kernel/eprocess) .</span><span class="sxs-lookup"><span data-stu-id="152dd-127">For more information, see the Windows Driver Kit documentation for the [EPROCESS](/windows-hardware/drivers/kernel/eprocess) structure.</span></span>

</dd> <dt>

<span data-ttu-id="152dd-128">*Punto de conexión*</span><span class="sxs-lookup"><span data-stu-id="152dd-128">*Endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="152dd-129">Dirección del \_ punto de conexión de AFD del socket.</span><span class="sxs-lookup"><span data-stu-id="152dd-129">The AFD\_ENDPOINT address of the socket.</span></span>

</dd> <dt>

<span data-ttu-id="152dd-130">*Estado*</span><span class="sxs-lookup"><span data-stu-id="152dd-130">*Status*</span></span> 
</dt> <dd>

<span data-ttu-id="152dd-131">Código NTSTATUS de la operación.</span><span class="sxs-lookup"><span data-stu-id="152dd-131">The NTSTATUS code for the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="152dd-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="152dd-132">Remarks</span></span>

<span data-ttu-id="152dd-133">Se realiza un seguimiento del evento de **\_ \_ cierre de evento de AFD** para que una operación de red Winsock cierre un socket.</span><span class="sxs-lookup"><span data-stu-id="152dd-133">The **AFD\_EVENT\_CLOSE** event is traced for a Winsock network operation to close a socket.</span></span> <span data-ttu-id="152dd-134">El canal de este evento es Winsock-AFD.</span><span class="sxs-lookup"><span data-stu-id="152dd-134">The channel for this event is Winsock-AFD.</span></span> <span data-ttu-id="152dd-135">El nivel de este evento es informativo.</span><span class="sxs-lookup"><span data-stu-id="152dd-135">The level for this event is informational.</span></span>

## <a name="requirements"></a><span data-ttu-id="152dd-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="152dd-136">Requirements</span></span>



| <span data-ttu-id="152dd-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="152dd-137">Requirement</span></span> | <span data-ttu-id="152dd-138">Value</span><span class="sxs-lookup"><span data-stu-id="152dd-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="152dd-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="152dd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="152dd-140">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="152dd-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="152dd-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="152dd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="152dd-142">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="152dd-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="152dd-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="152dd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152dd-144">Control de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="152dd-144">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="152dd-145">**descriptor de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="152dd-145">**EVENT\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[<span data-ttu-id="152dd-146">Seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="152dd-146">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="152dd-147">Niveles de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="152dd-147">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="152dd-148">Detalles de seguimiento de cambios de catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="152dd-148">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

