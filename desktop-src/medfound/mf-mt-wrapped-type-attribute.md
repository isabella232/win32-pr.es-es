---
description: Contiene un tipo de medio que se ha ajustado en otro tipo de medio.
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: MF_MT_WRAPPED_TYPE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad09c69f7b99c2c376a207270cadb034e735546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423527"
---
# <a name="mf_mt_wrapped_type-attribute"></a><span data-ttu-id="79c1b-103">\_Atributo de \_ tipo encapsulado MF MT \_</span><span class="sxs-lookup"><span data-stu-id="79c1b-103">MF\_MT\_WRAPPED\_TYPE attribute</span></span>

<span data-ttu-id="79c1b-104">Contiene un tipo de medio que se ha ajustado en otro tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="79c1b-104">Contains a media type that has been wrapped in another media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="79c1b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="79c1b-105">Data type</span></span>

<span data-ttu-id="79c1b-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="79c1b-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="79c1b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79c1b-107">Remarks</span></span>

<span data-ttu-id="79c1b-108">Este atributo se usa en la función [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) , que ajusta un tipo de medio dentro de otro tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="79c1b-108">This attribute is used in the [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function, which wraps a media type inside another media type.</span></span>

<span data-ttu-id="79c1b-109">La función [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="79c1b-109">The [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function does the following:</span></span>

1.  <span data-ttu-id="79c1b-110">Convierte el tipo de archivo multimedia original en una matriz binaria.</span><span class="sxs-lookup"><span data-stu-id="79c1b-110">Converts the original media type into a binary array.</span></span>
2.  <span data-ttu-id="79c1b-111">Establece el atributo de **\_ \_ \_ tipo ajustado MF MT** en el nuevo tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="79c1b-111">Sets the **MF\_MT\_WRAPPED\_TYPE** attribute on the new media type.</span></span> <span data-ttu-id="79c1b-112">El valor del atributo es la matriz binaria.</span><span class="sxs-lookup"><span data-stu-id="79c1b-112">The value of the attribute is the binary array.</span></span>

<span data-ttu-id="79c1b-113">Normalmente, las aplicaciones no usan este atributo directamente.</span><span class="sxs-lookup"><span data-stu-id="79c1b-113">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="79c1b-114">Para desencapsular el tipo de medio original, llame a [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span><span class="sxs-lookup"><span data-stu-id="79c1b-114">To unwrap the original media type, call [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span></span>

<span data-ttu-id="79c1b-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="79c1b-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="79c1b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79c1b-116">Requirements</span></span>



| <span data-ttu-id="79c1b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="79c1b-117">Requirement</span></span> | <span data-ttu-id="79c1b-118">Value</span><span class="sxs-lookup"><span data-stu-id="79c1b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79c1b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79c1b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="79c1b-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="79c1b-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="79c1b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79c1b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="79c1b-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="79c1b-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="79c1b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79c1b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="79c1b-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="79c1b-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79c1b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="79c1b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c1b-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79c1b-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="79c1b-127">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="79c1b-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="79c1b-128">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="79c1b-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="79c1b-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="79c1b-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="79c1b-130">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="79c1b-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




