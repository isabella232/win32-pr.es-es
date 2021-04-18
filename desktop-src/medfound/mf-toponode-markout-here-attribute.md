---
description: Especifica si la canalización aplica el marcado en este nodo. El marcado es el punto en el que finaliza una presentación. Si los componentes de canalización generan datos más allá del punto de la marca de salida, los datos no se representan.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: MF_TOPONODE_MARKOUT_HERE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5dc21f39f45aa04860f3374bead54d260f0821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715381"
---
# <a name="mf_toponode_markout_here-attribute"></a><span data-ttu-id="55dd5-105">MF \_ TOPONODE \_ MARKOUT \_ aquí atributo</span><span class="sxs-lookup"><span data-stu-id="55dd5-105">MF\_TOPONODE\_MARKOUT\_HERE attribute</span></span>

<span data-ttu-id="55dd5-106">Especifica si la canalización aplica el marcado en este nodo.</span><span class="sxs-lookup"><span data-stu-id="55dd5-106">Specifies whether the pipeline applies mark-out at this node.</span></span> <span data-ttu-id="55dd5-107">El marcado es el punto en el que finaliza una presentación.</span><span class="sxs-lookup"><span data-stu-id="55dd5-107">Mark-out is the point where a presentation ends.</span></span> <span data-ttu-id="55dd5-108">Si los componentes de canalización generan datos más allá del punto de la marca de salida, los datos no se representan.</span><span class="sxs-lookup"><span data-stu-id="55dd5-108">If pipeline components generate data past the mark-out point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="55dd5-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="55dd5-109">Data type</span></span>

<span data-ttu-id="55dd5-110">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="55dd5-110">**UINT32**</span></span>

<span data-ttu-id="55dd5-111">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="55dd5-111">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55dd5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55dd5-112">Remarks</span></span>

<span data-ttu-id="55dd5-113">Este atributo se aplica a todos los tipos de nodo.</span><span class="sxs-lookup"><span data-stu-id="55dd5-113">This attribute applies to all node types.</span></span>

<span data-ttu-id="55dd5-114">Si este atributo es **true**, la canalización Media Foundation recorta los ejemplos de salida de este nodo para que coincidan con la hora de detención de la presentación.</span><span class="sxs-lookup"><span data-stu-id="55dd5-114">If this attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the stop time for the presentation.</span></span> <span data-ttu-id="55dd5-115">El cargador de topología establece este atributo cuando resuelve una topología.</span><span class="sxs-lookup"><span data-stu-id="55dd5-115">The topology loader sets this attribute when it resolves a topology.</span></span> <span data-ttu-id="55dd5-116">La mayoría de las aplicaciones no necesitan establecer ni recuperar este atributo.</span><span class="sxs-lookup"><span data-stu-id="55dd5-116">Most applications do not need to set or retrieve this attribute.</span></span>

<span data-ttu-id="55dd5-117">Se recomienda que un nodo de cada rama de la topología tenga este atributo establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="55dd5-117">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="55dd5-118">Una rama de topología se define como la ruta de acceso desde un nodo de origen a un nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="55dd5-118">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="55dd5-119">Dentro de una bifurcación, \_ \_ \_ se deben establecer en el mismo nodo de la bifurcación los atributos MF TOPONODE MARKOUT aquí y [MF \_ TOPONODE \_ Marka \_ aquí](mf-toponode-markin-here-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="55dd5-119">Within a branch, the MF\_TOPONODE\_MARKOUT\_HERE and [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="55dd5-120">No se pueden establecer en nodos diferentes dentro de la misma rama.</span><span class="sxs-lookup"><span data-stu-id="55dd5-120">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="55dd5-121">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="55dd5-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="55dd5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55dd5-122">Requirements</span></span>



| <span data-ttu-id="55dd5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="55dd5-123">Requirement</span></span> | <span data-ttu-id="55dd5-124">Value</span><span class="sxs-lookup"><span data-stu-id="55dd5-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55dd5-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55dd5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="55dd5-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="55dd5-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="55dd5-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55dd5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="55dd5-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="55dd5-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="55dd5-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55dd5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="55dd5-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55dd5-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55dd5-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="55dd5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55dd5-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="55dd5-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="55dd5-133">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="55dd5-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="55dd5-134">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="55dd5-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="55dd5-135">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="55dd5-135">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="55dd5-136">**\_TOPONODE MF \_ \_ aquí**</span><span class="sxs-lookup"><span data-stu-id="55dd5-136">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="55dd5-137">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="55dd5-137">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




