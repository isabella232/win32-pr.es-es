---
description: Especifica la hora de inicio de una topología, relativa al inicio de la primera topología de la secuencia.
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: MF_TOPOLOGY_PROJECTSTOP atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5730791440131cd9efdbbb94ce15a598051f1e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544334"
---
# <a name="mf_topology_projectstop-attribute"></a><span data-ttu-id="85695-103">\_Atributo PROJECTSTOP de la topología MF \_</span><span class="sxs-lookup"><span data-stu-id="85695-103">MF\_TOPOLOGY\_PROJECTSTOP attribute</span></span>

<span data-ttu-id="85695-104">Especifica la hora de inicio de una topología, relativa al inicio de la primera topología de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="85695-104">Specifies the start time for a topology, relative to the start of the first topology in the sequence.</span></span>

## <a name="data-type"></a><span data-ttu-id="85695-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="85695-105">Data type</span></span>

<span data-ttu-id="85695-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="85695-106">**UINT64**</span></span>

<span data-ttu-id="85695-107">Trata como un valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="85695-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85695-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85695-108">Remarks</span></span>

<span data-ttu-id="85695-109">El valor se proporciona en unidades de 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="85695-109">The value is given in units of 100 nanoseconds.</span></span>

<span data-ttu-id="85695-110">Si la sesión multimedia se creó con el atributo de [**\_ \_ \_ hora global de la sesión MF**](mf-session-global-time-attribute.md) igual a **true**, todas las topologías deben contener el atributo PROJECTSTOP de la **\_ topología \_ MF** .</span><span class="sxs-lookup"><span data-stu-id="85695-110">If the Media Session was created with the [**MF\_SESSION\_GLOBAL\_TIME**](mf-session-global-time-attribute.md) attribute equal to **TRUE**, all topologies must contain the **MF\_TOPOLOGY\_PROJECTSTOP** attribute.</span></span> <span data-ttu-id="85695-111">De lo contrario, las topologías no deben contener el atributo **\_ \_ PROJECTSTOP de la topología MF** .</span><span class="sxs-lookup"><span data-stu-id="85695-111">Otherwise, topologies must not contain the **MF\_TOPOLOGY\_PROJECTSTOP** attribute.</span></span> <span data-ttu-id="85695-112">Para obtener más información, vea [tiempos de presentación de secuencias](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="85695-112">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="85695-113">Este atributo es un valor con signo, aunque se almacena como **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="85695-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="85695-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="85695-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="85695-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85695-115">Requirements</span></span>



| <span data-ttu-id="85695-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="85695-116">Requirement</span></span> | <span data-ttu-id="85695-117">Value</span><span class="sxs-lookup"><span data-stu-id="85695-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85695-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85695-118">Minimum supported client</span></span><br/> | <span data-ttu-id="85695-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="85695-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="85695-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85695-120">Minimum supported server</span></span><br/> | <span data-ttu-id="85695-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="85695-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="85695-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85695-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="85695-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85695-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85695-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="85695-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85695-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="85695-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="85695-126">Tiempos de presentación de secuencia</span><span class="sxs-lookup"><span data-stu-id="85695-126">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="85695-127">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="85695-127">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="85695-128">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="85695-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="85695-129">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="85695-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="85695-130">**\_PROJECTSTART de topología \_ MF**</span><span class="sxs-lookup"><span data-stu-id="85695-130">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




