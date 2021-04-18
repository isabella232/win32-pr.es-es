---
description: Especifica el elemento que contiene este nodo de origen.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: MF_TOPONODE_SEQUENCE_ELEMENTID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715379"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a><span data-ttu-id="9c7db-103">\_ \_ Atributo ELEMENTID de secuencia MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="9c7db-103">MF\_TOPONODE\_SEQUENCE\_ELEMENTID attribute</span></span>

<span data-ttu-id="9c7db-104">Especifica el elemento que contiene este nodo de origen.</span><span class="sxs-lookup"><span data-stu-id="9c7db-104">Specifies the element that contains this source node.</span></span>

## <a name="data-type"></a><span data-ttu-id="9c7db-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9c7db-105">Data type</span></span>

<span data-ttu-id="9c7db-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9c7db-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9c7db-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c7db-107">Remarks</span></span>

<span data-ttu-id="9c7db-108">Este atributo se aplica a los nodos de origen (**\_ \_ \_ nodo SOURCESTREAM de topología MF**).</span><span class="sxs-lookup"><span data-stu-id="9c7db-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span>

<span data-ttu-id="9c7db-109">La canalización multimedia usa este atributo para detectar cuándo los orígenes multimedia forman parte del mismo elemento.</span><span class="sxs-lookup"><span data-stu-id="9c7db-109">The media pipeline uses this attribute to discover when media sources are part of the same element.</span></span> <span data-ttu-id="9c7db-110">La canalización trata todos los nodos de origen que forman parte del mismo elemento que tienen el mismo reloj.</span><span class="sxs-lookup"><span data-stu-id="9c7db-110">The pipeline treats all source nodes that are part of the same element as having the same clock.</span></span>

<span data-ttu-id="9c7db-111">Cuando la canalización pone en cola una nueva topología que contiene nodos de origen que forman parte de un elemento que se encuentra en la topología anterior, la canalización trata estos nodos de origen como si tuvieran el mismo reloj que los nodos de origen de ese elemento en la topología anterior.</span><span class="sxs-lookup"><span data-stu-id="9c7db-111">When the pipeline queues up a new topology that contains source nodes that are part of an element that is present in the previous topology, the pipeline treats these source nodes as having the same clock as the source nodes from that element in the previous topology.</span></span>

> [!Note]  
> <span data-ttu-id="9c7db-112">La canalización multimedia no corrige las marcas de tiempo de los nodos de origen con diferentes velocidades de reloj.</span><span class="sxs-lookup"><span data-stu-id="9c7db-112">The media pipeline does not correct time stamps for source nodes with different clock rates.</span></span>

 

<span data-ttu-id="9c7db-113">Un origen multimedia que puede proporcionar topologías debe implementar la interfaz [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) o la interfaz [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) .</span><span class="sxs-lookup"><span data-stu-id="9c7db-113">A media source that can provide topologies should implement the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface or the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface.</span></span> <span data-ttu-id="9c7db-114">Un origen multimedia que proporciona topologías debe establecer el atributo de la **\_ \_ secuencia \_ TOPONODE de MF** en cada nodo de origen que cree.</span><span class="sxs-lookup"><span data-stu-id="9c7db-114">A media source that provides topologies should set the **MF\_TOPONODE\_SEQUENCE\_ELEMENTID** attribute on every source node that it creates.</span></span>

<span data-ttu-id="9c7db-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9c7db-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c7db-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c7db-116">Requirements</span></span>



| <span data-ttu-id="9c7db-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c7db-117">Requirement</span></span> | <span data-ttu-id="9c7db-118">Value</span><span class="sxs-lookup"><span data-stu-id="9c7db-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c7db-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c7db-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9c7db-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9c7db-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9c7db-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c7db-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9c7db-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c7db-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c7db-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c7db-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c7db-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c7db-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c7db-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c7db-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c7db-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9c7db-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9c7db-127">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9c7db-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9c7db-128">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9c7db-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="9c7db-129">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="9c7db-129">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[<span data-ttu-id="9c7db-130">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="9c7db-130">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[<span data-ttu-id="9c7db-131">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="9c7db-131">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="9c7db-132">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="9c7db-132">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="9c7db-133">Origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="9c7db-133">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




