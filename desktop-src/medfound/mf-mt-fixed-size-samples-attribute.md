---
description: Especifica para un tipo de medio si los ejemplos tienen un tamaño fijo.
ms.assetid: 2d67864a-fd2f-400d-8a1e-e71dc1920593
title: MF_MT_FIXED_SIZE_SAMPLES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1bb5bdd4e1330e4744902ed1b37cc55b7a67a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659849"
---
# <a name="mf_mt_fixed_size_samples-attribute"></a><span data-ttu-id="439be-103">\_Atributo MF MT \_ fixed \_ size \_ Samples</span><span class="sxs-lookup"><span data-stu-id="439be-103">MF\_MT\_FIXED\_SIZE\_SAMPLES attribute</span></span>

<span data-ttu-id="439be-104">Especifica para un tipo de medio si los ejemplos tienen un tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="439be-104">Specifies for a media type whether the samples have a fixed size.</span></span>

## <a name="data-type"></a><span data-ttu-id="439be-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="439be-105">Data type</span></span>

<span data-ttu-id="439be-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="439be-106">**UINT32**</span></span>

<span data-ttu-id="439be-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="439be-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="439be-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="439be-108">Remarks</span></span>

<span data-ttu-id="439be-109">Si este atributo es **true**, todas las muestras de la secuencia tienen el mismo tamaño (en bytes).</span><span class="sxs-lookup"><span data-stu-id="439be-109">If this attribute is **TRUE**, every sample in the stream is the same size (in bytes).</span></span> <span data-ttu-id="439be-110">De lo contrario, los ejemplos pueden variar en tamaño.</span><span class="sxs-lookup"><span data-stu-id="439be-110">Otherwise, samples might vary in size.</span></span>

<span data-ttu-id="439be-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="439be-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="439be-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="439be-112">Requirements</span></span>



| <span data-ttu-id="439be-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="439be-113">Requirement</span></span> | <span data-ttu-id="439be-114">Value</span><span class="sxs-lookup"><span data-stu-id="439be-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="439be-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="439be-115">Minimum supported client</span></span><br/> | <span data-ttu-id="439be-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="439be-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="439be-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="439be-117">Minimum supported server</span></span><br/> | <span data-ttu-id="439be-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="439be-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="439be-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="439be-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="439be-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="439be-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="439be-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="439be-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="439be-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="439be-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="439be-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="439be-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="439be-124">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="439be-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="439be-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="439be-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="439be-126">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="439be-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




