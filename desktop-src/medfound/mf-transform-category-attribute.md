---
description: Especifica la categoría de una transformación de Media Foundation (MFT).
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: MF_TRANSFORM_CATEGORY_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3c64fd5e19bba10646957e7c247294b6d82a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275683"
---
# <a name="mf_transform_category_attribute-attribute"></a><span data-ttu-id="2d12c-103">\_Atributo de \_ atributo de categoría de transformación MF \_</span><span class="sxs-lookup"><span data-stu-id="2d12c-103">MF\_TRANSFORM\_CATEGORY\_Attribute attribute</span></span>

<span data-ttu-id="2d12c-104">Especifica la categoría de una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="2d12c-104">Specifies the category for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="2d12c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2d12c-105">Data type</span></span>

<span data-ttu-id="2d12c-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="2d12c-106">**GUID**</span></span>

<span data-ttu-id="2d12c-107">Para obtener una lista de los valores posibles, consulte la [**\_ categoría MFT**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="2d12c-107">For a list of possible values, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

## <a name="getset"></a><span data-ttu-id="2d12c-108">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="2d12c-108">Get/set</span></span>

<span data-ttu-id="2d12c-109">Para obtener este atributo, llame a [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="2d12c-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="2d12c-110">Para establecer este atributo, llame a [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="2d12c-110">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="2d12c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d12c-111">Remarks</span></span>

<span data-ttu-id="2d12c-112">Este atributo se establece en los punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="2d12c-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d12c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d12c-113">Requirements</span></span>



| <span data-ttu-id="2d12c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d12c-114">Requirement</span></span> | <span data-ttu-id="2d12c-115">Value</span><span class="sxs-lookup"><span data-stu-id="2d12c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d12c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d12c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2d12c-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="2d12c-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="2d12c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d12c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2d12c-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="2d12c-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2d12c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d12c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d12c-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d12c-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d12c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d12c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d12c-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2d12c-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2d12c-124">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="2d12c-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




