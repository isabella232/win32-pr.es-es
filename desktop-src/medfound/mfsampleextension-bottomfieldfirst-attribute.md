---
description: Especifica el ámbito del campo de un fotograma de vídeo entrelazado.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: MFSampleExtension_BottomFieldFirst atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608160c92fa53e8cde6adee1831d6c3e8789bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360572"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a><span data-ttu-id="26af7-103">\_Atributo BottomFieldFirst de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="26af7-103">MFSampleExtension\_BottomFieldFirst attribute</span></span>

<span data-ttu-id="26af7-104">Especifica el ámbito del campo de un fotograma de vídeo entrelazado.</span><span class="sxs-lookup"><span data-stu-id="26af7-104">Specifies the field dominance for an interlaced video frame.</span></span> <span data-ttu-id="26af7-105">Este atributo se aplica a los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="26af7-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="26af7-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="26af7-106">Data type</span></span>

<span data-ttu-id="26af7-107">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="26af7-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="26af7-108">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="26af7-108">Get/set</span></span>

<span data-ttu-id="26af7-109">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="26af7-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="26af7-110">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="26af7-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="26af7-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="26af7-111">Applies to</span></span>

[<span data-ttu-id="26af7-112">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="26af7-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="26af7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26af7-113">Remarks</span></span>

<span data-ttu-id="26af7-114">Si el fotograma de vídeo está entrelazado y el ejemplo contiene dos campos intercalados, este atributo indica el campo que se muestra en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="26af7-114">If the video frame is interlaced and the sample contains two interleaved fields, this attribute indicates which field is displayed first.</span></span> <span data-ttu-id="26af7-115">Si es **true**, el campo inferior es el primero en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="26af7-115">If **TRUE**, the bottom field is first in time.</span></span> <span data-ttu-id="26af7-116">Si es **false**, el campo superior es primero.</span><span class="sxs-lookup"><span data-stu-id="26af7-116">If **FALSE**, the top field is first.</span></span>

<span data-ttu-id="26af7-117">Si el marco está entrelazado y el ejemplo contiene un campo único, este atributo indica el campo que contiene el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="26af7-117">If the frame is interlaced and the sample contains a single field, this attribute indicates which field the sample contains.</span></span> <span data-ttu-id="26af7-118">Si **es true**, el ejemplo contiene el campo inferior.</span><span class="sxs-lookup"><span data-stu-id="26af7-118">If **TRUE**, the sample contains the bottom field.</span></span> <span data-ttu-id="26af7-119">Si **es false**, el ejemplo contiene el campo superior.</span><span class="sxs-lookup"><span data-stu-id="26af7-119">If **FALSE**, the sample contains the top field.</span></span>

<span data-ttu-id="26af7-120">Si el marco es progresivo, este atributo describe cómo se deben ordenar los campos cuando la salida está entrelazada.</span><span class="sxs-lookup"><span data-stu-id="26af7-120">If the frame is progressive, this attribute describes how the fields should be ordered when the output is interlaced.</span></span> <span data-ttu-id="26af7-121">Si **es true**, el campo inferior debe generarse primero.</span><span class="sxs-lookup"><span data-stu-id="26af7-121">If **TRUE**, the bottom field should be output first.</span></span> <span data-ttu-id="26af7-122">Si **es false**, el campo superior se debe mostrar primero.</span><span class="sxs-lookup"><span data-stu-id="26af7-122">If **FALSE**, the top field should be output first.</span></span>

<span data-ttu-id="26af7-123">Si no se establece este atributo, el tipo de medio describe el ámbito de los campos.</span><span class="sxs-lookup"><span data-stu-id="26af7-123">If this attribute not set, the media type describes the field dominance.</span></span>

<span data-ttu-id="26af7-124">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="26af7-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="26af7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26af7-125">Requirements</span></span>



| <span data-ttu-id="26af7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="26af7-126">Requirement</span></span> | <span data-ttu-id="26af7-127">Value</span><span class="sxs-lookup"><span data-stu-id="26af7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26af7-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26af7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="26af7-129">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="26af7-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="26af7-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26af7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="26af7-131">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="26af7-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="26af7-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26af7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="26af7-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="26af7-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26af7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="26af7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26af7-135">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26af7-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="26af7-136">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="26af7-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="26af7-137">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="26af7-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="26af7-138">Entrelazado de vídeo</span><span class="sxs-lookup"><span data-stu-id="26af7-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




