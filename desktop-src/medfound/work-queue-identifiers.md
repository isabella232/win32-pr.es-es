---
description: Las constantes siguientes identifican las colas de trabajo de Media Foundation estándar.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Identificadores de cola de trabajo (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecff594bad2a4595862f0bc6457644f86949d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667579"
---
# <a name="work-queue-identifiers"></a><span data-ttu-id="91297-103">Identificadores de cola de trabajo</span><span class="sxs-lookup"><span data-stu-id="91297-103">Work Queue Identifiers</span></span>

<span data-ttu-id="91297-104">Las constantes siguientes identifican las colas de trabajo de Media Foundation estándar.</span><span class="sxs-lookup"><span data-stu-id="91297-104">The following constants identify the standard Media Foundation work queues.</span></span>

<span data-ttu-id="91297-105">Las aplicaciones deben usar \_ \_ la cola \_ de devolución de llamada de MFASYNC multiproceso o usar una cola de trabajo obtenida de [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) si desean controlar la prioridad de ejecución.</span><span class="sxs-lookup"><span data-stu-id="91297-105">Applications should use MFASYNC\_CALLBACK\_QUEUE\_MULTITHREADED or use a work queue obtained from [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) if they want to control the execution priority.</span></span> <span data-ttu-id="91297-106">Tenga en cuenta que las prioridades de la cola de trabajo de la plataforma predeterminada pueden cambiar dinámicamente cuando una aplicación llama a [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss).</span><span class="sxs-lookup"><span data-stu-id="91297-106">Note that the default platform work queue priorities can dynamically change when an application calls [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss).</span></span> <span data-ttu-id="91297-107">Para obtener más información acerca de las colas de trabajos, consulte [colas de trabajo](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="91297-107">For more information about work queues, see [Work Queues](work-queues.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="91297-108">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="91297-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="91297-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="91297-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl> <span data-ttu-id="91297-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="91297-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="91297-111">En la mayoría de los casos, las aplicaciones deben utilizar <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span><span class="sxs-lookup"><span data-stu-id="91297-111">In most cases, applications should use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/> <span data-ttu-id="91297-112">Esta cola de trabajo se utiliza para las operaciones sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="91297-112">This work queue is used for synchronous operations.</span></span> <span data-ttu-id="91297-113">El uso de la cola de trabajo estándar puede correr el riesgo de interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="91297-113">Using the standard work queue may run the risk of deadlocking.</span></span> <span data-ttu-id="91297-114">Las aplicaciones pueden crear una cola sincrónica privada sobre la cola multiproceso mediante <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="91297-114">Applications can create a private synchronous queue on top of the multithreaded queue by using <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl> <span data-ttu-id="91297-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="91297-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="91297-116">No es para uso general de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="91297-116">Not for general application use.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl> <span data-ttu-id="91297-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span><span class="sxs-lookup"><span data-stu-id="91297-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="91297-118">No es para uso general de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="91297-118">Not for general application use.</span></span><br/> <span data-ttu-id="91297-119">Esta cola de trabajo se usa internamente para operaciones de e/s, como la lectura de archivos y la lectura de la red.</span><span class="sxs-lookup"><span data-stu-id="91297-119">This work queue is used internally for I/O operations such as reading files and reading from the network.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl> <span data-ttu-id="91297-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="91297-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="91297-121">No es para uso general de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="91297-121">Not for general application use.</span></span><br/> <span data-ttu-id="91297-122">Esta cola de trabajo se utiliza para las devoluciones de llamada periódicas y los elementos de trabajo programados.</span><span class="sxs-lookup"><span data-stu-id="91297-122">This work queue is used for periodic callbacks and scheduled work items.</span></span> <span data-ttu-id="91297-123">Las siguientes funciones colocan los elementos de trabajo en esta cola:</span><span class="sxs-lookup"><span data-stu-id="91297-123">The following functions put work items in this queue:</span></span><br/>
<ul>
<li><span data-ttu-id="91297-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="91297-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></span></span></li>
<li><span data-ttu-id="91297-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="91297-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></span></span></li>
<li><span data-ttu-id="91297-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="91297-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl> <span data-ttu-id="91297-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span><span class="sxs-lookup"><span data-stu-id="91297-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="91297-128">En la mayoría de los casos, se debe usar esta cola de trabajo multiproceso.</span><span class="sxs-lookup"><span data-stu-id="91297-128">This multithreaded work queue should be used in most cases.</span></span> <br/> <span data-ttu-id="91297-129">Esta cola de trabajo se utiliza para las operaciones asincrónicas en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="91297-129">This work queue is used for asynchronous operations throughout Media Foundation.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl> <span data-ttu-id="91297-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span><span class="sxs-lookup"><span data-stu-id="91297-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="91297-131">No es para uso general de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="91297-131">Not for general application use.</span></span> <span data-ttu-id="91297-132">En su lugar, las aplicaciones deben usar <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span><span class="sxs-lookup"><span data-stu-id="91297-132">Applications should instead use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="91297-133">Además, se usan las siguientes constantes en relación con las colas de trabajos.</span><span class="sxs-lookup"><span data-stu-id="91297-133">In addition, the following constants are used in connection with work queues.</span></span>



| <span data-ttu-id="91297-134">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="91297-134">Constant/value</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="91297-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="91297-135">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <span data-ttu-id="91297-136"><dt>**MFASYNC \_ Cola de devolución de llamada no \_ \_ definida**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="91297-136"><dt>**MFASYNC\_CALLBACK\_QUEUE\_UNDEFINED**</dt> <dt>0x00000000</dt></span></span> </dl>           | <span data-ttu-id="91297-137">Cola de trabajo no definida.</span><span class="sxs-lookup"><span data-stu-id="91297-137">Undefined work queue.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <span data-ttu-id="91297-138"><dt>**MFASYNC \_ \_ \_ \_ Máscara privada de cola de devolución de llamada**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="91297-138"><dt>**MFASYNC\_CALLBACK\_QUEUE\_PRIVATE\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl> | <span data-ttu-id="91297-139">Máscara de bits para distinguir las colas de trabajo de plataforma de las creadas mediante una llamada a [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span><span class="sxs-lookup"><span data-stu-id="91297-139">Bit mask to distinguish platform work queues from those created by calling [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span><br/> <span data-ttu-id="91297-140">Para una cola de trabajo creada por [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), el siguiente valor es distinto de cero:</span><span class="sxs-lookup"><span data-stu-id="91297-140">For a work queue created by [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), the following value is nonzero:</span></span><br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <span data-ttu-id="91297-141"><dt>**MFASYNC \_ Cola de devolución de llamada \_ \_ todos**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="91297-141"><dt>**MFASYNC\_CALLBACK\_QUEUE\_ALL**</dt> <dt>0xFFFFFFFF</dt></span></span> </dl>                             | <span data-ttu-id="91297-142">Todas las colas de trabajo de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="91297-142">All platform work queues.</span></span><br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="91297-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91297-143">Requirements</span></span>



| <span data-ttu-id="91297-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="91297-144">Requirement</span></span> | <span data-ttu-id="91297-145">Value</span><span class="sxs-lookup"><span data-stu-id="91297-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91297-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91297-146">Minimum supported client</span></span><br/> | <span data-ttu-id="91297-147">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="91297-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="91297-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91297-148">Minimum supported server</span></span><br/> | <span data-ttu-id="91297-149">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="91297-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="91297-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91297-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="91297-151"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91297-151"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91297-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="91297-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91297-153">Constantes de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="91297-153">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> <dt>

[<span data-ttu-id="91297-154">Colas de trabajo</span><span class="sxs-lookup"><span data-stu-id="91297-154">Work Queues</span></span>](work-queues.md)
</dt> <dt>

[<span data-ttu-id="91297-155">Mejoras en la cola de trabajo y subprocesos</span><span class="sxs-lookup"><span data-stu-id="91297-155">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




