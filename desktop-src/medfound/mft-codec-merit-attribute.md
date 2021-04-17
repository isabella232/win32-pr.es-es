---
description: Contiene el valor de mérito de un códec de hardware.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: MFT_CODEC_MERIT_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659834"
---
# <a name="mft_codec_merit_attribute-attribute"></a><span data-ttu-id="3f646-103">\_Atributo de \_ mérito del códec de MFT \_</span><span class="sxs-lookup"><span data-stu-id="3f646-103">MFT\_CODEC\_MERIT\_Attribute attribute</span></span>

<span data-ttu-id="3f646-104">Contiene el valor de mérito de un códec de hardware.</span><span class="sxs-lookup"><span data-stu-id="3f646-104">Contains the merit value of a hardware codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="3f646-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3f646-105">Data type</span></span>

<span data-ttu-id="3f646-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3f646-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="3f646-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="3f646-107">Get/set</span></span>

<span data-ttu-id="3f646-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="3f646-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3f646-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="3f646-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f646-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f646-110">Remarks</span></span>

<span data-ttu-id="3f646-111">Este atributo se establece en el objeto de activación de una transformación de Media Foundation (MFT) que representa un códec de hardware.</span><span class="sxs-lookup"><span data-stu-id="3f646-111">This attribute is set on the activation object for a Media Foundation transform (MFT) that represents a hardware codec.</span></span> <span data-ttu-id="3f646-112">El valor del atributo es el valor de mérito del códec.</span><span class="sxs-lookup"><span data-stu-id="3f646-112">The value of the attribute is the codec's merit value.</span></span>

<span data-ttu-id="3f646-113">Este atributo controla el orden en el que la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) enumera los códecs, si se establece la marca SORTANDFILTER de la **\_ \_ marca \_ de enumeración MFT** .</span><span class="sxs-lookup"><span data-stu-id="3f646-113">This attribute controls the order in which the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function enumerates codecs, if the **MFT\_ENUM\_FLAG\_SORTANDFILTER** flag is set.</span></span> <span data-ttu-id="3f646-114">MFTs con un valor de mérito aparecen en la lista más arriba que en otras MFTs.</span><span class="sxs-lookup"><span data-stu-id="3f646-114">MFTs with a merit value appear higher in the list than other MFTs.</span></span>

<span data-ttu-id="3f646-115">Este atributo no contiene un valor de confianza.</span><span class="sxs-lookup"><span data-stu-id="3f646-115">This attribute does not contain a trusted value.</span></span> <span data-ttu-id="3f646-116">Para comprobar el valor de mérito real del códec, llame a la función [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .</span><span class="sxs-lookup"><span data-stu-id="3f646-116">To verify the codec's actual merit value, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span>

<span data-ttu-id="3f646-117">Si el valor del \_ atributo mérito del códec MFT \_ \_ no coincide con el valor de mérito recuperado [**por MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), se produce un error en el método [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) y se devuelve el mérito de un **\_ \_ \_ códec \_ no válido**.</span><span class="sxs-lookup"><span data-stu-id="3f646-117">If the value of the MFT\_CODEC\_MERIT\_Attribute attribute does not match the merit value retrieved by [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails and returns **MF\_E\_INVALID\_CODEC\_MERIT**.</span></span>

<span data-ttu-id="3f646-118">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3f646-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f646-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f646-119">Requirements</span></span>



| <span data-ttu-id="3f646-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f646-120">Requirement</span></span> | <span data-ttu-id="3f646-121">Value</span><span class="sxs-lookup"><span data-stu-id="3f646-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f646-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f646-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3f646-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="3f646-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="3f646-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f646-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3f646-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="3f646-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3f646-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f646-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f646-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f646-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f646-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f646-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f646-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f646-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3f646-130">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="3f646-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




