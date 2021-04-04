---
description: Especifica el formato de salida preferido para un codificador.
ms.assetid: 36a09696-3fe7-41a0-93f1-712220f88b04
title: MFT_PREFERRED_OUTPUTTYPE_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13cd079bee65f5324987d9b38dca845ec5b85f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908644"
---
# <a name="mft_preferred_outputtype_attribute-attribute"></a><span data-ttu-id="e87da-103">\_Atributo de \_ atributo OUTPUTTYPE preferido \_ de MFT</span><span class="sxs-lookup"><span data-stu-id="e87da-103">MFT\_PREFERRED\_OUTPUTTYPE\_Attribute attribute</span></span>

<span data-ttu-id="e87da-104">Especifica el formato de salida preferido para un codificador.</span><span class="sxs-lookup"><span data-stu-id="e87da-104">Specifies the preferred output format for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="e87da-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e87da-105">Data type</span></span>

<span data-ttu-id="e87da-106">**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) IMFAttributes \** _ almacenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="e87da-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="e87da-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="e87da-107">Get/set</span></span>

<span data-ttu-id="e87da-108">Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="e87da-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="e87da-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="e87da-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e87da-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="e87da-110">Applies to</span></span>

[<span data-ttu-id="e87da-111">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="e87da-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="e87da-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e87da-112">Remarks</span></span>

<span data-ttu-id="e87da-113">Este atributo se puede establecer en el objeto de activación devuelto por la función [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) .</span><span class="sxs-lookup"><span data-stu-id="e87da-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="e87da-114">El atributo solo se aplica cuando el objeto de activación está configurado para crear un codificador.</span><span class="sxs-lookup"><span data-stu-id="e87da-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="e87da-115">El valor del atributo es un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="e87da-115">The value of the attribute is a media type.</span></span> <span data-ttu-id="e87da-116">El objeto de activación establece este tipo de salida en el codificador.</span><span class="sxs-lookup"><span data-stu-id="e87da-116">The activation object sets this output type on the encoder.</span></span>

<span data-ttu-id="e87da-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e87da-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e87da-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e87da-118">Requirements</span></span>



| <span data-ttu-id="e87da-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e87da-119">Requirement</span></span> | <span data-ttu-id="e87da-120">Value</span><span class="sxs-lookup"><span data-stu-id="e87da-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e87da-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e87da-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e87da-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="e87da-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e87da-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e87da-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e87da-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="e87da-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e87da-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e87da-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e87da-126"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="e87da-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e87da-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e87da-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e87da-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e87da-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e87da-129">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="e87da-129">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="e87da-130">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="e87da-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




