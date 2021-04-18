---
description: Especifica una tarea del servicio de programador de clases multimedia (MMCSS) para una bifurcación de topología.
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: MF_TOPONODE_WORKQUEUE_MMCSS_CLASS atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 824c9dbdc9b12bbc8fead9ab6ae722fca1e6643a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720414"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a><span data-ttu-id="d82df-103">\_Atributo de clase MF TOPONODE \_ WORKQUEUE \_ MMCSS \_</span><span class="sxs-lookup"><span data-stu-id="d82df-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="d82df-104">Especifica una tarea del [servicio de programador de clases multimedia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) para una bifurcación de topología.</span><span class="sxs-lookup"><span data-stu-id="d82df-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) task for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="d82df-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d82df-105">Data type</span></span>

<span data-ttu-id="d82df-106">Cadena de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="d82df-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="d82df-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d82df-107">Remarks</span></span>

<span data-ttu-id="d82df-108">Este atributo se aplica a los nodos de origen (**\_ \_ \_ nodo SOURCESTREAM de topología MF**).</span><span class="sxs-lookup"><span data-stu-id="d82df-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="d82df-109">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="d82df-109">This attribute is optional.</span></span>

<span data-ttu-id="d82df-110">Este atributo requiere el atributo [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="d82df-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute.</span></span> <span data-ttu-id="d82df-111">Si establece este atributo, establezca también el atributo **MF \_ TOPONODE \_ WORKQUEUE \_ ID** en el mismo nodo.</span><span class="sxs-lookup"><span data-stu-id="d82df-111">If you set this attribute, also set the **MF\_TOPONODE\_WORKQUEUE\_ID** attribute is set on the same node.</span></span>

<span data-ttu-id="d82df-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d82df-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d82df-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d82df-113">Requirements</span></span>



| <span data-ttu-id="d82df-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d82df-114">Requirement</span></span> | <span data-ttu-id="d82df-115">Value</span><span class="sxs-lookup"><span data-stu-id="d82df-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d82df-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d82df-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d82df-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d82df-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d82df-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d82df-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d82df-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d82df-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d82df-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d82df-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d82df-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d82df-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d82df-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d82df-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d82df-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d82df-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d82df-124">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="d82df-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="d82df-125">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="d82df-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="d82df-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="d82df-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="d82df-127">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="d82df-127">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="d82df-128">**identificador de WORKQUEUE de MF \_ TOPONODE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d82df-128">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="d82df-129">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**</span><span class="sxs-lookup"><span data-stu-id="d82df-129">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="d82df-130">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="d82df-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="d82df-131">Colas de trabajo</span><span class="sxs-lookup"><span data-stu-id="d82df-131">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
