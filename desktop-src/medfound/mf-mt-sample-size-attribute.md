---
description: Especifica el tamaño de cada ejemplo, en bytes, en un tipo de medio.
ms.assetid: 4c28f73d-ff40-4eb9-a45f-57a60df719c6
title: MF_MT_SAMPLE_SIZE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bb897524dac5f73f4d4553f8e77e02ef473f611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687212"
---
# <a name="mf_mt_sample_size-attribute"></a><span data-ttu-id="6918f-103">\_Atributo de \_ tamaño de muestra MF MT \_</span><span class="sxs-lookup"><span data-stu-id="6918f-103">MF\_MT\_SAMPLE\_SIZE attribute</span></span>

<span data-ttu-id="6918f-104">Especifica el tamaño de cada ejemplo, en bytes, en un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6918f-104">Specifies the size of each sample, in bytes, in a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="6918f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6918f-105">Data type</span></span>

<span data-ttu-id="6918f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6918f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6918f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6918f-107">Remarks</span></span>

<span data-ttu-id="6918f-108">Este atributo solo es válido si el atributo [**MF \_ MT \_ fixed \_ size \_ Samples**](mf-mt-fixed-size-samples-attribute.md) es **true**.</span><span class="sxs-lookup"><span data-stu-id="6918f-108">This attribute is valid only if the [**MF\_MT\_FIXED\_SIZE\_SAMPLES**](mf-mt-fixed-size-samples-attribute.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="6918f-109">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6918f-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6918f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6918f-110">Requirements</span></span>



| <span data-ttu-id="6918f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="6918f-111">Requirement</span></span> | <span data-ttu-id="6918f-112">Value</span><span class="sxs-lookup"><span data-stu-id="6918f-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6918f-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6918f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6918f-114">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="6918f-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6918f-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6918f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6918f-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="6918f-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6918f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6918f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="6918f-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6918f-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6918f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="6918f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6918f-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6918f-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6918f-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6918f-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6918f-122">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6918f-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="6918f-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6918f-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6918f-124">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="6918f-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




