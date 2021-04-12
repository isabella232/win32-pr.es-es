---
description: Velocidad de fotogramas de un tipo de medio de vídeo, en fotogramas por segundo.
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: MF_MT_FRAME_RATE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8df2ef4268bd643d9f65eb16c3f7257bcaceb1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423991"
---
# <a name="mf_mt_frame_rate-attribute"></a><span data-ttu-id="e063e-103">MF \_ MT ( \_ atributo de velocidad de fotogramas) \_</span><span class="sxs-lookup"><span data-stu-id="e063e-103">MF\_MT\_FRAME\_RATE attribute</span></span>

<span data-ttu-id="e063e-104">Velocidad de fotogramas de un tipo de medio de vídeo, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="e063e-104">Frame rate of a video media type, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="e063e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e063e-105">Data type</span></span>

<span data-ttu-id="e063e-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="e063e-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="e063e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e063e-107">Remarks</span></span>

<span data-ttu-id="e063e-108">La velocidad de fotogramas se expresa como una proporción.</span><span class="sxs-lookup"><span data-stu-id="e063e-108">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="e063e-109">Los 32 superiores del valor del atributo contienen el numerador y los 32 bits inferiores contienen el denominador.</span><span class="sxs-lookup"><span data-stu-id="e063e-109">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="e063e-110">Por ejemplo, si la velocidad de fotogramas es de 30 fotogramas por segundo (FPS), la relación es 30/1.</span><span class="sxs-lookup"><span data-stu-id="e063e-110">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="e063e-111">Si la velocidad de fotogramas es 29,97 fps, la relación es 30000/1001.</span><span class="sxs-lookup"><span data-stu-id="e063e-111">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

<span data-ttu-id="e063e-112">Para establecer el valor, use la función [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="e063e-112">To set the value, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="e063e-113">Para obtener el valor, use la función [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="e063e-113">To get the value, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="e063e-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e063e-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="e063e-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e063e-115">Examples</span></span>

<span data-ttu-id="e063e-116">En el ejemplo siguiente se establece la velocidad de fotogramas en un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e063e-116">The following example sets the frame rate on a video media type.</span></span>


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



<span data-ttu-id="e063e-117">En el ejemplo siguiente se obtiene la velocidad de fotogramas de un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e063e-117">The following example gets the frame rate from a video media type.</span></span>


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a><span data-ttu-id="e063e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e063e-118">Requirements</span></span>



| <span data-ttu-id="e063e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e063e-119">Requirement</span></span> | <span data-ttu-id="e063e-120">Value</span><span class="sxs-lookup"><span data-stu-id="e063e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e063e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e063e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e063e-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="e063e-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e063e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e063e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e063e-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="e063e-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e063e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e063e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e063e-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e063e-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e063e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e063e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e063e-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e063e-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e063e-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e063e-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="e063e-130">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="e063e-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="e063e-131">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="e063e-131">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[<span data-ttu-id="e063e-132">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="e063e-132">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




