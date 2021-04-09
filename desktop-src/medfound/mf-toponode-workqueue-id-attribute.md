---
description: Especifica una cola de trabajo para una rama de topología.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: MF_TOPONODE_WORKQUEUE_ID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9acda95895a1812f6cebbe64cbf3cd3bcdea4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154984"
---
# <a name="mf_toponode_workqueue_id-attribute"></a><span data-ttu-id="3a75a-103">MF \_ TOPONODE \_ \_ ID WORKQUEUE Attribute</span><span class="sxs-lookup"><span data-stu-id="3a75a-103">MF\_TOPONODE\_WORKQUEUE\_ID attribute</span></span>

<span data-ttu-id="3a75a-104">Especifica una cola de trabajo para una rama de topología.</span><span class="sxs-lookup"><span data-stu-id="3a75a-104">Specifies a work queue for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="3a75a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3a75a-105">Data type</span></span>

<span data-ttu-id="3a75a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3a75a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3a75a-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a75a-107">Remarks</span></span>

<span data-ttu-id="3a75a-108">Este atributo se aplica a los nodos de origen (**\_ \_ \_ nodo SOURCESTREAM de topología MF**).</span><span class="sxs-lookup"><span data-stu-id="3a75a-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="3a75a-109">El atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="3a75a-109">The attribute is optional.</span></span>

<span data-ttu-id="3a75a-110">El valor del atributo es un identificador definido por la aplicación para la cola de trabajo.</span><span class="sxs-lookup"><span data-stu-id="3a75a-110">The value of the attribute is an application-defined identifier for the work queue.</span></span>

<span data-ttu-id="3a75a-111">Las aplicaciones pueden utilizar este atributo para asignar colas de trabajo a las bifurcaciones de la topología.</span><span class="sxs-lookup"><span data-stu-id="3a75a-111">Applications can use this attribute to assign work queues to branches of the topology.</span></span> <span data-ttu-id="3a75a-112">Cada nodo de origen de la topología define una rama.</span><span class="sxs-lookup"><span data-stu-id="3a75a-112">Each source node in the topology defines one branch.</span></span> <span data-ttu-id="3a75a-113">La rama incluye todos los nodos de topología que reciben datos de ese nodo.</span><span class="sxs-lookup"><span data-stu-id="3a75a-113">The branch includes every topology node that receives data from that node.</span></span>

<span data-ttu-id="3a75a-114">Si establece este atributo, llame al método [**IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) en la topología resuelta.</span><span class="sxs-lookup"><span data-stu-id="3a75a-114">If you set this attribute, call the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method on the resolved topology.</span></span> <span data-ttu-id="3a75a-115">Varias ramas de la topología pueden compartir la misma cola de trabajo y las colas de trabajos se pueden volver a usar en las topologías.</span><span class="sxs-lookup"><span data-stu-id="3a75a-115">Multiple branches in the topology can share the same work queue, and work queues can be re-used across topologies.</span></span>

> [!Note]  
> <span data-ttu-id="3a75a-116">El valor de este atributo no es el mismo que el identificador devuelto por la función [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) .</span><span class="sxs-lookup"><span data-stu-id="3a75a-116">The value of this attribute is not the same as the identifier that is returned by the [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) function.</span></span> <span data-ttu-id="3a75a-117">El valor del atributo es un identificador definido por la aplicación y se utiliza para asociar las ramas de la topología con las colas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="3a75a-117">The value of the attribute is an application-defined identifier, and is used to associate topology branches with work queues.</span></span> <span data-ttu-id="3a75a-118">Cuando la sesión multimedia asigna una nueva cola de trabajo, almacena internamente el identificador de la cola de trabajo real.</span><span class="sxs-lookup"><span data-stu-id="3a75a-118">When the Media Session allocates a new work queue, it stores the actual work-queue identifier internally.</span></span>

 

<span data-ttu-id="3a75a-119">Si este atributo se establece, la aplicación también puede asignar la rama a una tarea del servicio de programador de clases multimedia (MMCSS) estableciendo el atributo de [**\_ clase MF TOPONODE \_ WORKQUEUE \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="3a75a-119">If this attribute it set, the application can also assign the branch to a Multimedia Class Scheduler Service (MMCSS) task, by setting the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute.</span></span>

<span data-ttu-id="3a75a-120">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3a75a-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a75a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a75a-121">Requirements</span></span>



| <span data-ttu-id="3a75a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a75a-122">Requirement</span></span> | <span data-ttu-id="3a75a-123">Value</span><span class="sxs-lookup"><span data-stu-id="3a75a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a75a-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a75a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3a75a-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3a75a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3a75a-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a75a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3a75a-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a75a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a75a-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a75a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a75a-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a75a-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a75a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a75a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a75a-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a75a-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a75a-132">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3a75a-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3a75a-133">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3a75a-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3a75a-134">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="3a75a-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="3a75a-135">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="3a75a-135">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="3a75a-136">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS ( \_ clase)**</span><span class="sxs-lookup"><span data-stu-id="3a75a-136">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[<span data-ttu-id="3a75a-137">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**</span><span class="sxs-lookup"><span data-stu-id="3a75a-137">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="3a75a-138">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="3a75a-138">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a75a-139">Colas de trabajo</span><span class="sxs-lookup"><span data-stu-id="3a75a-139">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 




