---
description: Especifica un identificador de tarea del servicio Programador de clases multimedia (MMCSS) para una bifurcación de topología.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: MF_TOPONODE_WORKQUEUE_MMCSS_TASKID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53af119c58d725d42ec5737ffd9bf96286a65ac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543238"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a><span data-ttu-id="e93ff-103">MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ atributo TASKID</span><span class="sxs-lookup"><span data-stu-id="e93ff-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID attribute</span></span>

<span data-ttu-id="e93ff-104">Especifica un identificador de tarea del servicio Programador de clases multimedia (MMCSS) para una bifurcación de topología.</span><span class="sxs-lookup"><span data-stu-id="e93ff-104">Specifies a Multimedia Class Scheduler Service (MMCSS) task identifier for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="e93ff-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e93ff-105">Data type</span></span>

<span data-ttu-id="e93ff-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e93ff-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e93ff-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e93ff-107">Remarks</span></span>

<span data-ttu-id="e93ff-108">Este atributo se aplica a los nodos de origen (**\_ \_ \_ nodo SOURCESTREAM de topología MF**).</span><span class="sxs-lookup"><span data-stu-id="e93ff-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="e93ff-109">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="e93ff-109">This attribute is optional.</span></span>

<span data-ttu-id="e93ff-110">Este atributo se omite a menos que también se establezcan los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="e93ff-110">This attribute is ignored unless the following attributes are also set:</span></span>

-   [<span data-ttu-id="e93ff-111">**identificador de WORKQUEUE de MF \_ TOPONODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e93ff-111">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
-   [<span data-ttu-id="e93ff-112">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS ( \_ clase)**</span><span class="sxs-lookup"><span data-stu-id="e93ff-112">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)

<span data-ttu-id="e93ff-113">Si la aplicación registra uno de sus propios subprocesos con MMCSS, puede usar este atributo para asociar la cola de trabajo de topología al grupo MMCSS de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e93ff-113">If the application registers one of its own threads with MMCSS, you can use this attribute to associate the topology work queue with the application's MMCSS group.</span></span> <span data-ttu-id="e93ff-114">Establezca el valor de atributo igual al identificador de tarea que recibió la aplicación cuando se registró con MMCSS.</span><span class="sxs-lookup"><span data-stu-id="e93ff-114">Set the attribute value equal to the task identifier that the application received when it registered with MMCSS.</span></span> <span data-ttu-id="e93ff-115">(El identificador de tarea se devuelve en el parámetro *TaskIndex* de la función [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) .</span><span class="sxs-lookup"><span data-stu-id="e93ff-115">(The task identifier is returned in the *TaskIndex* parameter of the [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) function.</span></span> <span data-ttu-id="e93ff-116">Para obtener más información, vea el tema [Process and Thread Functions](../procthread/process-and-thread-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="e93ff-116">For more information, see the topic [Process and Thread Functions](../procthread/process-and-thread-functions.md).)</span></span>

<span data-ttu-id="e93ff-117">Si desea que MMCSS asigne un nuevo identificador de tarea para la topología, establezca el atributo de [**\_ clase MF TOPONODE \_ WORKQUEUE \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md) , pero no establezca el atributo **MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID** .</span><span class="sxs-lookup"><span data-stu-id="e93ff-117">If you want MMCSS to assign a new task identifier for the topology, set the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute, but do not set the **MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID** attribute.</span></span>

<span data-ttu-id="e93ff-118">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e93ff-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e93ff-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e93ff-119">Requirements</span></span>



| <span data-ttu-id="e93ff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e93ff-120">Requirement</span></span> | <span data-ttu-id="e93ff-121">Value</span><span class="sxs-lookup"><span data-stu-id="e93ff-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e93ff-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e93ff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e93ff-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e93ff-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e93ff-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e93ff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e93ff-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e93ff-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e93ff-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e93ff-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e93ff-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e93ff-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e93ff-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e93ff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e93ff-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e93ff-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e93ff-130">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e93ff-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e93ff-131">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e93ff-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e93ff-132">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="e93ff-132">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e93ff-133">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="e93ff-133">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="e93ff-134">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="e93ff-134">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="e93ff-135">Colas de trabajo</span><span class="sxs-lookup"><span data-stu-id="e93ff-135">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
