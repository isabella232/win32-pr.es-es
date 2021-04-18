---
description: Especifica si la canalización aplica el marcado en este nodo.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: MF_TOPONODE_MARKIN_HERE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa355cc070a7371ff2e294b3ca3ad558a4749b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715384"
---
# <a name="mf_toponode_markin_here-attribute"></a><span data-ttu-id="abb3e-103">MF \_ TOPONODE el \_ atributo avelinome \_ aquí</span><span class="sxs-lookup"><span data-stu-id="abb3e-103">MF\_TOPONODE\_MARKIN\_HERE attribute</span></span>

<span data-ttu-id="abb3e-104">Especifica si la canalización aplica el marcado en este nodo.</span><span class="sxs-lookup"><span data-stu-id="abb3e-104">Specifies whether the pipeline applies mark-in at this node.</span></span> <span data-ttu-id="abb3e-105">Marca de tiempo es el punto en el que se inicia una presentación.</span><span class="sxs-lookup"><span data-stu-id="abb3e-105">Mark-in is the point where a presentation starts.</span></span> <span data-ttu-id="abb3e-106">Si los componentes de canalización generan datos antes del punto de la marca de tiempo, los datos no se representan.</span><span class="sxs-lookup"><span data-stu-id="abb3e-106">If pipeline components generate data before the mark-in point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="abb3e-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="abb3e-107">Data type</span></span>

<span data-ttu-id="abb3e-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="abb3e-108">**UINT32**</span></span>

<span data-ttu-id="abb3e-109">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="abb3e-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="abb3e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="abb3e-110">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="abb3e-111">La mayoría de las aplicaciones no necesitan usar este atributo.</span><span class="sxs-lookup"><span data-stu-id="abb3e-111">Most applications do not need to use this attribute.</span></span> <span data-ttu-id="abb3e-112">La [sesión multimedia](media-session.md) establece automáticamente este atributo si es necesario.</span><span class="sxs-lookup"><span data-stu-id="abb3e-112">The [Media Session](media-session.md) automatically sets this attribute if needed.</span></span>

 

<span data-ttu-id="abb3e-113">Este atributo se aplica a todos los tipos de nodo.</span><span class="sxs-lookup"><span data-stu-id="abb3e-113">This attribute applies to all node types.</span></span> <span data-ttu-id="abb3e-114">Si el atributo es **true**, la canalización Media Foundation recorta los ejemplos de salida de este nodo para que coincidan con la hora de inicio de la presentación.</span><span class="sxs-lookup"><span data-stu-id="abb3e-114">If the attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the start time for the presentation.</span></span> <span data-ttu-id="abb3e-115">El cargador de topología establece este atributo cuando resuelve una topología.</span><span class="sxs-lookup"><span data-stu-id="abb3e-115">The topology loader sets this attribute when it resolves a topology.</span></span>

<span data-ttu-id="abb3e-116">Se recomienda que un nodo de cada rama de la topología tenga este atributo establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="abb3e-116">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="abb3e-117">Una rama de topología se define como la ruta de acceso desde un nodo de origen a un nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="abb3e-117">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="abb3e-118">Dentro de una bifurcación [, \_ \_ \_ ](mf-toponode-markout-here-attribute.md) \_ \_ \_ se deben establecer en el mismo nodo de la bifurcación los atributos MF TOPONODE MARKOUT aquí y MF TOPONODE Marka aquí.</span><span class="sxs-lookup"><span data-stu-id="abb3e-118">Within a branch, the [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) and MF\_TOPONODE\_MARKIN\_HERE attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="abb3e-119">No se pueden establecer en nodos diferentes dentro de la misma rama.</span><span class="sxs-lookup"><span data-stu-id="abb3e-119">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="abb3e-120">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="abb3e-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="abb3e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abb3e-121">Requirements</span></span>



| <span data-ttu-id="abb3e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="abb3e-122">Requirement</span></span> | <span data-ttu-id="abb3e-123">Value</span><span class="sxs-lookup"><span data-stu-id="abb3e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="abb3e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abb3e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="abb3e-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="abb3e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="abb3e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abb3e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="abb3e-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="abb3e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="abb3e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abb3e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="abb3e-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="abb3e-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abb3e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="abb3e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb3e-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="abb3e-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="abb3e-132">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="abb3e-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="abb3e-133">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="abb3e-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="abb3e-134">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="abb3e-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="abb3e-135">**MF \_ TOPONODE \_ MARKOUT \_ aquí**</span><span class="sxs-lookup"><span data-stu-id="abb3e-135">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="abb3e-136">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="abb3e-136">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




