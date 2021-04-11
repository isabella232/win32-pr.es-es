---
description: Especifica la prioridad del elemento de trabajo para una bifurcación de la topología.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5f7df6630e41a32eeb069c2a07b8030da79929
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275688"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a><span data-ttu-id="511b4-103">MF \_ TOPONODE \_ WORKQUEUE \_ atributo de prioridad de elemento \_</span><span class="sxs-lookup"><span data-stu-id="511b4-103">MF\_TOPONODE\_WORKQUEUE\_ITEM\_PRIORITY attribute</span></span>

<span data-ttu-id="511b4-104">Especifica la prioridad del elemento de trabajo para una bifurcación de la topología.</span><span class="sxs-lookup"><span data-stu-id="511b4-104">Specifies the work-item priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="511b4-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="511b4-105">Data type</span></span>

<span data-ttu-id="511b4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="511b4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="511b4-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="511b4-107">Remarks</span></span>

<span data-ttu-id="511b4-108">Este atributo se aplica a los nodos de origen (**\_ \_ \_ nodo SOURCESTREAM de topología MF**).</span><span class="sxs-lookup"><span data-stu-id="511b4-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="511b4-109">El atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="511b4-109">The attribute is optional.</span></span>

<span data-ttu-id="511b4-110">Este atributo requiere el atributo [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) en el mismo nodo.</span><span class="sxs-lookup"><span data-stu-id="511b4-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute on the same node.</span></span>

<span data-ttu-id="511b4-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="511b4-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="511b4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="511b4-112">Requirements</span></span>



| <span data-ttu-id="511b4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="511b4-113">Requirement</span></span> | <span data-ttu-id="511b4-114">Value</span><span class="sxs-lookup"><span data-stu-id="511b4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="511b4-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="511b4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="511b4-116">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="511b4-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="511b4-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="511b4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="511b4-118">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="511b4-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="511b4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="511b4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="511b4-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="511b4-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="511b4-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="511b4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="511b4-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="511b4-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="511b4-123">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="511b4-123">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="511b4-124">Mejoras en la cola de trabajo y subprocesos</span><span class="sxs-lookup"><span data-stu-id="511b4-124">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="511b4-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="511b4-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="511b4-126">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="511b4-126">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="511b4-127">**identificador de WORKQUEUE de MF \_ TOPONODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="511b4-127">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> </dl>

 

 




