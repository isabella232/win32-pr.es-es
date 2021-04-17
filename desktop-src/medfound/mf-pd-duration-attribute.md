---
description: Especifica la duración de una presentación, en unidades de 100-nanosegundos.
ms.assetid: abc21696-ea97-41ff-9341-6d9e9dcb19ec
title: MF_PD_DURATION atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace7bd4f897de0220c2c449ce4fa891ac52eb200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716418"
---
# <a name="mf_pd_duration-attribute"></a><span data-ttu-id="46f86-103">\_Atributo de \_ duración MF PD</span><span class="sxs-lookup"><span data-stu-id="46f86-103">MF\_PD\_DURATION attribute</span></span>

<span data-ttu-id="46f86-104">Especifica la duración de una presentación, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="46f86-104">Specifies the duration of a presentation, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="46f86-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="46f86-105">Data type</span></span>

<span data-ttu-id="46f86-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="46f86-106">**UINT64**</span></span>

<span data-ttu-id="46f86-107">Trata como un valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="46f86-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46f86-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46f86-108">Remarks</span></span>

<span data-ttu-id="46f86-109">Los orígenes multimedia pueden establecer este atributo en un descriptor de presentación para indicar la duración de la presentación.</span><span class="sxs-lookup"><span data-stu-id="46f86-109">Media sources can set this attribute on a presentation descriptor to indicate the duration of the presentation.</span></span>

<span data-ttu-id="46f86-110">Este atributo es un valor con signo, aunque se almacena como **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="46f86-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="46f86-111">Sin embargo, el atributo nunca debe contener un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="46f86-111">However, the attribute should never contain a negative value.</span></span>

<span data-ttu-id="46f86-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="46f86-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="46f86-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="46f86-113">Examples</span></span>

<span data-ttu-id="46f86-114">En el ejemplo siguiente se muestra cómo obtener la duración de la presentación desde un origen de multimedia.</span><span class="sxs-lookup"><span data-stu-id="46f86-114">The following example shows how to get the presentation duration from a media source.</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="46f86-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46f86-115">Requirements</span></span>



| <span data-ttu-id="46f86-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="46f86-116">Requirement</span></span> | <span data-ttu-id="46f86-117">Value</span><span class="sxs-lookup"><span data-stu-id="46f86-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46f86-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46f86-118">Minimum supported client</span></span><br/> | <span data-ttu-id="46f86-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="46f86-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="46f86-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46f86-120">Minimum supported server</span></span><br/> | <span data-ttu-id="46f86-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="46f86-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="46f86-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46f86-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="46f86-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46f86-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46f86-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="46f86-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f86-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="46f86-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="46f86-126">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="46f86-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="46f86-127">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="46f86-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="46f86-128">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="46f86-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="46f86-129">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="46f86-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="46f86-130">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="46f86-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




