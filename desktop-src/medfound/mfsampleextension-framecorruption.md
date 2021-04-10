---
description: Especifica si un fotograma de vídeo está dañado.
ms.assetid: 0218F6F6-6832-445C-B733-6A99E4EA2A3B
title: MFSampleExtension_FrameCorruption atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d3618e5d847833b539cdfa7f6f99ae784e96c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155964"
---
# <a name="mfsampleextension_framecorruption-attribute"></a><span data-ttu-id="53544-103">\_Atributo FrameCorruption de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="53544-103">MFSampleExtension\_FrameCorruption attribute</span></span>

<span data-ttu-id="53544-104">Especifica si un fotograma de vídeo está dañado.</span><span class="sxs-lookup"><span data-stu-id="53544-104">Specifies whether a video frame is corrupted.</span></span>

## <a name="data-type"></a><span data-ttu-id="53544-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="53544-105">Data type</span></span>

<span data-ttu-id="53544-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="53544-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="53544-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="53544-107">Get/set</span></span>

<span data-ttu-id="53544-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="53544-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="53544-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="53544-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="53544-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="53544-110">Applies to</span></span>

[<span data-ttu-id="53544-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="53544-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="53544-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53544-112">Remarks</span></span>

<span data-ttu-id="53544-113">Un descodificador de vídeo puede establecer este atributo en sus ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="53544-113">A video decoder can set this attribute on its output samples.</span></span> <span data-ttu-id="53544-114">Si el valor es 1, el descodificador detectó daños en los datos del marco.</span><span class="sxs-lookup"><span data-stu-id="53544-114">If the value is 1, the decoder detected data corruption in the frame.</span></span> <span data-ttu-id="53544-115">Si el valor es 0, no hay datos dañados o no se detectó ninguno.</span><span class="sxs-lookup"><span data-stu-id="53544-115">If the value is 0, there is no data corruption, or none was detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="53544-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53544-116">Requirements</span></span>



| <span data-ttu-id="53544-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="53544-117">Requirement</span></span> | <span data-ttu-id="53544-118">Value</span><span class="sxs-lookup"><span data-stu-id="53544-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53544-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53544-119">Minimum supported client</span></span><br/> | <span data-ttu-id="53544-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="53544-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="53544-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53544-121">Minimum supported server</span></span><br/> | <span data-ttu-id="53544-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="53544-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="53544-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53544-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="53544-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="53544-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53544-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="53544-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53544-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="53544-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="53544-127">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="53544-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="53544-128">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="53544-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




