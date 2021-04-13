---
description: Especifica si un ejemplo multimedia es el primer ejemplo después de un intervalo en la secuencia.
ms.assetid: f9e1e700-9958-404d-8b83-08f846f5a1b0
title: MFSampleExtension_Discontinuity atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e401a26c269a3b77d881bc74ae2c7b30d9d88f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543950"
---
# <a name="mfsampleextension_discontinuity-attribute"></a><span data-ttu-id="fc630-103">\_Atributo discontinuidad de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="fc630-103">MFSampleExtension\_Discontinuity attribute</span></span>

<span data-ttu-id="fc630-104">Especifica si un ejemplo multimedia es el primer ejemplo después de un intervalo en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="fc630-104">Specifies whether a media sample is the first sample after a gap in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="fc630-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fc630-105">Data type</span></span>

<span data-ttu-id="fc630-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="fc630-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="fc630-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="fc630-107">Get/set</span></span>

<span data-ttu-id="fc630-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="fc630-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="fc630-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="fc630-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="fc630-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="fc630-110">Applies to</span></span>

[<span data-ttu-id="fc630-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="fc630-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="fc630-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc630-112">Remarks</span></span>

<span data-ttu-id="fc630-113">Este atributo se aplica a los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="fc630-113">This attribute applies to media samples.</span></span> <span data-ttu-id="fc630-114">Si este atributo es **true**, significa que se ha producido una discontinuidad en el flujo y este ejemplo es el primero en aparecer después del intervalo.</span><span class="sxs-lookup"><span data-stu-id="fc630-114">If this attribute is **TRUE**, it means there was a discontinuity in the stream and this sample is the first to appear after the gap.</span></span>

<span data-ttu-id="fc630-115">Si no se establece este atributo, el valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="fc630-115">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="fc630-116">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="fc630-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc630-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc630-117">Requirements</span></span>



| <span data-ttu-id="fc630-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc630-118">Requirement</span></span> | <span data-ttu-id="fc630-119">Value</span><span class="sxs-lookup"><span data-stu-id="fc630-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc630-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc630-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fc630-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="fc630-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="fc630-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc630-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fc630-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="fc630-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="fc630-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc630-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc630-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc630-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc630-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc630-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc630-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fc630-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fc630-128">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc630-128">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="fc630-129">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="fc630-129">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




