---
description: Especifica la hora de inicio de la presentación.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: MF_TOPONODE_MEDIASTART atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab00727cc328bfd6ba780050160fb21eecbb96f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717371"
---
# <a name="mf_toponode_mediastart-attribute"></a><span data-ttu-id="5e078-103">\_ \_ Atributo MEDIASTART de MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="5e078-103">MF\_TOPONODE\_MEDIASTART attribute</span></span>

<span data-ttu-id="5e078-104">Especifica la hora de inicio de la presentación.</span><span class="sxs-lookup"><span data-stu-id="5e078-104">Specifies the start time of the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="5e078-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5e078-105">Data type</span></span>

<span data-ttu-id="5e078-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="5e078-106">**UINT64**</span></span>

<span data-ttu-id="5e078-107">Trata como un valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="5e078-107">Treat as a **LONGLONG** value.</span></span>

## <a name="getset"></a><span data-ttu-id="5e078-108">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="5e078-108">Get/set</span></span>

<span data-ttu-id="5e078-109">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="5e078-109">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="5e078-110">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="5e078-110">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5e078-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="5e078-111">Applies to</span></span>

[<span data-ttu-id="5e078-112">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="5e078-112">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a><span data-ttu-id="5e078-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e078-113">Remarks</span></span>

<span data-ttu-id="5e078-114">Este atributo especifica la posición en el origen donde se inicia la reproducción, en unidades de 100-nanosegundos, con respecto al inicio del origen.</span><span class="sxs-lookup"><span data-stu-id="5e078-114">This attribute specifies the position in the source where playback starts, in 100-nanosecond units, relative to the start the source.</span></span> <span data-ttu-id="5e078-115">Si no se establece el atributo, la reproducción comienza en cero (el inicio del archivo).</span><span class="sxs-lookup"><span data-stu-id="5e078-115">If the attribute is not set, playback starts at zero (the start of the file).</span></span> <span data-ttu-id="5e078-116">Por ejemplo, para iniciar la reproducción en la marca de 5 segundos, establezca este atributo en 50 millones.</span><span class="sxs-lookup"><span data-stu-id="5e078-116">For example, to start playback at the 5-second mark, set this attribute to 50000000.</span></span> <span data-ttu-id="5e078-117">Establezca el atributo en los nodos de origen de la topología (nodos con el tipo igual a la **\_ topología MF \_ SOURCESTREAM \_ nodo**).</span><span class="sxs-lookup"><span data-stu-id="5e078-117">Set the attribute on the source nodes in the topology (nodes with type equal to **MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="5e078-118">Establezca el atributo antes de llamar a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="5e078-118">Set the attribute before calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

> [!Note]  
> <span data-ttu-id="5e078-119">Si inserta manualmente un descodificador en la topología, también debe establecer los atributos [MF \_ TOPONODE \_ avelinot \_ aquí](mf-toponode-markin-here-attribute.md) y [MF \_ TOPONODE \_ MARKOUT \_ aquí](mf-toponode-markout-here-attribute.md) en el nodo descodificador.</span><span class="sxs-lookup"><span data-stu-id="5e078-119">If you manually insert a decoder into the topology, you must also set the [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) and [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) attributes on the decoder node.</span></span>

 

<span data-ttu-id="5e078-120">Este atributo es un valor con signo, aunque se almacena como **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="5e078-120">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="5e078-121">Sin embargo, los valores negativos no son significativos.</span><span class="sxs-lookup"><span data-stu-id="5e078-121">However, negative values are not meaningful.</span></span>

<span data-ttu-id="5e078-122">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5e078-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e078-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e078-123">Requirements</span></span>



| <span data-ttu-id="5e078-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e078-124">Requirement</span></span> | <span data-ttu-id="5e078-125">Value</span><span class="sxs-lookup"><span data-stu-id="5e078-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e078-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e078-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5e078-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e078-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e078-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e078-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5e078-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e078-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5e078-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e078-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e078-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e078-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e078-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e078-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e078-133">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e078-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e078-134">Tiempos de presentación de secuencia</span><span class="sxs-lookup"><span data-stu-id="5e078-134">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="5e078-135">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="5e078-135">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e078-136">**MF \_ TOPONODE \_ MEDIASTOP**</span><span class="sxs-lookup"><span data-stu-id="5e078-136">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




