---
description: Especifica si las secuencias de audio de una presentación tienen una velocidad de bits variable.
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: MF_PD_AUDIO_ISVARIABLEBITRATE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a34d3dd64f9100050dc9aae37e811d00c9d58af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277685"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a><span data-ttu-id="a3497-103">\_ \_ Atributo ISVARIABLEBITRATE de audio MF PD \_</span><span class="sxs-lookup"><span data-stu-id="a3497-103">MF\_PD\_AUDIO\_ISVARIABLEBITRATE attribute</span></span>

<span data-ttu-id="a3497-104">Especifica si las secuencias de audio de una presentación tienen una velocidad de bits variable.</span><span class="sxs-lookup"><span data-stu-id="a3497-104">Specifies whether the audio streams in a presentation have a variable bit rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="a3497-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a3497-105">Data type</span></span>

<span data-ttu-id="a3497-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a3497-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a3497-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="a3497-107">Get/set</span></span>

<span data-ttu-id="a3497-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a3497-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a3497-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a3497-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a3497-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="a3497-110">Applies To</span></span>

[<span data-ttu-id="a3497-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a3497-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="a3497-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3497-112">Remarks</span></span>

<span data-ttu-id="a3497-113">Este es un atributo opcional para los descriptores de presentación.</span><span class="sxs-lookup"><span data-stu-id="a3497-113">This is an optional attribute for presentation descriptors.</span></span> <span data-ttu-id="a3497-114">Si el atributo es **true** (distinto de cero), la presentación contiene al menos una secuencia de audio de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="a3497-114">If the attribute is **TRUE** (nonzero), the presentation contains at least one variable-bit-rate (VBR) audio stream.</span></span> <span data-ttu-id="a3497-115">Si el atributo es **false**, todas las secuencias de audio tienen una velocidad de bits constante.</span><span class="sxs-lookup"><span data-stu-id="a3497-115">If the attribute is **FALSE**, all of the audio streams have a constant bit rate.</span></span>

<span data-ttu-id="a3497-116">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a3497-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3497-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3497-117">Requirements</span></span>



| <span data-ttu-id="a3497-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3497-118">Requirement</span></span> | <span data-ttu-id="a3497-119">Value</span><span class="sxs-lookup"><span data-stu-id="a3497-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3497-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3497-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a3497-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="a3497-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a3497-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3497-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a3497-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="a3497-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a3497-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3497-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3497-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3497-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3497-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3497-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3497-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a3497-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a3497-128">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="a3497-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




