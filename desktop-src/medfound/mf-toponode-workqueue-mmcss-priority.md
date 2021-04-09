---
description: Especifica la prioridad relativa de subprocesos para una bifurcación de la topología.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0667c91054f8711b8825cf421a2ee565b9161f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154981"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a><span data-ttu-id="8244e-103">MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ prioridad atributo</span><span class="sxs-lookup"><span data-stu-id="8244e-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_PRIORITY attribute</span></span>

<span data-ttu-id="8244e-104">Especifica la prioridad relativa de subprocesos para una bifurcación de la topología.</span><span class="sxs-lookup"><span data-stu-id="8244e-104">Specifies the relative thread priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="8244e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8244e-105">Data type</span></span>

<span data-ttu-id="8244e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8244e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8244e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8244e-107">Remarks</span></span>

<span data-ttu-id="8244e-108">Este atributo se aplica a los nodos de origen (**\_ \_ \_ nodo SOURCESTREAM de topología MF**).</span><span class="sxs-lookup"><span data-stu-id="8244e-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="8244e-109">El atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="8244e-109">The attribute is optional.</span></span>

<span data-ttu-id="8244e-110">Este atributo requiere los atributos de clase [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) y [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) en el mismo nodo.</span><span class="sxs-lookup"><span data-stu-id="8244e-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) and [MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS](mf-toponode-workqueue-mmcss-class-attribute.md) attributes on the same node.</span></span>

<span data-ttu-id="8244e-111">El valor del atributo es la prioridad de subproceso relativa de la cola de trabajo para esta rama de la topología.</span><span class="sxs-lookup"><span data-stu-id="8244e-111">The value of the attribute is the relative thread priority of the work queue for this branch of the topology.</span></span> <span data-ttu-id="8244e-112">El [servicio Programador de clases multimedia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) utiliza la prioridad relativa cuando establece la prioridad del subproceso.</span><span class="sxs-lookup"><span data-stu-id="8244e-112">The [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) uses the relative priority when it sets the thread priority.</span></span> <span data-ttu-id="8244e-113">Para obtener más información, vea [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).</span><span class="sxs-lookup"><span data-stu-id="8244e-113">For more information, see [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).</span></span>

<span data-ttu-id="8244e-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8244e-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8244e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8244e-115">Requirements</span></span>



| <span data-ttu-id="8244e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8244e-116">Requirement</span></span> | <span data-ttu-id="8244e-117">Value</span><span class="sxs-lookup"><span data-stu-id="8244e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8244e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8244e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8244e-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8244e-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8244e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8244e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8244e-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8244e-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8244e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8244e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8244e-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8244e-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8244e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8244e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8244e-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8244e-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8244e-126">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="8244e-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="8244e-127">Mejoras en la cola de trabajo y subprocesos</span><span class="sxs-lookup"><span data-stu-id="8244e-127">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="8244e-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="8244e-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="8244e-129">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="8244e-129">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="8244e-130">**identificador de WORKQUEUE de MF \_ TOPONODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8244e-130">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="8244e-131">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**</span><span class="sxs-lookup"><span data-stu-id="8244e-131">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
