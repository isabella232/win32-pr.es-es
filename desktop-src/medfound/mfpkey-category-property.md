---
description: Contiene el GUID de categoría de una transformación de Media Foundation (MFT).
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: Propiedad MFPKEY_CATEGORY (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910194"
---
# <a name="mfpkey_category-property"></a><span data-ttu-id="449c4-103">\_Propiedad de categoría MFPKEY</span><span class="sxs-lookup"><span data-stu-id="449c4-103">MFPKEY\_CATEGORY property</span></span>

<span data-ttu-id="449c4-104">Contiene el GUID de categoría de una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="449c4-104">Contains the category GUID for a Media Foundation transform (MFT).</span></span>



<span data-ttu-id="449c4-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="449c4-105">Data type</span></span>

<span data-ttu-id="449c4-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="449c4-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="449c4-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="449c4-107">PROPVARIANT member</span></span>

<span data-ttu-id="449c4-108">**GUID** (**CLSID** \* )</span><span class="sxs-lookup"><span data-stu-id="449c4-108">**GUID** (**CLSID**\*)</span></span>

<span data-ttu-id="449c4-109">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="449c4-109">VT\_CLSID</span></span>

<span data-ttu-id="449c4-110">**puuid**</span><span class="sxs-lookup"><span data-stu-id="449c4-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="449c4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="449c4-111">Remarks</span></span>

<span data-ttu-id="449c4-112">El valor de esta propiedad es un GUID que identifica la categoría MFT.</span><span class="sxs-lookup"><span data-stu-id="449c4-112">The value of this property is a GUID that identifies the MFT category.</span></span> <span data-ttu-id="449c4-113">Para obtener una lista de categorías, consulte la [**\_ categoría MFT**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="449c4-113">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

<span data-ttu-id="449c4-114">Esta propiedad es opcional y solo es meramente informativo.</span><span class="sxs-lookup"><span data-stu-id="449c4-114">This property is optional and is informational only.</span></span> <span data-ttu-id="449c4-115">Una MFT puede usar esta propiedad para informar de la categoría en la que se registra.</span><span class="sxs-lookup"><span data-stu-id="449c4-115">An MFT can use this property to report the category under which it is registered.</span></span> <span data-ttu-id="449c4-116">Para obtener esta propiedad, consulte la MFT para la interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="449c4-116">To get this property, query the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="449c4-117">Para enumerar una categoría MFT, llame a la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .</span><span class="sxs-lookup"><span data-stu-id="449c4-117">To enumerate an MFT category, call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function.</span></span> <span data-ttu-id="449c4-118">No hay ningún vínculo directo entre la función **MFTEnum** y esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="449c4-118">There is no direct link between the **MFTEnum** function and this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="449c4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="449c4-119">Requirements</span></span>



| <span data-ttu-id="449c4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="449c4-120">Requirement</span></span> | <span data-ttu-id="449c4-121">Value</span><span class="sxs-lookup"><span data-stu-id="449c4-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="449c4-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="449c4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="449c4-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="449c4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="449c4-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="449c4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="449c4-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="449c4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="449c4-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="449c4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="449c4-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="449c4-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="449c4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="449c4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="449c4-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="449c4-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="449c4-130">Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="449c4-130">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




